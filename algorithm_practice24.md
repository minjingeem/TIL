<h3>Algorithm Practice: Day 24</h3> 

**11.22.22**                                    																														

-------

<h5>Basic Level</h5>

1. ## 문제

   첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제

   하지만, 오른쪽을 기준으로 정렬한 별(예제 참고)을 출력하시오.

   ## 입력

   첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

   ## 출력

   첫째 줄부터 N번째 줄까지 차례대로 별을 출력한다.

   ## 예제 입력 1 복사

   ```
   5
   ```

   ## 예제 출력 1 복사

   ```
       *
      **
     ***
    ****
   *****
   ```

```java
import java.util.*;

public class Main{
  public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    
    int N = sc.nextInt(); //3
    in.close();
    
    for(int i=1; i<=N; i++){ // 1..2..3
      for(int j=1; j<=N-i; j++){ //3-1..3-2..3-3
        System.out.print(" ");
      }
      for(int k=1; k<=i; k++){
        System.out.print("*");
      }
      System.out.println();
    }
  }
}
```







<b>Thoughts</b>

- 어렵다.. 두번 생각해야한다.
- print 와 println의 속성 활용!!

