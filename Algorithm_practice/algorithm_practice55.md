### Algorithm Practice: Day 55

01.17.23            

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
public class Java4673 {
    public static void main(String[] args) {
        //
        boolean[] check = new boolean[10001];

        for(int i = 1; i < 10001; i++) { //1 2 3 ..... 10000
            int n = d(i);

            //
            if(n < 10001) {
                check[n] = true;
            }
        }
        //
        StringBuilder sb = new StringBuilder();
        for(int i = 1; i < 10001; i++) {
            if(check[i] != true) {
                sb.append(i).append('\n');
            }
        }
        System.out.println(sb);
    }
    public static int d(int number) { //1 2 3 ..... 10000
        int sum = number; //937

        while(number != 0) {
            sum = sum + (number%10); // number + 1의 자리수
            number = number/10; // 1의 자리수 제거.... 0 이되면 반복문이 끝난다.
        }

        return sum;
    }
}

```





- 다른 분 코드 참고해서 풀었다. 다시 공부 꼭꼭 해야됨.

