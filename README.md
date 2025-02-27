`<img width="440" alt="image" src="https://github.com/user-attachments/assets/b30e2b2f-1462-4757-ab0e-1d9dcc502eb7" />

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
- 결론: C# + C# Dev Kit + .NET SDK + Visual Studio Code = 개발환경 세팅 끝

<br>

## appsettings.json
- DB 커넥션 정보 및 비밀번호 같은 것들 세팅할 경우 사용(application.properties라 보면 됨), 민감 정보들을 전역적으로 설정 가능

<br>

## 공통 레이아웃(Microsoft 표준 레이아웃 _Layout)
- ASP.NET.Core MVC 프로젝트 생성 시 내부적으로 레이아웃 파일이 생성됨
- 해당 파일은 Microsoft 표준 레이아웃 파일임
- 이름은 기본적으로 Microsoft에서 _ViewStart.cshtml 파일에서 @{Layout = "_Layout"}으로 정의함으로써 cshtml 파일명이 _Layout이면 공통 레이아웃 파일이라고 설정
- 해당 _Layout.cshtml 파일에서 공통 레이아웃 정의하면 됨
- 스프링 부트는 오픈소스로서 레이아웃을 JSP, Thymeleaf와 같은 여러 템플릿 엔진을 사용해서 정의할 수 있지만, ASP.NET은 Microsoft가 미리 정의해놨고 편하게 해당 틀 내에서 사용자가 레이아웃을 커스터마이징 할 수 있음
- 레이아웃은 헤더 및 푸터로 잘 구현되어있음 ㅇㅇ 손 안대도 됨 이 위에서 갈아끼우기만 하면 될듯
- 레이아웃에는 ```@ViewData[키]```로 정의돼있는데 사용자 cshtml 파일에서 해당 값에 각 사용자마자 차별화된 값을 매겨서 할당할 수 있음 예를 들어 ```<title>@ViewData["title"] Page</title>```라고 _Layout 파일에서 지정해놨으면 각 사용자 파일에선 @{ViewData["Title"] = "Hello"}라고 한다면 최종 해당 페이지 랜더링 시에는 Hello Page 형태가 됨

## Razor Syntax
### 개요
- JSP에서는 HTML 파일 내에서 자바 코딩이 가능하듯 C#도 HTML 파일 내에서 C# 코딩이 가능하다
- Razor Syntax를 통해 가능
- ```@{}``` 영역 안에서 사용 가능
- C# 코드 전부 다 사용이 가능한 게 아닌 제한적으로 사용 가능
- if, for, foreach, 타입 컨버팅(string -> int), ToString()
- 즉 html에서 C# 코드 사용하려면 Razor Syntax인 @를 사용해야됨

### 활용 1) 변수 선언
```cs
@{
  var age="20";
}
```
- 위와 같이 ```@{}``` 영역 내에서 자유롭게 C# 코드 작성 가능

### 활용 2) 변수 호출
```<h1>나이는 @age세 입니다</h1>```

### 활용 3) for문 및 if문
```cs
@if(@name=="레인보우 푸쉬업바"){
    <h2>푸쉬업바가 맛있어요</h2>    
}
else{
    <h2>별로 맛없어요</h2>    
}

@for(int i=0;i<5;i++){
    <h2>최고최고</h2>    
}
```

<br>

## Controller에서 View로 Model 넘기는 3가지 방법
- 컨트롤러에서 ```return View()```를 통해 전달 가능
- 이때 View() 메서드에 어떤 파라메터를 지정하느냐에 따라 3가지 방법으로 나뉨(1. 직접 객체 전달 2. ViewBag 전달 3. ViewData 전달)

### 1. 직접 객체 전달
```cs
User user = new User(1 , "kim");
return View(user)
```



### 2. ViewBag 전달


### 3. ViewData 전달



