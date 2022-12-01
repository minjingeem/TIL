~~~객체
Scanner name = new Scanner(System.in);
Calendar now = Calendar.getInstance();
Math.random(); //static은 객체를 만들 필요가 없다.

~~~



메소드 : 기능 구현

생성자 메소드 (constructor summary 참고): new 





### 상속 inheritance

- Parent(상위) and Child(하위)

- child class는 parent class data에 모두 접근가능.

  - Ex) Object <- A <- B <- C

    ~~~상속
    B y = new C();
    A t = new B();
    Object z = new C();
    object u = new B();
    ~~~

- 반대로 parent class는 child class data에 접근이 불가능하다. 

  - Ex) Object <- A <- B <- C

    ~~~상속
    C w = new A(); //불가능
    ~~~

    

- 상위에서 하위로 접근할때에는 typecasting을 사용해야한다.
- 상속관계에서 생엉자 메소드는 parent(상위) class가 먼저 실행된다.

- extends를 사용하여 상속 받는다

  ~~~extends
  publc class Child extends Parent {
  }
  ~~~

  

- 모든 클래스의 최상위 클래스는 object

``super`` : 상위클래스 지칭



### 접근제한자

``public``  >  ``protected``  > ``default``   > ``private``



public: 

protected : 같은 패키지끼리 가능하나  패키지가 다를 경우에는 상속받아 사용할 수 있음.

default: 같은 패키지끼리만 가능.

private: 멤버변수에서 자주 사용됨. 



### 추상클래스 abstract

- 추상클래스 -> 추상메소드 포함 -> 반환형과 메소드명은 존재하나 실행부가 없는 메소드
- 상속받아 추상메소드 오버라이딩



### interface

- 추상메소드들 + static final 변수



### overloading

- 메소드명은 같고, 매개변수의 수나 데이터형이 달라야한다.



*Dependence Injection (DI)



### 예외(Exceptions)처리

- 프로그램 코드로 처리 할 수 있는 것을 Exceptions, 처리 할 수 없는 것은 Errors



> 예외처리방법 1
>
> ~~~예외처리방법1
> 	try{
> 		예외가 발생할 가능성이 있는 코드
> 	
> 	}catch(예외종류){
> 		예외가 발생했을때 처리하는 곳
> 	}
> 	-->
> 	:
> 	:
> 	}finally {//예외가 발생하든 안하든 무조건 실행됨
> }
> ~~~
>
> 
>
> 예외처리방법 2
>
> ~~~예외처리방법 2
> ~~~
>
> 
>
> 예외처리방법 3
>
> ~~~예외처리방법3
> ~~~
>
> 



### wrapper class

- class는 다 object이다.



### Format

