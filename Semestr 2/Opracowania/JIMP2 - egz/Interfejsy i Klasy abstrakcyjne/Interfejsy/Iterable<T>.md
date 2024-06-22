# Iterator
Najpierw należy stworzyć klasę implementującą `Iterator<T>`.
Wymagane metody to:
- `boolean hasNext()` - zwraca prawdę jeżeli są następne elementy.
- `E next()` - Zwraca następny element, oraz przesuwa 'wskaźnik'

> [!TIP] Dostęp do niepublicznych zmiennych i metod
> Aby mieć dostęp do wewnętrznych metod oraz zmiennych można zaimplementować iterator w środku klasy implementującej `Iterable<T>`.

# Iterable
Klasa implementująca `Iterable<T>` musi zaimplementować jedynie metodę `Iterator<T> iterator()` zwracającą instancję `Iteratora`

# Przykład
Student:
```java
class Student {
	public int studentIndex;
	public Student(int studentIndex) {
		this.studentIndex = studentIndex;
	}
}
```
Group:
```java
import java.util.*;

class Group implements Iterable<Student> {
	private int studentCount;
	private Student[] students;
	
	public Group(int studentCount){
	  this.studentCount = studentCount;
		this.students = new Student[studentCount];
		for(int i = 0; i < studentCount; i++) {
			this.students[i] = new Student(i);
		}	
	}
	@Override
	public Iterator<Student> iterator(){
		return new Iterator<Student>() {
			private int currentIndex = 0;
			private int size = studentCount;
			private Student[] students;
			
			{
				students = Arrays.copyOf(Group.this.students, Group.this.students.length);
			}
			
			@Override
			public boolean hasNext(){
				return currentIndex < size;
			}
			@Override
			public Student next(){
				return students[currentIndex++];
			}
		};
	}
  }
}
```
Main:
```java
class Main{
	public static void main(String[] args){
    Group group = new Group(100);
    for(Student student : group){
      System.out.println(student.studentIndex);
    }
}
```
Wypisze to numery studentów od $0..99$
