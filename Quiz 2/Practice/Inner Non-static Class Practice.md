My attempt:
```
public class Driver {
	public static void main(String[] args) {
		LibraryBook jp = new LibraryBook("Java Programming");
		jp.Status jpStatus = new jp.Status();
		jpStatus.printStatus();
	}
}

public class LibraryBook {
	String title;
	boolean checkedOut;
	
	{
		checkedOut = false;
	}
	
	public LibraryBook(String title) {
		this.title = title;
	}
	
	class Status {
		public printStatus() {
			if (checkedOut) {
				System.out.println("The book " + title + " is checked out.");
			} else {
				System.out.println("The book " + title + " is available.");
			}
		}
	}
}
```

Errors:
- Need return type `void` on `printStatus()` method inside `status` inner class.
- Incorrect creation of inner class. Should be:
	- `LibraryBook.Status jpStatus = jp.new Status()`
	- This is because `LibraryBook` specified the enclosing class, and the `new` keyword has to come after the instance `jp` when creating a new inner class.
Corrected version:
```
public class Driver {
	public static void main(String[] args) {
		LibraryBook jp = new LibraryBook("Java Programming");
		// Fixed
		LibraryBook.Status jpStatus = jp.new Status();
		jpStatus.printStatus();
	}
}

public class LibraryBook {
	String title;
	boolean checkedOut;
	
	{
		checkedOut = false;
	}
	
	public LibraryBook(String title) {
		this.title = title;
	}
	
	class Status {
		public void printStatus() {
			if (checkedOut) {
				System.out.println("The book " + title + " is checked out.");
			} else {
				System.out.println("The book " + title + " is available.");
			}
		}
	}
}
```