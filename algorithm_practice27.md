<h3>Algorithm Practice: Day 27</h3> 

**11.25.22**                                    																														

-------

<h5>Basic Level</h5>

1. ## 문제

   두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

   ## 입력

   입력은 여러 개의 테스트 케이스로 이루어져 있다.

   각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

   ## 출력

   각 테스트 케이스마다 A+B를 출력한다.

   ## 예제 입력 1 복사

   ```
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
오답

import java.io.*;
import java.util.*;

public class Main {
  public static void main(String[] args) throws IOException {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
   
    String value;
    
    while((value=br.readLine()) != null){ //EOF 조건 추가
      StringTokenizer st = new StringTokenizer(br.readLine());
      int A = Integer.parseInt(st.nextToken());
      int B = Integer.parseInt(st.nextToken());
      bw.write((A+B)+ "\n");
    }
    bw.flush();
  }
}
```

```java
정답
  
import java.io.*;
import java.util.*;

public class Main {
  public static void main(String[] args) throws IOException {
    BufferedReader br = new BufferedReader(InputStreamReader(System.in));
    BufferedWriter bw = new BufferedWriter(OutputStreamWriter(System.out));
    
    String value;
    while((value = br.readLine()) != null){ //EOF 조건 추가
      StringTokenizer st = new StringTokenizer(value);
      int A = Integer.parseInt(nextToken());
      int B = Integer.parseInt(nextToken());
      
      bw.write((A+B)+"\n");
    }
    bw.flush();
  }
}
```







<b>Thoughts</b>

- 입력의 종료는 **더이상 읽을 수 있는 데이터 (EOF)** 가 없을 때 종료한다.
- EOF (End Of File)
  - **입력에서** **더이상의 읽을 수 있는 데이터가 존재하지 않을 때** 반복문을 종료

- BufferedReader 의 경우 데이터가 존재하지 않을 때 **null 을 반환**한다. 
