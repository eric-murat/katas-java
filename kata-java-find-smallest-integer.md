
## Instructions

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
