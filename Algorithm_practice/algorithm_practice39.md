<h3>Algorithm Practice: Day 30, 31, 32, 33, 34, 35, 36, 37, 38, 39</h3> 

11.29.22 , 11.30.22, 12.01.22, 12.02.22, 12.05.22, 12.06.22, 12.07.22, 12.08.22, 12.09.22, 12.13.22                                   																														

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





2884번: 알람시계

```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
    public static void main(String[] args) throws IOException {
        //BufferedReader로 입력받기, 시는 h 분은 m
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String[] time = br.readLine().split(" ");
        int h = Integer.parseInt(time[0]);
        int m = Integer.parseInt(time[1]);
          
        
        // 분이 44 이하일 경우, 시는 -1 변동된다. ex) 12:44 -> 11:59
        if(m<45){
            // 시가 0일때 24로 변경후 시를 -1 변동시킨다.
            if(h==0){
                h = 24 - 1;
            }else{
                h = h - 1;
            }
            m = (m + 60) - 45;
        // 분이 45 이상일 경우, 시는 변동되지 않는다. ex) 12:45 -> 12:00
        }else{
            m = m -45;
        }
        System.out.println(h);
        System.out.println(m);
    }
}
```

* BufferedReader를 사용할때에는 입력(Input) 형태를 잘 확인해야 한다.

  ```java
  1
  2
  ```

  와

  ```java
  1 2
  ```

  는 다르다. 해당 문제는 후자를 input 형태로 하고 있음. 즉, split을 이용하여 공백단위로 입력을 나누어 변수에 담아야함



2525번: 오븐시계

```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String[] currentTime = br.readLine().split(" ");
        int h = Integer.parseInt(currentTime[0]);
        int m = Integer.parseInt(currentTime[1]);
        
        int minutes = Integer.parseInt(br.readLine());
        
        int time = m + minutes;
        
        if(time >= 60) {
            h = h + (time/60);
            if(h >= 24) {
                h = h - 24;
            }else {
                h = h;
            }
            m = time%60;
        }else {
            h = h;
            m = time;
        }
        System.out.println(h + " " + m);
    }
}
```



2480번: 주사위 3개

```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.lang.Math;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String[] cube = br.readLine().split(" ");
        int a = Integer.parseInt(cube[0]);
        int b = Integer.parseInt(cube[1]);
        int c = Integer.parseInt(cube[2]);
        
        int result = 0;
        
        // 3개가 모두 같을 때 a == b == c 10,000+(같은눈x1,000)
        if(a == b && b == c){
            result = 10000+(a*1000);
        
        // 같은 눈이 두개 일때 1,000+(같은눈x100)
        }else if(a == b | a == c | b == c) {
            if(a == b){
                result = 1000+(a*100);
            }else if(a == c){
                result = 1000+(c*100);
            }else{
                result = 1000+(b*100);
            }
        // 모두 다른 눈일 때 가장큰눈x100 Math.max 활용    
        }else{
            result = Math.max(Math.max(a,b),c)*100;
        }
        System.out.println(result);
    }
}
```

- Math.max( ) 는 두개의 파라미터만을 받을 수 있기 때문에 본 문제에서는 Math.max( )안에서 한번 더 함수를 사용했다.



<반복문>

8393번: 합

```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int number = 0;
        for(int i = 1; i <=n ; i++) {
            number += i ;
        }
        System.out.println(number);
    }
}
```

- ``x += y``  는 ``x = x + y``와 같다.



25304번: 영수증

```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int N = Integer.parseInt(br.readLine());
        int X = Integer.parseInt(br.readLine());
        int totalCost = 0;

        for(int i = 0; i < X; i++) {
            String[] receipt = br.readLine().split(" ");
            int price = Integer.parseInt(receipt[0]);
            int count = Integer.parseInt(receipt[1]);
            totalCost += price * count; 
        }
        if(totalCost == N){
            System.out.println("Yes");
        }else {
            System.out.println("No");
        } 
    }
}
```



15552번: 빠른 A+B

```java
import java.io.IOException;
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
        int T = Integer.parseInt(br.readLine());
        for(int i = 0; i < T; i++ ) {
            String[] numbers = br.readLine().split(" ");
            int a = Integer.parseInt(numbers[0]);
            int b = Integer.parseInt(numbers[1]);
            int total = a+b;
            bw.write(total + "\n");
        }
        bw.flush();
    }
}
```

- StringTokenizer vs String.split()