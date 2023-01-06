### Algorithm Practice: Day 50

01.06.23            



8958번: OX퀴즈

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java8958 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine()); //3
        String[] array = new String[n];

        StringBuilder sb = new StringBuilder();
        for(int i = 0; i < n; i++) {
            array[i] = br.readLine(); // [OOXXOO OXXXXO OOX]
        }
        for(int i = 0; i < n; i++) { //0
            int cnt = 0;
            int sum = 0;
            for(int j = 0; j < array[i].length(); j++) { //6
                if(array[i].charAt(j) == 'O') {
                    cnt = cnt + 1; //1 2
                }else { // "X"
                    cnt = 0;
                }
                sum = sum + cnt; //1 3 3
            }
            sb.append(sum).append('\n');
        }
        System.out.println(sb);
    }
}

```





- 배열을 어떻게 어디에 활용 할 것인가?를 잘 생각해보기
- ``charAt`` 을 활용하여 푸는 문제. 