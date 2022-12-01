# JAVA 기초

> JAVA 프로그래밍의 기초를 알아보자. ** w3schools JAVA 자료를 번역하고 참고하였습니다.*

## 1. Java Methods

<aside> ✅ - *method는 호출 되었을 때에만 실행되는 코드 블럭이다.

- 매개변수(parameters)를 이용해 데이터를 method에 넘겨 줄 수 있다.
- method는 특정 액션을 취할 수 있고, functions라고 불리기도 한다.*

Q: 왜 메소드를 사용하는가? A: 코드를 재사용하기 위해. 코드를 한번 정의하고, 여러번 사용하기 위해.

</aside>

- **Method 생성하는 방법**

  - 메소드는 반드시 class 내부에 정의 되어야 한다.
  - 메소드는 `메소드 이름` ****뒤에 괄호 `( )`가 따라오는 형식으로 정의 된다.
  - Java는 이미 지정된 메소드를 제공하기도 하는데 `System.out.println()`이 그 예시다.
  - 우리는 언제나 우리만의 메소드를 생성할수 있다.

  예시) Main 내에 메소드 생성

  ```java
  public class Main {
  	static void myMethod() {
  		// 실행될 코드
  	}
  }
  ```

- Method 호출하기

  - 메소드를 호출하려면 `메소드이름` 뒤에 괄호`( )` 그리고 세미콜론 `;`을 붙여준다.
  - 메소드는 여려번 호출 할 수 있다.

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

<aside> ✅ *- 정보는 메소드를 통과할 수 있는데, 매개변수로서 통과한다. 매개변수는 메소드 내에서 변수의 역할을 한다.

- 매개변수는 `메소드이름` 다음의 괄호`( )` 안에서 지정된다. 여러 매개변수를 지정 할 수도 있고 `,` 로 구분 짓는다.*

</aside>

예시) **fname**이라는 `String`을 매개변수로한 메소드

```java
public class Main {
	static void myMethod(String fname){
		System.out.println(fname + "Geem");
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

💡**매개변수(parameter)** 가 메소드에 전달되면 이를 **argument**라고 부른다. 위의 예시에서 `fname`은 **매개변수**고, `Minjin`, `MaryJane`, `MJ` 는 **argumen**t 다.

💡매개변수 parameter는 변수명이라는 의미

💡전달인자 argument는 전달값이라는 의미