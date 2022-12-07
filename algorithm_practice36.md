<h3>Algorithm Practice: Day 30, 31, 32, 33, 34, 35, 36</h3> 

11.29.22 , 11.30.22, 12.01.22, 12.02.22, 12.05.22, 12.06.22, 12.07.22                                    																														

-------

입출력과 사칙연산, 조건문, 반복문 복습



```java
import java.util.*;

public class Q2557 {
  public static void main(String[] args) {
    System.out.println("Hello World!");
  }
}

```



```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
      
        //StringTokenizer st = new StringTokenizer(br.readLine()," ");
      	String str = br.readLine();
      	StringTokenizer st = new StringTokenizer(str, " ")// 객체 생성 할 때 StringTokenizer( "문자열" , 구분자 )
      	
        
        int A = Integer.parseInt(st.nextToken());
        int B = Integer.parseInt(st.nextToken());
        
        System.out.println(A+B);
    }
}
```

https://www.webucator.com/article/how-to-use-systemin-in-java/

- <i><b>System.in</b></i> 
  - 키보드에서 Input Stream을 제공한다 -> 키보드로부터 오는 데이터를 input받을 수 있는 Stream을 만든다.
  - System이라는 class안에 in이라는 attribute(variable)
- <i><b>InputStreamReader</b></i>
  - 키보드로부터 오는 데이터 Stream을 읽는다.
- <i><b>BufferedReader</b></i>
  - BufferedReader 객체는 input을 버퍼에 담는다





Method는 Class 안에 선언된 함수

Attributes는 Class 안에 선언된 변수



```java
import java.util.*;

public class Main {
  public static void main(String[] args){
    System.out.println("\\    /\\");
    System.out.println( )  ( '));
    System.out.println((  /  ));
    System.out.println( \\(__)|);
  }
}
```





```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main{
    public static void main(String args[]) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String[] str = br.readLine().split(" ");
        
        int A = Integer.parseInt(str[0]);
        int B = Integer.parseInt(str[1]);
        
        if(A > B){
            System.out.println(">");
        }else if(A < B){
            System.out.println("<");
        }else{
            System.out.println("==");
        }
    }
}
```



```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
    public static void main(String[] args) throws IOException{
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int year = Integer.parseInt(br.readLine());
        
        if(year%4 == 0 ) {
            if(year%100 != 0 | year%400 == 0){
                System.out.println(1);
            }else{
                System.out.println(0);
            }
        }else {
            System.out.println(0);
        }
    }
}
```



```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
    public static void main(String[] args) throws IOException{
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
  
        int x = Integer.parseInt(br.readLine());
        int y = Integer.parseInt(br.readLine());
        
        if(x>0 && y>0){
            System.out.println(1);
        }else if(x<0 && y>0){
            System.out.println(2);
        }else if(x<0 && y<0){
            System.out.println(3);
        }else{
            System.out.println(4);
        }
    }
}
```

