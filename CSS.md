## CSS 

<link/> 

- 링크를 여러개를 걸 수 있다.



*CSS 는 CSS끼리 폴더 관리





#### <a 태그의 상태에 따른 스타일시트 적용하기>

가상클래스는 변수가 만들어져있음. 

~~~
a:link{	}	//링크상태일때(기본)
a:visited{ } //링크를 방문했을때
a:hover{ } // 마우스오버
a:active{	} // 마우스를 누른 상태일때
~~~

- a에 link가 걸려있으면 {이 안을 실행해라}

  

#### <background 속성>

~~~background
<style>
	body{
		background-color: ; /*rgb코드, 컬러명으로 배경색상설정 */
		background-image:url(파일경로);
		background-repeat: ; /*반복처리 no-repeat, repeat-x, repeat-y */
		background-position: ; /* left, center, right, top, middle, bottom, 백분율 */
		background-attachment: ; /*fixed, scroll*/ 
		
		background-size: ; /*배경이미지 크기 px, % */
		opacity: ; /*투명도 설정 0~1사이*/
	}
</style>
~~~

*background-position 참고

​								top



Left					 center                 right

​                           

​							Bottom



	##### - 속성의 그룹화

~~~그룹화
background:url(../img/01.png) no-repeat 100% 20% fixed 
~~~



#### < Font>

~~~font
<style>
	/*
		폰트 스타일 : font-size, font-family(글꼴), color
		font-size: px(기본:16px), pt, cm. mm, in(inch)
				   em(현재글자크기를 기준으로 사이즈가 정해진다.) 0.5em->10px  1.5em->30px
		font-family: 글꼴
	
	
	*/
	li{
		font-size:1.1em;
		font-family: sans-serif 돋움체 궁서; /*없을때 다음 글씨채 */
		
	}
</style>
~~~

 

#### Border

~~~border
<style>
	/*
		border-style : 선모양(solid:실선, dotted:점선, dashed, double:이중선, none, groove, inset)
			border-lefty-style, border-right-style, border-top-style, border-bottom-style
		border-color: rgb, color
			border-left-color, border-right-color, border-top-color, border-bottom-color
		border-width : 선의 두깨 (px), 보통 1px
			border-left-width, border-right-width, border-top-width, border-bottom-width
	*/
	li{
		margin:50px 10px; /* margin-left, margin-right, margin-top, margin-bottiom */
		padding:10px;
	}
	li{
	/*	
		border-style:solid dotted dashed double;    시계방향으로 돌아감 
		border-width:3px 4px 5px 6px;
		border-color:red green blue yellow; 
		*/	 
		border: solid 5px orange;
		border-bottom-color : green;
	}



</style>
~~~



#### List

~~~list
<style>
	/*
		list-style-type: list 헤더설정 
	
	
	
	*/
	body, ul, li{
		margin:0px; padding:0px;
	}
	ul{
		border: 3px green solid;
	}
	li{list-style-type:none;
		float: right ;/* 좌우로 정렬(left, right)*/
		background:orange;
		width:20%;
		text-align:center;/*내용을 정렬(left, center, right)*/
	
	}
</style>
~~~





#### attribute 속성선택자

- html에 있는 속성들





