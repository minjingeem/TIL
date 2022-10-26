<h3>Algorithm Practice: Day 5</h3> 

10.26.22

-------

<h5>Basic Level</h5>

1. (세 자리 수) × (세 자리 수)는 다음과 같은 과정을 통하여 이루어진다.

   ![img](https://www.acmicpc.net/upload/images/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png)

   (1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램을 작성하시오.

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
      Scanner sc = new Scanner(System.in);
      int num1 = sc.nextInt();
      int[] num2 = sc.nextInt();
      
      int[] num3 = num1*num2[2];
      
      int[] num4 = new int[4];
      int[] num4 = num1*num2[1];
      
      int[] num5 = new int[5];
      int[] num5 = num1*num2[0];
      
      System.out.println(num3);
      System.out.println(num4);
      System.out.println(num5);
      System.out.println(parseInt(num3)+ parseInt(num4)+ parseInt(num5));

    }
}
```



<h5>Thoughts</h5>

- 못품

