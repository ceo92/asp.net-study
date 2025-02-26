<img width="440" alt="image" src="https://github.com/user-attachments/assets/b30e2b2f-1462-4757-ab0e-1d9dcc502eb7" />

<br>

## ASP.NET이란?
-  웹 애플리케이션을 제작할 때 사용하는 기술
- HTML CSS JS Vue JS React는 클라이언트 개발 언어, Java ,Spring, ASP.NET은 서버 개발 언어
- ASP.NET은 C#을 통해 개발
- ASP.NET은 C#의 프레임워크임 애플리케이션을 더 빠르게 개발 및 유지보수 가능
- 개발도구: Visual Studio, DB: MS SQL
- Mac은 Visual Studio를 2024년 8월 31일자로 종료했으므로 Visual Studio Code 혹은 Rider 사용해야됨

<br>

## ★ ASP.NET MVC
- 초기에는 Web Form을 통해 ASP.NET을 개발
- 하지만 Web Form은 HTML 코드 내에 ASP.NET 관련 소스코드들이 겹치게되어 추후 유지보수가 힘듬
- UI를 담당하는 HTML에서 ASP.NET 관련 C# 소스코드가 혼합되니 유지보수가 힘들고 코드가 지저분해짐, 대용량 프로젝트일 경우 더 혼잡 우려
- 그에 따라 객치제향적이지 못해서 SOLID 원칙에도 위배
- 자바에서 서블릿으로만 개발하면 자바 코드에 HTML 첨가되고 JSP로만 개발하면 HTML에 자바 코드 첨가되니 유지보수하기 까다로움, 한 클래스가 여러 책임 지게되므로 SRP 위배
- 그에 따라 ASP.NET MVC 등장하며 UI 영역과 코드 영역 분리할 수 있게 됨, Controller에서 요청 및 응답 처리하고 Model에 데이터를 넣어서 View에 전달하면 View에선 UI 담당하고 Controller로부터 넘어온 Model을 통해 동적 랜더링 가능
- Spring도 강력한 MVC가 있음에 따라 구시대적인 Web Form을 하는 것보단 ASP.NET MVC가 좋음

<br>

## ★ Web API(REST API)
- 웹 애플리케이션 상에서 HTTP 응답 방식은 1. MVC 방식 및 2. API 방식이 존재하는데 1. MVC방식이 ASP.NET MVC이고 2. API 방식이 Web API 즉 REST API 통신!
- 둘의 차이는 MVC는 컨트롤러에서 모델 넘겨서 뷰에서 SSR을 통해 화면에 랜더링되는 것이고 API 방식은 상대방에게 데이터를 전달하는 개념임, **즉 화면을 설계하고 싶으면 MVC, 데이터를 전달하고싶으면 API**
- API 방식은 JSON 형식의 데이터로 통신하므로 어떤 플랫폼이든 구애받지 않고 통신 가능, IOS, Android와 통신 가능, 자바 스프링과 ajax를 통해 통신 가능!

<br>

## ASP.NET(닷넷 프레임워크) VS ASP.NET Core(닷넷 코어)
- ASP.NET: 윈도우 서버에서만 개발 가능, Full dot net, System.Net.XXXX
- ASP.NET Core은 크로스 플랫폼 지원함에 따라 모든 OS 구애받지 않고 개발 가능, System.Net.XXXX 삭제해서 퍼포먼스적으로 빨라짐 응답 속도 면에서 우수

<br>

## Blazor
- 프론트를 C#으로도 개발 가능, 즉 Blazor을 통해 Front-end 및 Back-end 풀스택 개발 가능

<br>

## 프로젝트 생성(for Mac)
https://learn.microsoft.com/ko-kr/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-10.0&tabs=visual-studio-code <= 참고(공식 사이트)
1. 비쥬얼 스튜디오 코드 설치
2. 비쥬얼 스튜디오 내에서 C# 개발 키트 설치
3. 마이크로소프트 계정 연결 및 개발할 프로젝트 폴더 지정
4. .NET SDK 설치(Java의 JDK와 같은) 후 껐다 켜야됨(껐다 켜야 비쥬얼 스튜디오 코드와 SDK 연동)
5. .NET Core 웹앱 MVC(Model View Controller) 프로젝트 생성(웹앱 API가 아닌 웹앱 MVC 선택하기, 어차피 MVC 안에 API가 들어가있어서 MVC 프로젝트에서 API 통신 가능)
<img width="961" alt="image" src="https://github.com/user-attachments/assets/1756426b-4dfb-45cd-847b-35cee562602d" />

사진과 같이 웹앱이 아닌 웹앱 MVC(Model View Controller)을 선택해야됨
- ※ dotnet 명령은 iTerms와 같은 터미널이 아닌 비쥬얼 스튜디오 코드 내 터미널에서만 가능
- ※ Command + Shift + P를 통해 프로젝트 생성 가능
- ```dotnet new mvc -o [MVC 프로젝트 명]``` 콘솔에서 해당 명령을 통해 닷넷 MVC 프로젝트 생성 가능
