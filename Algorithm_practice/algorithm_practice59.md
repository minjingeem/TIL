### Algorithm Practice: Day 59

01.26.23            

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
        int num = Integer.parseInt(br.readLine());
        int n = f(num);
    }
    public static int f(int number) {
        int count = 0;
        if(number < 100) {
            count++;
        }
        else if(number>99 && number<1000) {
            
        }
    }
}

```

- 약간 햇갈리기 시작함