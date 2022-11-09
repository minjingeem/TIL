<h3>Algorithm Practice: Day 15</h3> 

**11.9.22**

-------

<h5>Basic Level</h5>

1. ## 문제

   N을 입력받은 뒤, 구구단 N단을 출력하는 프로그램을 작성하시오. 출력 형식에 맞춰서 출력하면 된다.

   ## 입력

   첫째 줄에 N이 주어진다. N은 1보다 크거나 같고, 9보다 작거나 같다.

   ## 출력

   출력형식과 같게 N*1부터 N*9까지 출력한다.

   ## 예제 입력 1 복사

   ```
   2
   ```

   ## 예제 출력 1 복사

   ```
   2 * 1 = 2
   2 * 2 = 4
   2 * 3 = 6
   2 * 4 = 8
   2 * 5 = 10
   2 * 6 = 12
   2 * 7 = 14
   2 * 8 = 16
   2 * 9 = 18
   ```



```java
import java.util.*;

public class Main{
  public static void main(String[] args){
    Scanner scan = new Scanner(System.in);
    int N;
    N = scan.nextInt();
    
    for(int i=1; i <= 9 ; i++){
      System.out.println(N + " * " + i + " = " + N*i);
    }
  }
}
```



2. 문제

   두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

   ## 입력

   첫째 줄에 테스트 케이스의 개수 T가 주어진다.

   각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

   ## 출력

   각 테스트 케이스마다 A+B를 출력한다.

   ## 예제 입력 1 복사

   ```
   5
   1 1
   2 3
   3 4
   9 8
   5 2
   ```

   ## 예제 출력 1 복사

   ```
   2
   5
   7
   17
   7
   ```



````java
import java.util.*;
public class Main{
  public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    int T,A,B;
    T = sc.nextInt();
    A = sc.nextInt();
    B = sc.nextInt();
    
    for(int i = 1; i <= T; i++){
      System.out.println(A+B);
    }
  }
}
````







<b>Thoughts</b>

- 예제 출력을 잘 확인. 연산사이에 공백이 있을때, 출력할때 같은 형식을 따라야한다.
- 마지막 문제 틀림.

