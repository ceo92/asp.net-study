# asp.net-study
<img width="440" alt="image" src="https://github.com/user-attachments/assets/b30e2b2f-1462-4757-ab0e-1d9dcc502eb7" />

<br>

## ASP.NET이란?
-  웹 애플리케이션을 제작할 때 사용하는 기술
- HTML CSS JS Vue JS React는 클라이언트 개발 언어, Java ,Spring, ASP.NET은 서버 개발 언어
- ASP.NET은 C#을 통해 개발
- ASP.NET은 C#의 프레임워크임 애플리케이션을 더 빠르게 개발 및 유지보수 가능
- 개발도구: Visual Studio, DB: MS SQL
- Mac은 Visual Studio를 2024년 8월 31일자로 종료했으므로 Visual Studio Code 혹은 Rider 사용해야됨

## ASP.NET MVC
- 초기에는 Web Form을 통해 ASP.NET을 개발
- 하지만 Web Form은 HTML 코드 내에 ASP.NET 관련 소스코드들이 겹치게되어 추후 유지보수가 힘듬
- UI를 담당하는 HTML에서 ASP.NET 관련 C# 소스코드가 혼합되니 유지보수가 힘들고 코드가 지저분해짐, 대용량 프로젝트일 경우 더 혼잡 우려
- 그에 따라 객치제향적이지 못해서 SOLID 원칙에도 위배
- 자바에서 서블릿으로만 개발하면 자바 코드에 HTML 첨가되고 JSP로만 개발하면 HTML에 자바 코드 첨가되니 유지보수하기 까다로움, 한 클래스가 여러 책임 지게되므로 SRP 위배
- 그에 따라 ASP.NET MVC 등장하며 UI 영역과 코드 영역 분리할 수 있게 됨, Controller에서 요청 및 응답 처리하고 Model에 데이터를 넣어서 View에 전달하면 View에선 UI 담당하고 Controller로부터 넘어온 Model을 통해 동적 랜더링 가능
- Spring도 강력한 MVC가 있음에 따라 구시대적인 Web Form을 하는 것보단 ASP.NET MVC가 좋음


## Web API(REST API)
- 웹 애플리케이션 상에서 HTTP 응답 방식은 1. MVC 방식 및 2. API 방식이 존재하는데 1. MVC방식이 ASP.NET MVC이고 2. API 방식이 Web API 즉 REST API 통신!
- 둘의 차이는 MVC는 컨트롤러에서 모델 넘겨서 뷰에서 SSR을 통해 화면에 랜더링되는 것이고 API 방식은 상대방에게 데이터를 전달하는 개념임, **즉 화면을 설계하고 싶으면 MVC, 데이터를 전달하고싶으면 API
