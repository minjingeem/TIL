<h3>Algorithm Practice: Day 5</h3> 

10.26.22

-------

<h5>Basic Level</h5>

1. (세 자리 수) × (세 자리 수)는 다음과 같은 과정을 통하여 이루어진다.

   ![img](https://www.acmicpc.net/upload/images/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png)

   (1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램을 작성하시오.

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
      Scanner sc = new Scanner(System.in);
      int A = sc.nextInt();
      String B = sc.next();
      
      int C = A * (B.charAt(2)-'0');// charAt을 사용하면 아스키코드의 result 값이 담김으로 '0'을 해줌으로써 문자자체를 담게 함.
      int D = A * (B.charAt(1)-'0');
      int E = A * (B.charAt(0)-'0');
      int F = A * (Integer.parseInt(B));// String을 int형으로 바꾸기
      
      System.out.println(C); 
      System.out.println(D);
      System.out.println(E);
      System.out.println(F);

    }
}
```



```java
import java.util.*;

public class Main{
    public static void main(String[] args){
      Scanner sc = new Scanner(System.in);
      int A = sc.nextInt(); // 472
      int B = sc.nextInt(); // 385
      
      int C = A * (B%10); // 385/10 = 38 ... 5
      int D = A * ((B/10)%10); // 385/10 = 38, 38/10 = 3 ... 8
      int E = A * (B/100);
      int F = A * B;
      
      System.out.println(C); 
      System.out.println(D);
      System.out.println(E);
      System.out.println(F);

    }
}
```

<h5>Thoughts</h5>

- 여러가지 풀이 방법 익히기!!
- 응용이 중요!

