# JAVA 기초 : Methods

> JAVA 프로그래밍의 기초를 알아보아요. 이번 편은 Methods에 대해서 알아봅니다.

** w3schools JAVA 자료를 번역하고 참고하였습니다.*



## 1. Java Methods란?

<aside> ✅ - ***method는 호출 되었을 때에만 실행되는 코드 블럭입니다.

- 매개변수(parameters)를 이용해 데이터를 method에 넘겨 줄 수도 있습니다.
- method는 특정 액션을 취할 수 있고, functions라고 불리기도 합니다.***

Q: 왜 메소드를 사용하나요? A: 코드를 재사용하기 위해. 코드를 한번 정의하고, 여러번 사용하기 위해.

</aside>

1-1. **Method 생성하는 방법**

- 메소드는 반드시 class 내부에 정의 되어야 합니다.
- 메소드는 `메소드 이름` ****뒤에 괄호 `( )`가 따라오는 형식으로 정의 됩니다.
- Java는 이미 지정된 메소드를 제공하기도 하는데 `System.out.println()`이 그 예시입니다.
- 우리는 언제나 우리만의 메소드를 생성할수 있습니다.

예시) Main 내에 메소드 생성

```java
public class Main {
	static void myMethod() {
		// 실행될 코드
	}
}
```

1-2. **Method 호출하기**

- 메소드를 호출하려면 `메소드이름` 뒤에 괄호`( )` 그리고 세미콜론 `;`을 붙여줍니다.
- 메소드는 여려번 호출 할 수 있습니다.

예시) main 안에서 myMethod()라는 메소드를 호출

```java
public class Main {
	static void myMethod(){
		System.out.println("조금 전에 호출되었어요!");
	}
		public static void main(String[] args) {
			myMehtod();
	}
}

// "조금 전에 호출되었어요!" 출력
```

## 2. JAVA Method Parameters

2-1. **Parameter 와 Argument**

<aside> ✅ ***- 정보는 메소드를 통과할 수 있는데, 매개변수로서 통과한다. 매개변수는 메소드 내에서 변수의 역할을 합니다.

- 매개변수는 `메소드이름` 다음의 괄호`( )` 안에서 지정 됩니다.
- 여러 매개변수를 지정 할 수도 있고 `,` 로 구분 짓습니다.***

</aside>

매개변수(parameter)는 **데이터타입**과 **데이터이름**(원하는 이름)으로 지정합니다.

ex) myMethod(String **name**)

→ 데이터타입은 ****String이고 데이터의이름은 **name**

예시) **name**이라는 `String`을 매개변수로한 메소드

```java
public class Main {
	static void myMethod(String name){
		System.out.println(name + "Geem");
	}
		public static void main(String[] args) {
			myMehtod("Minjin");
			myMehtod("MaryJane");
			myMehtod("MJ");
	}
}
// Minjin Geem
// MaryJane Geem
// MJ Geem
```

- 위의 예시에서, `name`은 `myMethod` 메소드가 전달 받을 수 있는 String 데이터 타입의 **parameter** 입니다.
- 실제로 `myMethod` 메소드에 전달되는 값인 `Minjin`, `MaryJane`, `MJ` 는 **argument**입니다.

<aside> 💡 알아두기!

매개변수 / **parameter** : 메소드가 전달 받을 수 있는 데이터의 종류.

전달인자 / **argument** : 메소드에 전달되는 것. (메소드에 전달 되는 실제 값)

</aside>

2-2. **Multiple Parameters**

- 원하는 만큼의 매개변수(parameter)를 가질 수 있습니다.

예시)

```java
public class Main {
	static void myMethod(String name){
		System.out.println(name + "is" + age);
	}
		public static void main(String[] args) {
			myMehtod("John", 15);
			myMehtod("Erik", 15);
			myMehtod("Woo", 14);
			myMehtod("Sun", 15);
	}
}
// John is 15
// Erik is 15
// Woo is 14
// Sun is 15
```

2-3. **Return Values**

<aside> ✅ ***- `void` 키워드는 메소드가 어떤 value도 리턴하지 않아야 함을 명시합니다.

- 만약 메소드가 어떠한 value를 리턴하게 하고 싶다면, 기본 데이터 타입(`int`, `char`, 등)을 `void` 대신 사용하면 됩니다. 그리고 `return` 키워드를 메소드에 사용하면 됩니다.***

</aside>

예시)

```java
// 1개 parameter 일때
public class Main {
	static int myMethod(int x){
		return 5 + x;
	}
		public static void main(String[] args) {
			System.out.println(myMethods(3));
	}
}

// 2개 parameter 일때

public class Main {
	static int myMethod(int x, int y){
		return x + y;
	}
		public static void main(String[] args) {
			System.out.println(myMethods(5,3));
	}
}

// 둘다 8을 출력한다.
```

- 결과를 변수에 담을 수도 있습니다. (코드 유지와 가독성에 용이함으로 권장)

  예시)

  ```java
  public class Main {
  	static int myMethod(int x){
  		return 5 + x;
  	}
  		public static void main(String[] args) {
  			int z = myMethod(5,3);
  			System.out.println(z);
  	}
  }
  ```

2-4. **A Method wit If…Else**

- `if…else` 구문은 메소드 안에서 자주 사용됩니다.

예시)

```java
public class Main {
	static void checkAge(int age){
		if(age < 18) {
			System.out.println("엑세스가 거부 되었습니다 - 너무 어려요!");
		} else {
			System.out.println("엑세스가 허용 되었습니다 - 너무 어리지 않군요!");
		}
	}
	public static void main(String[] args) {
		checkAge(20);
	}
}

// 엑세스가 허용 되었습니다 - 너무 어리지 않군요! 출력
```

## 3. Method Overloading

<aside> ✅ ***메소드 오버로딩을 하면 여러 메서드가 매개변수가 다른, 동일한 이름을 가질 수 있습니다.***

</aside>

예시 1)

```java
static int plusMethodInt(int x, int y) {
  return x + y;
}

static double plusMethodDouble(double x, double y) {
  return x + y;
}

public static void main(String[] args) {
  int myNum1 = plusMethodInt(8, 5);
  double myNum2 = plusMethodDouble(4.3, 6.26);
  System.out.println("int: " + myNum1);
  System.out.println("double: " + myNum2);
}
```

예시 2) 동일한 작업을 수행해야 하는 두개의 메서드를 정의하는 것보다 overload하는 것이 좋다. 아래 예에서는 `int`와 `double` 모두에 작동하도록 `plusMethod` 메서드를 overload한다.

```java
static int plusMethod(int x, int y) {
  return x + y;
}

static double plusMethod(double x, double y) {
  return x + y;
}

public static void main(String[] args) {
  int myNum1 = plusMethod(8, 5);
  double myNum2 = plusMethod(4.3, 6.26);
  System.out.println("int: " + myNum1);
  System.out.println("double: " + myNum2);
}
```

## 4. Java Scope

<aside> ✅ ***java에서 변수는 변수가 생성된 영역 내에서만 접근 할 수 있습니다. → scope***

</aside>

- Method Scope

  - 메서드 내에서 직접 선언된 변수는 변수가 선언된 코드 줄 다음부터 메서드의 모든 위치에서 사용할 수 있습니다.

  예시)

  ```java
  public class Main {
    public static void main(String[] args) {
  
      // 변수가 아직 선언 되기 전 임으로, 변수 x를 사용할 수 없음
  
      int x = 100;
  
      // 이곳의 코드는 변수 x 사용가능.
      System.out.println(x);
    }
  }
  ```

- Block Scope

  - 코드 블럭은 `{ }` 안에 있는 코드를 의미합니다.
  - 코드 블럭 내에서 선언된 변수는 `{ }` 안에서만 접근 할 수 있고, 변수가 선언된 줄 다음에 나오는 코드에서만 접근이 가능합니다.

  ```java
  public class Main {
    public static void main(String[] args) {
  
      // 변수x는 블럭 내에 있음으로 변수x를 사용 할 수 없음.
  
      { // 블럭
  
        // 변수 x가 아직 선언되지 않았기 때문에 이곳 코드에는 변수 x를 사용할 수 없다.
  
        int x = 100;
  
        // 이 라인의 코드에는 변수 x 사용 가능.
        System.out.println(x);
  
      } // 블럭 끝
  
    // Code here CANNOT use x
  
    }
  }
  ```

  <aside> 💡 알아두기!

  코드블럭은 자체적으로 존재하거나 `if` , `while` or `for`문에 속할 수 있습니다. `for` 문의 경우 statement에 선언된 변수를 블록 범위 내에서 사용 할 수 있습니다.

  </aside>