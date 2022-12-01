## F/E, B/E Summary

프론트엔드, 백엔드 (html,css,javascript,jquery, ajax, jsp, jstl, spring)



- el 표현식

  - ${   } jstl 

  

- a 태그 

  - <a href="주소" title="구글로가요" target = "_blank">구글.  

  

- Javascript 함수 생성하는 방법 

  - function 함수이름 ( ){

    }

  - 함수명( )=>{

    }

  - var a ( ) =>{

    }

    

- sementic 태그 :

  - Header, footer, nav, section, article , aside, body, thread, foot, main...

  

- 클라이언트측과 서버측에 정보를 저장할 수 있는 내장객체 

  - cookie, session

  

- jquery 표기법 

  - $(document).ready(function( ){ 

    });

  - jquery(document).ready(function( ){ 

    });

  - $(function( ){ 

    })

  - $(( )=>{

    });

    

- css 포지션 

  - **position 원하는 위치에 요소를 배치할때 사용되는 속성**

    **- static : 기본적으로 생성되는 위치(디폴트) 다른요소와 겹치지 않게 배치.**

    **- relative : 기본위치에서 이동을 시킬때 사용되는 값**. 원래위치를 기준으로 계산.

    **- absolute : 절대위치를 기준으로 이동시킬때 사용되는 값**

    **- fixed : 고정값. 브라우저 화면을 기준으로 고정 위치에 배치**

    

    

- css 선택자 

  - #A>div:nth-chid(2)...

    

- Controller 

  - 서버로 데이터를 가져온다 request
  - 뷰페이지 정보 제공 
  - 서버에서 클라이언트로 정보보내기 (실제로는 dao에서 db 작업 )

  

- 유효성검사 

  - 아이디가 있나 없나? 

  - If($("#userid").val()=="") {

    alert("아이디를 입력하세요");

    $("#userid").focus()

    return false; 

    }

  - If(document.getElementByid("userid").value.length<8 || document.getElementById("userid").value.length>12){

    alert("아이디를 입력하세요");

    document.getElementByid("userid").value="";

    document.getElementByid

    

- ajax 표기법 

  - $.ajax({

  ​				url : url,

  ​				data : params,

  ​				type : "GET",

  ​				success:**function**(result){

  ​					$("#view").append(result);

  ​				},

  ​				error:**function**(e){

  ​					console.log(e.responseText);

  ​				}

  ​			});

  

- 스피링에서 데이터 받는 대표적인 방법

  - **CASE 1)** **@RequestParam** 

    - URI의 **물음표 뒤 queryString형태**로 파라미터 받음

    

    **CASE 2) @PathVariable** 

    - **/로 구분된 URL 경로**를 통해 파라미터 받음

      

- 로그인하기(백엔드)

  - // public ____ loginOk(String userid, String userpwd) {

    ​	public ModelAndView loginOk(MemberVO vo, HttpSession session) { 

    // vo 를 매개변수로 사용하면 보낸 데이터변수와 같은 이름을 가진 변수에 자동으로 request 해준다.

    ​		MemberVO resultVO = service.login(vo);

    ​		

    ​		// 아이디, 비밀번호가 있으면 아이디와 이름을 vo에 담아서 return

    ​		// 없으면 null 이 return 된다.

    ​		ModelAndView mav = new ModelAndView();

    ​		

    ​		if(resultVO==null) { // 로그인 실패

    ​			mav.setViewName("redirect:login");

    ​		}else { // 로그인 성공

    ​			

    ​			// session 기록

    ​			// HttpSession session = request.getSession();

    ​			session.setAttribute("logId", resultVO.getUserid());

    ​			session.setAttribute("logName", resultVO.getUsername());

    ​			session.setAttribute("logStatus", "Y");

    ​			

    ​			// 페이지 이동

    ​			mav.setViewName("redirect:/");

    ​		}

    ​		return mav;

    

- Mybatis 쿼리문 구현하는 방법 

  - public List <BoardVO> boardList(int a);

    <select id = "boardList" resultType = "com.mulcam.myapp.vo.BoardVO". parameterType="int">
      select no, subject, userid, hit, date_format(writedate, %m-%d %H:%i) writedate
      from board order by no desc
    </select>
    
    

