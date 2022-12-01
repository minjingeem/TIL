<h3>Algorithm Practice: Day 16</h3> 

**11.10.22**                                    																														HAPPY 10 YEARS ANNIVERSARY!!

-------

<h5>Basic Level</h5>

1. ## 문제

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



```java
import java.util.*;

public class Main{
  public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    int T,A,B;
    T = sc.nextInt();
    for(int i=1; i<=T; i++ ){
      A = sc.nextInt();
      B = sc.nextInt();
      System.out.println(A+B);
    }
  }
}
```
 



2.  n이 주어졌을 때, 1부터 n까지 합을 구하는 프로그램을 작성하시오.

   첫째 줄에 n (1 ≤ n ≤ 10,000)이 주어진다.

   ```` java
   import java.util.*;
   
   public class Main{
     public static void main(String[] args){
       Scanner sc = new Scanner(System.in);
       int n;
       int sum = 0;
       n = sc.nextInt();
       for(int i = 1; i <= n ; i++){
         sum += i;
       }
         System.out.println(sum);
     }
   }
   ````

   

   

<b>Thoughts</b>

- ``+=`` : A += B 의 의미는 A = A+B라는 의미