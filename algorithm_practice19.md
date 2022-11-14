<h3>Algorithm Practice: Day 19</h3> 

**11.14.22**                                    																														

-------

<h5>Basic Level</h5>

1. ## 문제

   본격적으로 for문 문제를 풀기 전에 주의해야 할 점이 있다. 입출력 방식이 느리면 여러 줄을 입력받거나 출력할 때 시간초과가 날 수 있다는 점이다.

   C++을 사용하고 있고 `cin`/`cout`을 사용하고자 한다면, `cin.tie(NULL)`과 `sync_with_stdio(false)`를 둘 다 적용해 주고, `endl` 대신 개행문자(`\n`)를 쓰자. 단, 이렇게 하면 더 이상 `scanf`/`printf`/`puts`/`getchar`/`putchar` 등 C의 입출력 방식을 사용하면 안 된다.

   Java를 사용하고 있다면, `Scanner`와 `System.out.println` 대신 `BufferedReader`와 `BufferedWriter`를 사용할 수 있다. `BufferedWriter.flush`는 맨 마지막에 한 번만 하면 된다.

   Python을 사용하고 있다면, `input` 대신 `sys.stdin.readline`을 사용할 수 있다. 단, 이때는 맨 끝의 개행문자까지 같이 입력받기 때문에 문자열을 저장하고 싶을 경우 `.rstrip()`을 추가로 해 주는 것이 좋다.

   또한 입력과 출력 스트림은 별개이므로, 테스트케이스를 전부 입력받아서 저장한 뒤 전부 출력할 필요는 없다. 테스트케이스를 하나 받은 뒤 하나 출력해도 된다.

   자세한 설명 및 다른 언어의 경우는 [이 글](http://www.acmicpc.net/board/view/22716)에 설명되어 있다.

   [이 블로그 글](http://www.acmicpc.net/blog/view/55)에서 BOJ의 기타 여러 가지 팁을 볼 수 있다.

   ## 입력

   첫 줄에 테스트케이스의 개수 T가 주어진다. T는 최대 1,000,000이다. 다음 T줄에는 각각 두 정수 A와 B가 주어진다. A와 B는 1 이상, 1,000 이하이다.

   ## 출력

   각 테스트케이스마다 A+B를 한 줄에 하나씩 순서대로 출력한다.

   ## 예제 입력 1 복사

   ```
   5
   1 1
   12 34
   5 500
   40 60
   1000 1000
   ```

   ## 예제 출력 1 복사

   ```
   2
   46
   505
   100
   2000
   ```

```java
import java.io.*; // java.io.bufferReader; java.io.bufferWriter; // java.io.*;

public class Main{
  public static void main(String[] args){
   BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
   BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
   int T,A,B;
    
   try{// 실행문
     
   }catch(Exception e){// 실행문 이외의 예외가 있을때 실행해줄 문장
     
   }

  }
}
```

````java
import java.io.*;

public class Main{
  public static void main(String[] args) throws IOException{
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
   
    StringTokenizer st = new StringTokenizer(br.readLine()); //데이터 가공
    
    int T = Integer.parseInt(st.nextToken());
    for(int i =1; i <= T; i++){
      int A = Integer.parseInt(st.nextToken());
      int B = Integer.parseInt(st.nextToken());
      
      bw.write((A+B)+"\n");
    }
    bw.flush();
  }
}
````





<b>Thoughts</b>

- Scanner는 키보드 입력이 바로 프로그램으로 전달된다. 하지만 I/O가 자주 일어나면 속도가 느려진다. 
- 그렇기때문에 중간에 Buffer를 두어 한번에 묶어 전달하는 것이 더 효율적이고 빠르다.
- Buffer는 입력을 String으로 받는다
- StringTokenizer는 사용자가 지정한 방식으로 String을 Token화 하여 데이터를 가공한다.(문자열의 제일 작은단위 Token으로 쪼갠다. 자른다.)
  - Ex) 해당 문제에서는 BufferedReader로 읽어온 String 단위별로 자른다.
- nextToken( ) 은 readLine( ) 을 통해 입력받은 값을 공백 단위로 구분하여 순서대로 호출한다. 
- ``"\n"`` : 줄바꿈
- 하지만 못품 ㅠㅠ