### Algorithm Practice: Day 44

12.20.22                            



10871번: 최소값 최대값

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java10871 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        Integer.parseInt(br.readLine());	//첫 줄 N 은 안쓰이므로 입력만 받는다.
        StringTokenizer st = new StringTokenizer(br.readLine()," ");

        int max = -1000001; // 0; 5;
        int min = 1000001; // 11; 5;

        while(st.hasMoreTokens()) {
            int val = Integer.parseInt(st.nextToken()); //5; 3;
            if(val>max) { //5>0 -> max=5; 3>5 -> max = 5;
                max = val;
            }
            if(val<min) { //5<11 -> min=5; 3<5 -> min = 3;
                min = val;
            }
        }
        System.out.println(min + " " + max);
    }
}

```



- Thoughts: 로직이 어렵다 아직. max와 min을 변수로 선언해서 풀어볼 생각을 하기는 했는데 답을 찾지 못해 다른 방식으로 풀다가 틀렸다. 위의 코드는 다른 분 코드를 가져온 것.