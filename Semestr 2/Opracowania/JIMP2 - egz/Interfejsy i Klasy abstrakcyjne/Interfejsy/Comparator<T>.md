Interfejs umożliwia zaimplementowanie metody porównującej dla Obiektów.
Klasy implementujące tą metodę mogą następnie być przekazane do np. klas sortujących.

```java
import java.util.Comparator;

public class Student{
	int points;
	public Student(int points) {
		this.points = points;
	}
}

class sortStudentsByName implements Comparator<Student> {
	@Override
	public int compare(Student s1, Student s2){
		if(s1.points < s2.points) return -1;
		else if(s1.points == s2.points) return 0;
		else if(s1.points > s2.points) return 1;
      // Tu nigdy nie dojdzie, ale konieczne jest aby java wiedziała że coś zwraca, albo ewentualnie wyrzuca błąd
      else throw new RuntimeException();
	}
}
```

# Wykorzystanie w Klasach sortujących
