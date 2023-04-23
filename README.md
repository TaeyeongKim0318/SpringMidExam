# SpringMidExam
## 1. 스프링 개요
1. 웹프로그래밍에 대한 이해
   1. 정적인 컨텐츠와 동적인 컨텐츠<br>
      ![동적 정적 웹페이지.png](Img/동적%20정적%20웹페이지.png)
      - JSP(Java Server Page)는 HTML 내에 자바 코드를 삽입하여 웹 서버에서 동적으로 웹 페이지를 생성하여 웹 브라우저에게 돌려주는 언어.
      - 웹 페이지는 크게 정적(Static)과 동적(Dynamic)으로 나뉜다.
      - 동적 웹 페이지는 웹 서버에 이미 저장된 파일(HTML, 이미지, JavaScript 등)을 클라이언트에게 전송하는 웹페이지
      - 정적 웹 페이지는 사용자 요청에 따라 동적으로 만들어 전송하는 웹페이지
   2. Servlet(Server Application Let)
      1. Servlet의 개념
      - 웹 기반의 요청에 대한 동적인 처리가 가능한 하나의 클래스이다.
      2. Servlet Program의 기본적인 동작 과정<br>
      ![servlet 프로그램의 기본 동작 과정](Img/servlet-program.png)
        1. Web Server는 HTTP request를 WAS(Web Application Server)내에 Web Container(Servlet Container)에게 위임한다.
           1. web.xml 설정에서 어떤 URL과 매핑되어 있는지 확인
           2. 클라이언트(browser)의 요청 URL을 보고 적절한 Servlet을 실행
        2. Web Container는 service() 메서드를 호출하기 전에 Servlet 객체를 메모리에 올린다
           1. Web Container는 적절한 Servlet 파일을 컴파일(.class 파일 생성)한다.
           2. .class 파일을 메모리에 올려 Servlet 객체를 만든다.
           3.  메모리에 로드될 때 Servlet 객체를 초기화하는 init() 메서드가 실행된다.
        3. Web Container는 Request가 올 때마다 thread를 생성하여 처리한다.
           1. 각 thread는 Servlet의 단일 객체에 대한 service() 메서드를 실행한다.
