### Algorithm Practice: Day 49

01.05.23            



1546번: 평균

```java
// 코드 길이는 더 길고, 속도는 아래와 같고 메로리를 덜 차지 한다.
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java1546 {
    public static void main(String[] args) throws IOException { // IOException 왜 사용하는지 정확히 이해할 필요가있다.
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        float[] scores = new float[n];
        float max = 0;
        StringTokenizer st = new StringTokenizer(br.readLine());
        for(int i = 0; i < n; i++) {
            int score = Integer.parseInt(st.nextToken());
            scores[i] = score;
            if(score > max) {
                max = score;
            }
        }
        float sum = 0;
        for(int i = 0; i < n; i++) {
            float newScore = (scores[i]/max)*100;
            sum = sum+newScore;
        }
        System.out.println(sum/n);
    }
}

```

```java
// 코드 길이는 짧지만, 속도는 위에와 같고 메모리를 더 많이 차지함.

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java1546 {
    public static void main(String[] args) throws IOException { // IOException 왜 사용하는지 정확히 이해할 필요가있다.
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        float[] scores = new float[n];
        float max = 0;
      	float sum = 0;
        StringTokenizer st = new StringTokenizer(br.readLine());
        for(int i = 0; i < n; i++) {
            int score = Integer.parseInt(st.nextToken());
            scores[i] = score;
            if(score > max) {
                max = score;
            }
          	sum = sum + scores[i];
        }
        System.out.println((sum/max*100)/n);
    }
}

```



- 왜 틀렸는지 모르겠다.. 연구가 필요하다.
- 업데이트! 알아냈다!!!
  - 자료형이 정수/정수 일때 ``/`` 연산은 정수형태의 몫의 값만 구한다. Ex) 3/4 =0, 5/4 = 1 
  - 자료형이 정수/실수(하나이상이 실수) 일때 ``/`` 연산은 실수형태의 몫의 값을 구한다. Ex) 3/4 = 0.75, 1.25