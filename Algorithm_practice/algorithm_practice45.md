### Algorithm Practice: Day 45

12.27.22                            



10871번: 최소값 최대값

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java10818practice2 {
    public static void main(String[] args) throws IOException {
      
        // 기존에 있는 숫자와 입력받은 숫자를 비교하여 최소, 최대를 구한다.
        // 1. 처음에 입력받은 숫자는 기준이 없음으로 최소,최대에 모두 배치한다.
        // 1-1. 처음에 입력받은 숫자를 최소,최대에 모두 배치하려면?
        // 2. 처음에 배치된 최소,최대 값을 기준으로 숫자를 비교한다.
        // 3. 입력받은 숫자가 현재의 최소값보다 작으면 최소값 업데이트, 최대값보다 크면 최대값 업데이트
      
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int min = 1000001;
        int max = -1000001;

        StringTokenizer st = new StringTokenizer(br.readLine());
        while(st.hasMoreTokens()) {
            int num = Integer.parseInt(st.nextToken());
            if(num < min) {
                min = num;
            }if (num > max) {
                max = num;
            }
        }
        StringBuilder sb = new StringBuilder();
        sb.append(min).append(" ").append(max);
        System.out.println(sb);
    }
}

```



- 나름의 로직을 만들어 문제를 풀긴 했지만 여전히 왜 최솟값 최대값 변수를 저렇게 설정해야하는지 정확하게 이해를 못한상태다. 그래도 일주일만에 다시 공부를 시작했는데 오히려 감이 더 좋아진 느낌이다.

