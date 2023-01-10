### Algorithm Practice: Day 52

01.10.23            



15596번: 정수 N개의 합

```java

public class Test {
    long sum(int[] a) {
        long sum = 0; // a 배열 정수 합 변수

        for(int i = 0; i < a.length; i++){
            sum = sum + a[i];
        }
        return sum;
    }
}

```





- 문제는 어렵지 않지만 함수를 작성하는 방법이 익숙치 않다.

