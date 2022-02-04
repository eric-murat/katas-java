Kata Java : Find the smallest integer in the array https://www.codewars.com/kata/55a2d7ebe362935a210000b2

## Instructions
Given an array of integers your solution should find the smallest integer.  
For example:  
Given `[34, 15, 88, 2]` your solution will return `2`  
Given `[34, -345, -1, 100]` your solution will return `-345`  
You can assume, for the purpose of this kata, that the supplied array will not be empty.

✒️ FUNDAMENTALS

## Mon code
```java
import java.util.Arrays;

public class SmallestIntegerFinder {
    public static int findSmallestInt(int[] args) {
      Arrays.sort(args);
      return args[0];
    }
}
```

## Code de la communauté
```java
import java.util.stream.IntStream;

public class SmallestIntegerFinder {
    public static int findSmallestInt(int[] args) {
        return IntStream.of(args).min().getAsInt();
    }
}
```

## Docs
- Arrays.sort : https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html#sort(short[])
