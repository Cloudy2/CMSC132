```
public class Driver {
	public static main(String[] args) {
		int[] arr = {90, 85, 95};
		Student a = new Student("Alex", arr);
		Student b = new Student(a);
		b.changeGrade(0, 100);
		System.out.println(a.getGrade(0));
		System.out.println(b.getGrade(0));
	}
}

public class Student {
	private String name;
	private int[] grades;
	
	public Student(String name, int[] grades) {
		this.name = name;
		this.grades = grades;
	}
	
	public Student(Student other) {
		this.name = other.name;
		this.grades = Arrays.copyOf(other.grades, other.grades.length);
	}
	
	public void changeGrade(int index, int grade) {
		grades[index] = grade;
	}
	
	public int getGrade(int index) {
		return grades[index];
	}
}
```