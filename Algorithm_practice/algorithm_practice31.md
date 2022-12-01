<h3>Algorithm Practice: Day 30, 31</h3> 

**11.29.22** , 11.30.22,                                    																														

-------

입출력과 사칙연산, 조건문, 반복문 복습



```java
import java.util.*;

public class Q2557 {
  public static void main(String[] args) {
    System.out.println("Hello World!");
  }
}

```



```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
      
        //StringTokenizer st = new StringTokenizer(br.readLine()," ");
      	String str = br.readLine();
      	StringTokenizer st = new StringTokenizer(str, " ")// 객체 생성 할 때 StringTokenizer( "문자열" , 구분자 )
      	
        
        int A = Integer.parseInt(st.nextToken());
        int B = Integer.parseInt(st.nextToken());
        
        System.out.println(A+B);
    }
}
```

https://www.webucator.com/article/how-to-use-systemin-in-java/

- <i><b>System.in</b></i> 
  - 키보드에서 Input Stream을 제공한다 -> 키보드로부터 오는 데이터를 받을 수 있는 Stream을 만든다.
- <i><b>InputStreamReader</b></i>
  - 키보드로부터 오는 데이터 Stream을 읽는다.
- <i><b>BufferedReader</b></i>
  - BufferedReader 객체는 input을 버퍼에 담는다

