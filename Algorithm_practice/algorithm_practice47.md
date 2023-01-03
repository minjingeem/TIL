### Algorithm Practice: Day 47

01.03.23            



3052번: 나머지

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.HashSet;

public class Java3052 {
    public static void main(String[] args) throws IOException {
        // 서로 다른 값? HashSet을 사용하면 간단하다!
        // HashSet은 중복원소를 허용하지 않는다.

        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        HashSet<Integer> numbers = new HashSet<Integer>();

        for(int i = 0; i < 10; i++) {
            numbers.add(Integer.parseInt(br.readLine()) % 42);
        }
        System.out.println(numbers.size());
    }
}


```



- HashSet을 활용하여 푼다. 
  - HashSet은 중복원소를 허용하지 않는다. 
  - HashSet.add() 메소드는 HashSet에 저장하는 메소드이다. 처음 생성할 때 HashSet<Integer> 으로 타입을 Integer로 선언했기 때문에 int 형 또는 Integer 객체를 넣어주어야한다.
  - 또한 이 메소드에서 값을 넣을 때 만약 중복되는 값이 없으면 HashSet 에 저장되면서 True 를 반환하고, 만약 중복되어 저장되지 않으면 False 를 반환한다.

- 다른풀이법 참고: https://st-lab.tistory.com/46