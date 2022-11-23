<h3>Algorithm Practice: Day 25</h3> 

**11.23.22**                                    																														

-------

<h5>Basic Level</h5>

1. ## 문제

   두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

   ## 입력

   입력은 여러 개의 테스트 케이스로 이루어져 있다.

   각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

   입력의 마지막에는 0 두 개가 들어온다.

   ## 출력

   각 테스트 케이스마다 A+B를 출력한다.

   ## 예제 입력 1 복사

   ```
   1 1
   2 3
   3 4
   9 8
   5 2
   0 0
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
import java.io.*;
import java.util.*;

public class Main{
  public static void main(String[] args) throws IOException{
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
    
    while(true){
      StringTokenizer st = new StringTokenizer(br.readLine()); //문자열 한 줄을 한번에 입력받음(공백함께)
      int A = Integer.parseInt(st.nextToken());//StirngTokenizer을 이용하여 문자열을 분리해 꺼내오는 nextToken은 문자열반환
      int B = Integer.parseInt(st.nextToken());
      if(A==0 && B==0){
        break;
      }
      bw.write((A+B)+"\n");
    }
    bw.flush();
  }
}
```







<b>Thoughts</b>

- BufferedReader와 BufferedWriter의 기본 로직을 이해해야한다. 공부필요!! 
- 이번주말에는 지금까지 푼 알고리즘 정리 및 오답시간을 가져야겠다.

