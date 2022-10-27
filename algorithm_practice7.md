<h3>Algorithm Practice: Day 7</h3> 

10.20.27

-------

<h5>Basic Level</h5>

1.  예제 출력 1 복사

   ```
   \    /\
    )  ( ')
   (  /  )
    \(__)|
   ```

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
      	// '\' 는 단독으로 출력이 불가능한 문자.
      	// 이때 사용되는 것이 Escape Sequance 라고 한다. 이스케이프 시퀀스는 백슬래시(\) + 문자 의 조합으로 쓰인다.
        System.out.println("\\    /\\");
        System.out.println(" )  ( ')");
        System.out.println("(  /  )");
        System.out.println(" \\(__)|");
                           
    }
}
```



<h5>Thoughts</h5>

- 자바에는 단독으로 출력이 불가능한 문자가 있다!!!
- 이때 사용되는 것이 escape sequence라고 불리는데 사용방법은,  \ + 문자 조합이다.

