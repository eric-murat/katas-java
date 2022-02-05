Kata Java : Ones and zeros

## Instructions

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
