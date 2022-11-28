## 정보 조사

- Spring Initializer 에 있는 정보 조사
- 어노테이션이란??
- Bean 이란??
- Framework 와 Library 의 차이점

## 실습
1.annotation ?
에노테이션은 주석이라는 의미를 가진다.
ex)@override 메서드 오버라이드
@컨트롤러 이런게 이노테이션 @autowired 또는
@inject 또는 appllicatiomcontext 에서 getbean()으로 직접 꺼내씀

자바 소스 코드에 사이에 @ 기호를 앞에 붙여서 사용하는데, 
JDK 1.5 버전 이상에서 사용 가능하다.
컴파일러에게 코드 작성 문법 에러를 체크하도록 정보를 제공
소프트웨어 개발툴이 빌드나 배치시 코드를 자동으로 생성할 수 있도록 정보 제공
실행시(런타임시)특정 기능을 실행하도록 정보를 제공

2.bean 이란
개발자가 일일히 객체를 직접 생생하고 제어하는 것이 아닌
프로그램(스프링)이 개발자의 코드를 호출해서 객체를 생성하고 제어하는 것
Spring 이 생성하고 제어하는 자바 객체를 Bean 이라고 한다.
ApplicationContext.getBean()으로 얻을 수 있는 객체이다
1. @ComponentScan(찾으라고알려주는거) 과
@Component(빈으로등록하고싶은class) 어노테이션을 사용하는 방법
2. xml 파일에 직접 bean을 등록하는 방법
3. https://suzyalrahala.tistory.com/36 (참고했음) <- 빈설정방법!


Inversion of Control

3.framework 와 Library 의 차이점
프레임워크
애플리케이션 개발시 필수코드 알고리즘db연동같은 기능들을 위해
뼈대를 제공 이 뼈대위에서 코드작성
쉽게말해 프레임워크가 짜놓은틀에서 수동적 동작 제어흐름은 프레임워크
자바 이클립스 스프링
파이썬 딩고
C는 ASP.NET
JS는 NODE
자바기반 jsp를위한 struts
라이브러리
소프트웨어 개발할때 프로그램이 사용하는 비휘발성자원모임/특정기능모아둔코드/함수집합
제어흐름이 직접 능동적으로 라이브러리를 호출하거나 기존에
구성된 함수나 코드를 가져다씀
node.js에서 npm(아직 난사용해본적없음)
html에서 jqurey
웹에서 인터페이스개발react.js
내가지금하고있는 intellij 는 jar (자바)
차이점
프워는 뼈대 라이브러리는 함수모음

spring initializer

Maven은 프로젝트의 전체적인 라이프사이클을 관리하는 도구
maven 에서는 미리 정의하고 있는 빌드 순서가 있으며 이 순서를 라이프사이클이라고 한다
Gradle은 메이븐보다 최대 100배 빠르다.
지금 시점에서 Gradle을 사용하지 않을 이유는 익숙함 뿐인 것 같다
우리가 프로젝트에서 작성한 java 코드와 프로젝트 내에 필요한 각종 xml, properties, jar 파일들을 
JVM이 나 WAS 가 인식할 수 있도록 패키징 해주는 빌드 과정 == "빌드 자동화 도구" 라고 할 수 있다!

- 프로젝트 생성, 테스트 빌드, 배포 등의 작업을 위한 전용 프로그램이라 할 수 있다.

java(8,11,17)
Long Time Service 란 말 그대로 장기간에 걸쳐 지원을 해주겠다는 뜻
jRE JDK
JDK 는 JRE를 포함할 뿐만 아니라 컴파일러(javac), javadoc, jar 등 개발에 유용한 도구들을 포함
결론은 JRE JVM 는 자바 실행환경이고, JDK 는 자바 개발 도구라는 것이다
java 8 11 17 이 3가지버전들은 이 버전들이 LTS(Long Term Support) 버전이기 때문이다

java 8
오라클이 자바 인수 후 출시한 첫 번째 LTS 버전
Oracle JDK(Oracle사에서 지원하는 버전으로 유료) , Open JDK(오픈소스 기반의 무료)로 나뉨
람다식(Lambda), Stream API

java 11
Oracle JDK와 Open JDK 통합
Oracle JDK가 구독형 유료 모델로 전환
람다 지역 변수 사용법 변경


java 17

가장 최신 LTS 버전
애플 M1 및 이후 프로세서 탑재 제품군에 대한 정식 지원 (Mac 유저들 환호)

jar?

JAR 파일은 원하는 구조로 구성이 가능하며 JDK(Java Development Kit)에 
포함하고 있는 JRE(Java Runtime Environment)만 가지고도 실행이 가능합니다
JAVA 어플리케이션이 동작할 수 있도록 자바 프로젝트를 압축한 파일로

war?

웹 어플리케이션(Web Application) 압축 파일 포맷
웹 관련 자원만 포함하고 있으며 이를 사용하면 웹 어플리케이션을 쉽게 배포




-------------------------------------


dependencies (의존성)
스프링부트가 의존성이라 나에게 필요한 라이브러리들을 불러와 사용가능

lombok (디벨로프 툴)
코드를 간결히 사용시켜주는 라이브러리


자바 단축기 같은역활 ex)get set 게터세터 같은거 길게호출할필요없이
쓸수잇음(사용법은 아직모름)

spring wep
스프링 웹 페이지 열떄 사용하는 라이브러리

thymeleaf 템플릿 엔진처리
컨트롤러에서 뷰로넘기고 타임리프가 html 변환후 웹으로넘김

mybatis framework // JPA 
마이바티스 프라임워크란
sql문으로 키널값넣는 박스들을 유지보수하는 프라임워크

JDBC

db데이터를 다루는 객체관계맵퍼 mapping
데이터 저장조회변경삭제등 에플리케이션을 종료하고 다시실행해도
이전에 저장한 데이터를 다시불러올수있는 기술(persistence퍼시스턴스)데이터지속성
mariadb driber
데이터베이스 연결 라이브러리