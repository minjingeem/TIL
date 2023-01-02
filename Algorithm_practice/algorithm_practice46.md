### Algorithm Practice: Day 46

01.02.23 HAPYY NEW YEAR'S                     



55971번: 과제 안내신분?

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Java5597 {
    public static void main(String[] args) throws IOException {
       BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
       int[] numbers = new int[31]; // index 0 - 30
       numbers[0] = 0;
       for(int i = 0; i < 28; i++) { // repeat 28 times
           int num = Integer.parseInt(br.readLine());
           numbers[num] = num; //ex) number[3] = 3
       }
       for(int i = 0; i < 31; i ++) {
           if(numbers[i] != i) {
               System.out.println(i);
           }
       }
    }
}

```



- 생각보다 빠르고 쉽게 풀었다!

  - 인덱스 번호를 0부터 30번까지 만들고 입력받은 숫자와 같은 인덱스 번호에 입력받은 숫자를 담는다

    Ex) index[1] = 1, index[10] = 10, index[27] = 27

    인덱스번호와 입력받은 번호가 같다-> 인덱스번호가 출석번호가 된다. 

  - 인덱스 번호와 입력번호가 같지 않은경우(값이 없는 경우 포함), 출력한다.

