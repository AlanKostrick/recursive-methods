# recursive-methods

## Objectives:
- Students will be able to run and test recursive methods and map their output 
- Students will be able to develop a basic understanding of the functionalities of recursive method calls

## Your task:
- Execute each of these code blocks in Eclipse to see the end result...sketch the process that gets us there from start to finish
- Follow along with my instructional video to see how I have build out the first few examples

``` java
public int mystery(int n) {
		if(n<0) {
			return n*2;
		} else {
			return mystery(n-1) + mystery(n-2);
		}
	}
```
