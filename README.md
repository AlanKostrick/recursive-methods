# recursive-methods

## Objectives:
- Students will be able to run and test recursive methods and map their output 
- Students will be able to develop a basic understanding of the functionalities of recursive method calls
- Students will understand the 2 parts of a recursive method call

## Your task:
- Execute each of these code blocks in Eclipse to see the end result...sketch the process that gets us there from start to finish
- Follow along with my instructional video to see how I have build out the first few examples

## Base Case vs. Case that iterates closer and closer to termination
- **Base Case**: Will be the final run in the recursive method call (because it needs to exit at some point)
- **Iterative Case** Will bring the method closer to the base with each iteration 

### Example #1

```java
public int mystery(int n) {
		if(n<0) {
			return n*2;
		} else {
			return mystery(n-1) + mystery(n-2);
		}
	}
```

### Example #2

```java
public int mystery(int n, int a, int b) {
		if(n==0) {
			return a;
		} else {
			return b* mystery(n-1, a, b);
		}
	}
```

### Example #3

```java
public int recur(int n) {
		if(n <= 10) {
			return n*2;
		} else {
			return recur(recur(n/3));
		}
	}
```

### Example #4

```java 
	public int recur(int n, int a, int b) {
		if(n==1) {
			return a;
		} else {
			return b + recur(n-1, a, b);
		}
	}
```

### Example #5

```java
	public int recur(int k, int n) {
		if (n == k) {
			return k;
		} else {
			if (n > k) {
				return recur(k, n - k);
			} else {
				return recur(k - n, n);
			}
		}
	}
```

### Example #6

```java
	public int result(int n) {
		if(n==1) {
			return 2;
		} else {
			return 2 * result(n-1);
		}
	}
```

### The application class to check output for these methods

```java
import java.util.Scanner;

public class RecursiveApp {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);

		RecursiveMethods demo = new RecursiveMethods();

		System.out.println("Enter the example # you would like to test");
		System.out.println("Enter 1 for a call to mystery(4)");
		System.out.println("Enter 2 for a call to mystery(4,3,5)");
		System.out.println("Enter 3 for a call to recur(27)");
		System.out.println("Enter 4 for a call to recur(3,2,6)");
		System.out.println("Enter 5 for a call to recur(6,8)");
		System.out.println("Enter 6 for a call to result(5)");
		int example = input.nextInt();

		if (example == 1) {
			System.out.println("a call to mystery(4) produces a value of: " + demo.mystery(4));
		} else if (example == 2) {
			System.out.println("a call to mystery(4,3,5) produces a value of: " + demo.mystery(4, 3, 5));
		} else if (example == 3) {
			System.out.println("a call to recur(27) produces a value of: " + demo.recur(27));
		} else if (example == 4) {
			System.out.println("a call to recur(3,2,6) produces a value of: " + demo.recur(3, 2, 6));
		} else if (example == 5) {
			System.out.println("a call to recur(6,8) produces a value of: " + demo.recur(6, 8));
		} else if (example == 6) {
			System.out.println("a call to result(5) produces a value of: " + demo.result(5));
		} else {
			System.out.println("invalid input");
		}

	}

}
```


