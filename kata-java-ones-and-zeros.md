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

## Docs
- Collections.reverse :
- Math.pow : 
