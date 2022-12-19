### Algorithm Practice: Day 43

12.19.22                            



10807번: 개수세기

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Java10807 {
    public static void main(String[] args) throws IOException, IOException { //void일때만 IOException이 가능한가?
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringBuilder sb = new StringBuilder(); // 출력용

        System.out.println("정수의 총 개수를 입력하세요.");
        int n = Integer.parseInt(br.readLine());
      
      	StringTokenizer st = new StringTokenizer(br.readLine(), " ");
        System.out.println("각 정수를 공백으로 구분하여 입력하세요.");
        int[] numbers = Integer.parseInt(st.nextToken());
      
        System.out.println("찾고 싶은 정수를 입력하세요");
        int v = Integer.parseInt(br.readLine());
        int count = 0;

        for(int i = 0; i < n; i++) {
            if(numbers[i]) == v){
                count++;
            }else{
                count = count;
            }
        }
        sb.append(count);
        System.out.println("정수 "+ v + "은(는) " + sb +"개 있습니다.");
    }
}

```

