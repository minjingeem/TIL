### Algorithm Practice: Day 60

01.27.23            

<복습하기>

1065번: 한수

## 문제

어떤 양의 정수 X의 각 자리가 등차수열을 이룬다면, 그 수를 한수라고 한다. 등차수열은 연속된 두 개의 수의 차이가 일정한 수열을 말한다. N이 주어졌을 때, 1보다 크거나 같고, N보다 작거나 같은 한수의 개수를 출력하는 프로그램을 작성하시오. 

## 입력

첫째 줄에 1,000보다 작거나 같은 자연수 N이 주어진다.

## 출력

첫째 줄에 1보다 크거나 같고, N보다 작거나 같은 한수의 개수를 출력한다.

## 예제 입력 1 복사

```
110
```

## 예제 출력 1 복사

```
99
```

## 예제 입력 2 복사

```
1
```

## 예제 출력 2 복사

```
1
```

## 예제 입력 3 복사

```
210
```

## 예제 출력 3 복사

```
105
```

## 예제 입력 4 복사

```
1000
```

## 예제 출력 4 복사

```
144
```

## 예제 입력 5 복사

```
500
```

## 예제 출력 5 복사

```
119
```

<h2>해결</h2>

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class practice1065 {
    public static void main(String[] args) throws IOException{
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        System.out.print(arithmetic_sequece(Integer.parseInt(br.readLine())));
        
    }
    public static int arithmetic_sequece(int num) {
        int count = 0;
        if(num < 100) { 
            return num; // 굳이 반복문을 이용하여 cout를 하지 않아도 1 - 99 는 모두 한수이기 때문에 num을 사용한다.
        }else {
            count = 99;
            for(int i=100; i <=num; i++ ){ // 100부터 입력받은 수 까지 반복
                int ones = i%10; // 937
                int tens = (i/10)%10;
                int hundreds = i/100;

                if((hundreds - tens) == (tens - ones)) {
                    count++;
                }
            }
        }
        return count;
    }
}


```

- 참고해서 풀음. 풀었다고 할 수 없다..
- https://st-lab.tistory.com/54 참고자료 보고도 어려움