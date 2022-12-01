<h3>Algorithm Practice: Day 21</h3> 

**11.16.22**                                    																														

-------

<h5>Basic Level</h5>

1. ## 문제

   두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

   ## 입력

   첫째 줄에 테스트 케이스의 개수 T가 주어진다.

   각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

   ## 출력

   각 테스트 케이스마다 "Case #x: "를 출력한 다음, A+B를 출력한다. 테스트 케이스 번호는 1부터 시작한다.

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
   Case #1: 2
   Case #2: 5
   Case #3: 7
   Case #4: 17
   Case #5: 7
   ```

   

```java
import java.io.*; // input,output 관련 Buffer사용하기 위해 
import java.util.*; 

public class Main{
  public static void main(String[] args) throws IOException{
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
    
    int T = Integer.parseInt(br.readLine());
    for(int i = 1; i<=T; i++){
      StringTokenizer st = new StringTokenizer(br.readLine());
      
      int A = Integer.parseInt(st.nextToken());
      int B = Integer.parseInt(st.nextToken());
      
      bw.write("Case #"+i+":"+" "+(A+B)+"\n");
    }
    bw.flush();
  }
}


```







<b>Thoughts</b>

- Scanner는 키보드 입력이 바로 프로그램으로 전달된다. 하지만 I/O가 자주 일어나면 속도가 느려진다. 
- 그렇기때문에 중간에 Buffer를 두어 한번에 묶어 전달하는 것이 더 효율적이고 빠르다.
- Buffer는 입력을 String으로 받는다
- ``InputStreamReader``  는 byte를 읽어서 character로 변환해준다. 
- ``OutputStreamWriter`` 는 character를 읽어서 byte로 변환해준다.
- StringTokenizer는 사용자가 지정한 방식으로 String을 Token화 하여 데이터를 가공한다.(문자열의 제일 작은단위 Token으로 쪼갠다. 자른다.)
  - Ex) 해당 문제에서는 BufferedReader로 읽어온 String 단위별로 자른다.
- nextToken( ) 은 readLine( ) 을 통해 입력받은 값을 공백 단위로 구분하여 순서대로 호출한다. 
- ``"\n"`` : 줄바꿈
- 이전 문제와 같음. Input Output Stream에 대한 이해가 필요.

