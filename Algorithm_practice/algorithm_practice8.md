<h3>Algorithm Practice: Day 8</h3> 

10.28.22

-------

<h5>Basic Level</h5>

1. 예제 출력 

```

|\_/|
|q p|   /}
( 0 )"""\
|"^"`    |
||_/=\\__|

```

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
      	// '\' 는 단독으로 출력이 불가능한 문자.
      	// 이때 사용되는 것이 Escape Sequance 라고 한다. 이스케이프 시퀀스는 백슬래시(\) + 문자 의 조합으로 쓰인다.
        System.out.println("|\\_/|");
        System.out.println("|q p|   /}");
        System.out.println("( 0 )\"\"\"\\");
        System.out.println("|\"^\"`    |");
        System.out.println("||_/=\\\\__|");
                           
    }
}
```





2. 예제 출력 

```
         ,r'"7
r`-_   ,'  ,/
 \. ". L_r'
   `~\/
      |
      |
```

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
      	// '\' 는 단독으로 출력이 불가능한 문자.
      	// 이때 사용되는 것이 Escape Sequance 라고 한다. 이스케이프 시퀀스는 백슬래시(\) + 문자 의 조합으로 쓰인다.
        System.out.println("         ,r'\"7");
        System.out.println("r`-_   ,'  ,/");
        System.out.println(" \\. \". L_r'");
        System.out.println("   `~\\/");
        System.out.println("      |");
      	System.out.println("      |");
                           
    }
}
```



-------

입출력과 사칙연산 끝, 조건문 시작!

-------------



3. 문제

   두 정수 A와 B가 주어졌을 때, A와 B를 비교하는 프로그램을 작성하시오.

   첫째 줄에 A와 B가 주어진다. A와 B는 공백 한 칸으로 구분되어져 있다.

   

   첫째 줄에 다음 세 가지 중 하나를 출력한다.

   - A가 B보다 큰 경우에는 '`>`'를 출력한다.
   - A가 B보다 작은 경우에는 '`<`'를 출력한다.
   - A와 B가 같은 경우에는 '`==`'를 출력한다.

   

   - -10,000 ≤ A, B ≤ 10,000

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int A,B;
        A = sc.nextInt();
        B = sc.nextInt();
        
        sc.close();
        
        if(A>B){
            System.out.println(">");
        }else if(A<B){
            System.out.println("<");
        }else{
            System.out.println("==");
        }
        
    }
}
```



4. 문제

   시험 점수를 입력받아 90 ~ 100점은 A, 80 ~ 89점은 B, 70 ~ 79점은 C, 60 ~ 69점은 D, 나머지 점수는 F를 출력하는 프로그램을 작성하시오.

   

   첫째 줄에 시험 점수가 주어진다. 시험 점수는 0보다 크거나 같고, 100보다 작거나 같은 정수이다.

   

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int score;
        score = sc.nextInt();
        sc.close();
        
      // 위에서부터 순서대로 돌아간다.
        if(score >= 90){
            System.out.println("A");
        }else if(score >= 80){
            System.out.println("B");
        }else if(score >= 70){
            System.out.println("C");
        }else if(score >= 60){
            System.out.println("D");
        }else{
            System.out.println("F");
        }
        
    }
}
```



<h5>Thoughts</h5>

- 자바에는 단독으로 출력이 불가능한 문자가 있다!!!
- 이때 사용되는 것이 escape sequence라고 불리는데 사용방법은,  \ + 문자 조합이다.
- 단독출력불가 문자: ``\``, ``"`` 

