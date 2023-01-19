### Algorithm Practice: Day 56

01.19.23            

<복습하기>

15596번: 정수 N개의 합

<h2>문제

정수 n개가 주어졌을 때, n개의 합을 구하는 함수를 작성하시오.

- Java : long sum(int[] a); (클래스 이름: Test)

  - `a`: 합을 구해야 하는 정수 `n`개가 저장되어 있는 배열 (0 ≤ a[i] ≤ 1,000,000, 1 ≤ n ≤ 3,000,000)
  - 리턴값: `a`에 포함되어 있는 정수 `n`개의 합



<h2>해결</h2>

```java
public class Test {
    long sum(int[] a) { // int[] a = 합을 구해야하 하는 정수 n개가 저장되어 있는 배열
        long cum = 0; // a 배열 정수 합을 누적할 변수인 'cum'설정 & initialize

        for(int i = 0; i < a.length; i++){
            cum = cum + a[i];
        }
        return cum;
    }
}

```



1. long 데이터타입의 sum은 int[] a를 인자로한 함수이다.

   1-1. int[] a = 합을 구해야하 하는 정수 n개가 저장되어 있는 배열이다.

   1-1. long형 함수임으로, long형으로 값을 리턴받아야 한다.

2. a 배열의 정수의 합을 누적할 변수인 cum을 설정하고 initialize를 한다.

3. a 배열의 길이만큼 반복문을 돌려, a 배열의 각 인덱스 값에 있는 값을 누적하여 더한다.

4. 누적합(cumulative sum)을 리턴한다.

*리턴받아야 하는 값의 데이터 타입과 함수의 데이터 타입과 같아야 한다!
