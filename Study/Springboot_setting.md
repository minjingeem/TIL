## Springboot 맥



1. spring.io/tools 접속 후 tool 다운.

![Screen Shot 2022-07-28 at 9.47.26](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 9.47.26.png)



2. applications로 drag 해준다. 

![Screen Shot 2022-07-28 at 9.48.54](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 9.48.54.png)

3. SpringToolSuite4 오픈 후 workspace 설정

![Screen Shot 2022-07-28 at 10.07.07](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.07.07.png)





4. Spring boot 프로젝트 시작하기 

![Screen Shot 2022-07-28 at 10.11.53](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.11.53.png)



4-1 프로젝트 제목 설정 및 형식, 배포방식 등 설정 

 * 참고: 스프링부트에서  JSP를 사용하려면 War 프로젝트로 만들어야함. War 프로젝트 생성시 SpringBootServletInitializer를 상속받는 ServletInitializer 클래스 파일이 생성된다. War 파일로 배포하는 경우에, 이를 상속받아 배포한다.

 * 스프링 웹 애플리케이션이 Tomcat에서 동작되기 위해서는 Web.xml에 ApplicationContext 등록해줘야한다.
   Apache Tomcat이 구동될때 web.xml을 읽어 웹 애플리케이션을 구성하기 때문이다.

   Servlet 3.0으로 스펙이 업데이트 되면서 web.xml 설정을 WebApplicationInitializer 인터페이스를 구현하여 대신 할 수 있게 되었고 이를 구현한 SpringBootServletInitializer를 상속받아 외부 Tomcat에서 스프링부트가 실행되도록 해준다.

   SpringBootServletInitializer를 상속 받는 다는 것은 tomcat 같은 Servlet Container 환경에서Spring Boot 애플리케이션 동작 가능 하도록 웹 애플리케이션 컨텍스트를 구성한다는 의미.

![Screen Shot 2022-07-28 at 10.16.16](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.16.16.png)



4-2 dependencies에 framework 추가 후 완료.

![Screen Shot 2022-07-28 at 10.21.14](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.21.14.png)



5. 파일 생성

 ![Screen Shot 2022-07-28 at 10.31.58](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.31.58.png)



6. build.gradle에 프레임워크추가

![Screen Shot 2022-07-28 at 10.40.28](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.40.28.png)



아래의 3가지 프레임워크(Tomcat Jasper, jstl, Javax Inject)를 추가하면 된다 .

 - Tomacat Jasper>> 9.0.58

   https://mvnrepository.com/artifact/org.apache.tomcat/tomcat-jasper/9.0.58  (프레임워크 코드를 받을 수 있는 주소)

   - // https://mvnrepository.com/artifact/org.apache.tomcat/tomcat-jasper
     implementation 'org.apache.tomcat:tomcat-jasper:9.0.58'

     (또는, 위를 복사 붙여넣기)

 - JSTL>>1.2

   https://mvnrepository.com/artifact/javax.servlet/jstl/1.2

   - // https://mvnrepository.com/artifact/javax.servlet/jstl
     implementation 'javax.servlet:jstl:1.2'

 - javax>>1

   https://mvnrepository.com/artifact/javax.inject/javax.inject/1

   - // https://mvnrepository.com/artifact/javax.inject/javax.inject
     implementation 'javax.inject:javax.inject:1'





7. refresh 꼭 해주기 !

![Screen Shot 2022-07-28 at 10.41.58](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.41.58.png)



8.  application.properties는 스프링부트에서 사용하는 서비스포트번호라던가, DB접속정보, 외부프로그램 사용정보등을 기록하는 곳인데 통상 yml을 많이 쓰는 추세이다. 바꾸는것은 간단하다. application.properties를 삭제하고, application.yml 파일로 교체한다.



![Screen Shot 2022-07-28 at 11.11.59](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 11.11.59.png)



![Screen Shot 2022-07-28 at 10.49.03](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 10.49.03.png)



10. Help > Eclipse Marketplace

![Screen Shot 2022-07-28 at 11.16.24](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 11.16.24.png)



11. web developer를 검색하고 Eclipse Enterprise Java and Web Developer Tools 3.26 다운 

![Screen Shot 2022-07-28 at 11.17.50](/Users/minjinkim/Desktop/Screen Shot/Screen Shot 2022-07-28 at 11.17.50.png)



