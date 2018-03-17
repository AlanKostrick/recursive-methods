# recursive-methods

## Objectives:
- Students will be able to run and test recursive methods and map their output 
- Students will be able to develop a basic understanding of the functionalities of recursive method calls

## Your task:
- Execute each of these code blocks in Eclipse to see the end result...sketch the process that gets us there from start to finish
- Follow along with my instructional video to see how I have build out the first few examples

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
public int recur(int a, int b) {
		if(a==b) {
			return a;
		} else {
			if (b>a) {
				return recur(a, b-a);
			} else {
				return recur(b-a, b);
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


