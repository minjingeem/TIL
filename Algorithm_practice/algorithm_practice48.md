### Algorithm Practice: Day 48

01.04.23            



1546번: 평균

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java1546 {
    public static void main(String[] args) throws IOException { // IOException 왜 사용하는지 정확히 이해할 필요가있다.
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int[] scores = new int[n];
        int max = 0;
        StringTokenizer st = new StringTokenizer(br.readLine());
        for(int i = 0; i < n; i++) {
            int score = Integer.parseInt(st.nextToken());
            scores[i] = score;
            if(score > max) {
                max = score;
            }
        }
        int sum = 0;
        for(int i = 0; i < n; i++) {
            int newScore = (scores[i]/max)*100;
            sum = sum+newScore;
        }
        System.out.println(sum/n);
    }
}

```



- 왜 틀렸는지 모르겠다.. 연구가 필요하다.
