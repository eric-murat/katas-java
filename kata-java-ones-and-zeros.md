Kata Java : Ones and zeros

## Instructions
Given an array of ones and zeroes, convert the equivalent binary value to an integer.

Eg: [0, 0, 0, 1] is treated as 0001 which is the binary representation of 1.

Examples:

Testing: [0, 0, 0, 1] ==> 1
Testing: [0, 0, 1, 0] ==> 2
Testing: [0, 1, 0, 1] ==> 5
Testing: [1, 0, 0, 1] ==> 9
Testing: [0, 0, 1, 0] ==> 2
Testing: [0, 1, 1, 0] ==> 6
Testing: [1, 1, 1, 1] ==> 15
Testing: [1, 0, 1, 1] ==> 11
However, the arrays can have varying lengths, not just limited to 4.

✒️ FUNDAMENTALSARRAYS

## Mon code
```java
import java.util.*;

public class BinaryArrayToNumber {

    public static int ConvertBinaryArrayToInt(List<Integer> binary) {
        Collections.reverse(binary);
        int res = 0;
        for (int i = 0; i < binary.size(); i++) {
          if (binary.get(i) > 0) res = res + (int)Math.pow(2,i);
        }
        return res;
    }
}
```

## Code de la communauté
```java
import java.util.List;

public class BinaryArrayToNumber {

    public static int ConvertBinaryArrayToInt(List<Integer> binary) {
        return binary.stream().reduce((x, y) -> x * 2 + y).get();
    }
}
```

## Docs
- Collections.reverse : https://docs.oracle.com/javase/7/docs/api/java/util/Collections.html#reverse(java.util.List)
- Math.pow : https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#pow-double-double-
