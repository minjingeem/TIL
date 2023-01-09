### Algorithm Practice: Day 51

01.09.23            



4344번

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java4344 {
    public static void main(String[] args) throws IOException {
        BufferedReader  br = new BufferedReader(new InputStreamReader(System.in));
        System.out.println("테스트 케이스 개수를 입력해주세요.");
        int C = Integer.parseInt(br.readLine()); // 테스트케이스 개수 입력받기
        for(int i = 0; i < C; i++) { // 각 테스트케이스의 정보 입력받기
            System.out.println("학생의 수와 점수를 공백단위로 입력해 주세요.");
            StringTokenizer st = new StringTokenizer(br.readLine());
            int n = Integer.parseInt(st.nextToken());// 총 점수의 개수
            int[] array = new int[n];
            int sum = 0;
            float cnt = 0;
            for( int j = 0; j < n; j++) { // 점수 입력받기
                int num = Integer.parseInt(st.nextToken());
                array[j] = num;
                sum = sum + num;
                System.out.println("sum의 값은 " + sum);
            }
            for(int j = 0; j < n; j++) {
                if(array[j] > sum/n ) {
                    cnt = cnt + 1;
                }else{
                    cnt = cnt;
                }
                System.out.println("cnt의 값은 " + cnt);
            }
            float result = (cnt/n)*100;
            System.out.println(String.format("%.3f", result)+"%");
        }
    }
}

```





- ``String.format("%.3f", 포멧을 적용할 데이터)`` 활용 

