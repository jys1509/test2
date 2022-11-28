## 정보 조사

- MVC 1, MVC 2 구조와 차이점
- HTTP 프로토콜이란
- 기본 키 , 제약 조건 이란 DB
- 인덱스의 기능 
- 데이터 db로 추가했을떄 에러가뜨는데 왜 에러가뜨는지 추정해보기

## 실습

- JAVA 윈도우에 깔고 환경설정 해보기 -(고급시스템설정-환경변수)
- 사람인, 점핏, 잡코리아, 원티드 -
- JAVA 문제 계속해서 풀기


MVC 1, MVC 2 구조와 차이점

mvc1 패턴은 클라이언트에서 ->(http) jsp(view + controller) 
->(model)데이터 ->db >다시 model ->controller -> view로 클라이언트 
고객에게 보여줌 
mvc2 패턴은 컨트롤러에 jsp(view)랑 controller(필터/servlet) 가 따로분리
고객 ->컨트롤러(서블릿) ->모델 ->디비 >모델 ->jsp(view만)->고객
mvc1은 만들기쉽지만 유지보수가어려움 mvc2는 패턴은 이해하기어렵지만 
유지보수장점이있어 각각 모듈화되있어 역활분담도 되고 회사들은 mvc2방식씀
참조 : https://velog.io/@gillog/a-j5c0h49n 

http 프로토콜이란 http서버는 기본 포트 값이 80번
ex)post(보낼방식)/basic/resultjsp(어디로요청하는지에대한정보)?
   lck&age=20(서버에전달해주고자하는값) http/1.1(버전)
클라이언트에서 컨트롤러로 보낼떄 송신방식
요청 메서드
get 검색,얻기 (체크박스체크,검색)그래서 url길이의 제한이있다 (select) <요청 바디가없음
post 보내기 request body에 데이터 담아서 전송 (insert) 
PUT 정보를 업데이트하기 위해서 사용한다. (UPDATE)
DELETE 정보를 삭제하기 위해서 사용한다. (DELETE)
HEAD (HTTP)헤더 정보만 요청. 해당 자원이 존재하는지 혹은 서버에 문제가 없는지를 확인하기 위해서 사용
response 응답 데이터 2xx 성공 4xx클라이언트오류 404 서버자원없. 5xx서버오류
참조 : https://www.youtube.com/watch?v=aCSryu_emlA

기본 키 , 제약 조건 이란 DB

1.NOT NULL 조건
컬럼을 필수 필드화 시킬 때 사용.
NOT NULL 제약조건 설정 시 해당 컬럼에는 꼭 데이터를 입력해야 함.
2.UNIQUE 조건
데이터의 유일성을 보장(=> 중복되는 데이터가 존재할 수 없음)하고, 자동으로 인덱스가 생성.
unique은 null허용하지만, primary key는 null허용 안함
unique은 하나의 테이블에 여러개 올 수 있지만, primary key는 하나만 존재
3.CHECK 조건
컬럼의 값을 어떤 특정 범위로 제한
4.DEFAULT (컬럼 기본값) 지정
데이터를 입력하지 않아도 지정된 값이 기본으로 입력된다.
default라고 값을 명시하면 기본값이 들어감
열이름이 명시되지 않으면 자동 기본값
값이 직접 명기되면 기본값은 무시됨.
5.primary key 
기본키 : UNIQUE + NOT NULL 의 결합과 같음.
기본키는 그 데이터 행을 대표하는 컬럼으로서의 역할을 수행하여 다른 테이블에서 
외래키들이 참조할 수 있는 키로서의 자격을 가지고 있다. => 참조 무결성
UNIQUE 제약조건과 마찬가지로 기본키를 정의하면 자동으로 인덱스를 생성, 그 이름은 기본 키 제약조건의 이름과 같다.
만약 테이블에 각 필드값에 유니크한 값이 없다면, 필드 두 개를 묶어서 primary key로 지정 가능하다.
ex )constraint pk_value primary key (필드1,필드2)
6.FOREIGN KEY (외래키) 지정
기본키를 참조하는 컬럼 or 컬럼들의 집합 (외래키는 기본키나 유니크가 아니면 생성 제약)
외래키를 가지는 컬럼의 데이터 형은 외래키가 참조하는 기본키의 컬럼과 데이터 형이 일치해야 한다.
(이를 어기면 참조 무결성 제약에 의해 테이블을 생성할 수 없음 !)
외래키에 의해 참조되고 있는 기본키 : 삭제 불가 !!
on update cascade하면 기본키가 수정될 경우 외래키도 같이 수정해준다는 말
ON DELETE CASCADE 연산자와 함께 정의된 외래키의 데이터는 그 기본키가 삭제될 때 같이 삭제된다

참조 :https://inpa.tistory.com/entry/DB-%F0%9F%93%9A-%ED%85%8C%EC%9D%B4%EB%B8%94-%EC%A0%9C%EC%95%BD-%EC%A1%B0%EA%B1%B4-%F0%9F%95%B5%EF%B8%8F-%EC%A0%95%EB%A6%AC

인덱스의 기능
INDEX:
검색 키로서 검색 속도를 향상시킨다. ( UNIQUE, PRIMARY KEY 생성시 자동적으로 생긴다.
index에 주로 사용된느 자료구조는 b-tree(2진트리반대) 알고리즘 루트 브런치 리프node
btree를 사용하는이유 binary search tree는 모든 리프노드들이 같은레벨을 가질수 있도록
자동으로 균형을 맞추는트리 시간복잡도는 평균적으로 o(log N) 하지만 최악의경우 시간복잡도o(N)

참조 : https://www.youtube.com/watch?v=at2sMaNYqCE

데이터 db로 추가했을떄 에러가뜨는데 왜 에러가뜨는지 추정해보기
SSMS(SQL Server Management Studio(SSMS) 방지옵션이 설정되서.라고생각
변경 내용을 저장할 수 없습니다. 변경한 내용을 적용하려면 다음 테이블을 삭제하고 다시 만들어야 합니다
라고 에러가 뜬다
그이유는테이블 다시 만들기가 필요한 변경 내용 저장 방지 옵션이 
기본적으로 SQL Server Management Studio 사용하도록 설정되어 있기 때문에 발생
열에 대해 Null 허용 설정을 변경합니다.
테이블의 열 순서를 다시 지정합니다.
열 데이터 형식을 변경합니다.
새 열을 추가합니다.
테이블의 text/image 또는 해당 filegroup 데이터를 변경합니다.
중 하나이상을 변경할떄 발생

해결법
LTER TABLE Transact-SQL 문을 사용하여 테이블의 메타데이터 구조를 변경
ex) MyTable이라는 테이블에서 datetime 형식의 MyDate 열을 변경하여 
NULL 값을 허용하려면 다음을 사용
 alter table MyTable alter column MyDate7 datetime NULL

테이블 다시 만들기가 필요한 변경 내용 저장 방지 옵션을 변경하려면 다음 단계를 수행
1.SQL Server Management Studio를 엽니다.
2.도구 메뉴에서 옵션을 클릭합니다.
3.옵션 창의 탐색 창에서 Designers를 클릭합니다.
4.테이블 다시 만들기가 필요한 변경 내용 저장 방지 확인란을 선택하거나 선택 취소한 
   다음 확인을 클릭합니다.

참조 : https://learn.microsoft.com/ko-kr/troubleshoot/sql/ssms/error-when-you-save-table