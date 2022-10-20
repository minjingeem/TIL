<h3>Algorithm Practice: Day 2</h3> 

10.20.22

-------

<h5>Basic Level</h5>

1. Write a program that takes two integers A and B as input and outputs <b style="color:blue;">A/B</b>

   *첫째 줄에 A/B를 출력한다. 실제 정답과 출력값의 절대오차 또는 상대오차가 10-9 이하이면 정답이다.

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a,b;
        a = sc.nextInt();
        b = sc.nextInt();
        System.out.println((double)a/(double)b);
    }
}

```



2. Given two integers A and B, write a program that outputs A+B, A-B, A*B, A/B (quotient), and A%B (remainder). Outputs A+B on the first line, A-B on the second line, A*B on the third line, A/B on the fourth line, and A%B on the fifth line.

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a, b;
        a = sc.nextInt();
        b = sc.nextInt();
        System.out.println(a+b);
        System.out.println(a-b);
        System.out.println(a*b);
        System.out.println(a/b);
        System.out.println(a%b);
    }
}
```





3. Junha was surprised to see that the ID joonas already existed while signing up for the site. Junha expresses surprise with ??! Write a program that expresses surprise when given an ID that already exists on the site that Junha wants to join. Print Junha's surprise on the first line. Surprise is indicated by adding ??! after the ID.

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String id;
        id = sc.next();
        System.out.println(id + "??!");
        
    }
}

```



<h5>Thoughts</h5>

- 응용이 가능한지?

