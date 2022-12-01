# MVC Pattern Architecture



SpringBoot에서 사용되는 MVC Pattern을 알아보자.









### MVC 패턴 기본구조

------------------------



![Untitled presentation (1)](/Users/minjinkim/Downloads/Untitled presentation (1).png)



### controller 이해하기

-----------------------



우선 controller의 역할을 이해하기 위해 간단한 실습을 해 본다.



1. Src/main/java에 test를 위한 controller 패키지를 만들고, TestController 클래스를 생성한다.

<img src="/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-08-22 at 21.10.11.png" alt="Screen Shot 2022-08-22 at 21.10.11" style="zoom: 50%;" />



2. TestController.java에 아래와 같이 ex1 메소드를 생성한다. 

<img src="/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-08-22 at 21.11.49.png" alt="Screen Shot 2022-08-22 at 21.11.49" style="zoom:50%;" />



```ex1
@Controller
@RequestMapping("/test") 
public class TestController {

	@GetMapping("/ex1") // "/ex1"라는 url 주소와 메소드를 mapping 한다. 즉, ex1 이라는 url 주소로 들어오면 매핑된 메소드가 실행됨.
	public void ex() { 
		System.out.println("ex1 메소드 실행됨....");
	}
}
```



3. 스프링부트 프로젝트를 실행하고, 주소창에 <b> localhost:####/test/ex1</b> 을 입력하면 아래와 같은 창이 뜬다. 

   <b>JSP file not found</b> 라는 에러 메세지를 확일 할 수 있다.(*뷰파일이 없다는 의미)

   

   <img src="/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-08-22 at 21.13.10.png" alt="Screen Shot 2022-08-22 at 21.13.10" style="zoom:67%;" />

   4. 스프링부트 콘솔을 확인해보면, ex1 메소드가 정상 출력되어있는 것을 확인 할 수 있다.



<img src="/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-08-22 at 21.12.32.png" alt="Screen Shot 2022-08-22 at 21.12.32" style="zoom: 50%;" />





* Controller는 클라이언트가 uri 요청을 하면, 그 요청을 받고 해당 uri가 mapping된 메소드를 실행한다.
* 해당 실습에는 클라이언트에게 보내줄 뷰페이지가 없음으로 404오류가 뜬다.



![Screen Shot 2022-08-22 at 21.39.07](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-08-22 at 21.39.07.png)







### Views 이해하기

--------------------

1. Test 프로젝트의 src > main 폴더에 webapp > WEB-INF > views 폴더를 생성하고 <b>ex1.jsp</b> , <b>ex2.jsp</b> 파일 생성

<img src="../../Desktop/Screen Shot/Screen Shot 2022-08-22 at 23.49.56.png" alt="Screen Shot 2022-08-22 at 23.49.56" style="zoom:50%;" />





2. 생성된 각 jsp 파일에 파일명을 표기해준다. (뷰화면 확인용으로)

![Screen Shot 2022-08-22 at 23.51.41](../../Desktop/Screen Shot/Screen Shot 2022-08-22 at 23.51.41.png)





3. TestController에 <b>ex2</b>, <b>ex3</b> 메소드를 생성해준다. (String, 반환형)

<img src="../../Desktop/Screen Shot/Screen Shot 2022-08-22 at 23.52.47.png" alt="Screen Shot 2022-08-22 at 23.52.47" style="zoom:50%;" />





4. 결과 : 

<img src="../../Desktop/Screen Shot/Screen Shot 2022-08-22 at 23.53.20.png" alt="Screen Shot 2022-08-22 at 23.53.20" style="zoom: 50%;" />

<img src="../../Desktop/Screen Shot/Screen Shot 2022-08-22 at 23.53.30.png" alt="Screen Shot 2022-08-22 at 23.53.30" style="zoom:50%;" />



<img src="../../Desktop/Screen Shot/Screen Shot 2022-08-22 at 23.53.40.png" alt="Screen Shot 2022-08-22 at 23.53.40" style="zoom:50%;" />





5. 스프링부트의 콘솔에서 메소드 3개 모두 실행된 것을 확인할 수 있다.

<img src="../../Desktop/Screen Shot/Screen Shot 2022-08-22 at 23.54.09.png" alt="Screen Shot 2022-08-22 at 23.54.09" style="zoom:50%;" />