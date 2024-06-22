Interfejs umożliwia zaimplementowanie metody porównującej dla Obiektów.
Klasy implementujące tą metodę mogą następnie być przekazane do między innymi klas sortujących.

```
import java.utils.*;

class Student{
	int points;
	Student(int points) {
		this.points = points;
	}
}

class sortStudentsByName implements Comparator<Student> {
	@Override
	public int compare(Student s1, Student s2){
		if(s1.points < s2.points) return -1;
		else if(s1.points == s2.points) return 0;
		else if(s1.points > s2.points) return 1;
	}
}
```

# Wykorzystanie w Klasach sortujących
