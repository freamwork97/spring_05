1. 프로젝트 만들기 연습
    1. 프로젝트 이름: spring_05
    2. 기본패키지: com.icia.demo
    3. 클래스
        1. HomeController
           - index.jsp를 출력함
        2. DemoController
           - req1, req2 주소 요청을 각각 처리함
        3. DemoService
        4. DemoDTO
           - name(String)
           - age(int)
    4. 시작화면: index.jsp
        1. demo1.jsp 화면으로 이동하는 링크 있음.
        2. demo2.jsp 화면으로 이동하는 링크 있음.
    5. demo1.jsp
        1. query string 방식으로 name=’손흥민’, age=31 값을 req1 주소로 요청함
        2. 컨트롤러에서는 이 값을 받아서 서비스의 req1 메서드로 전달함
        3. 서비스에서는 전달받은 name, age를 DTO 객체에 담아서 리턴함
        4. 컨트롤러에서 리턴받은 DTO객체를 model에 담아서 req1.jsp로 가져가고 req1.jsp에서 값을 출력함.
    6. demo2.jsp
        1. form 태그에 name, age값을 입력받아서 req2 주소로 post 요청함
        2. 컨트롤러에서는 DTO로 바로 받고 서비스의 req2 메서드로 전달함
        3. 서비스에서는 전달받은 DTO 객체를 리스트 객체에 추가하고 리스트를 리턴함
        4. 컨트롤러에서 리턴받은 리스트 객체를 model에 담아서 req2.jsp로 가져가고 req2.jsp에서 값을 출력함. (출력되는 값은 하나임)
2. 메서드(method)
    1. 특정 기능을 수행하기 위한 코드블록
    2. 혼자서는 실행할 수 없음. 어디에서든 호출을 해줘야 실행됨.
    3. 메서드 정의
       1. 리턴타입
          - 리턴없다: void
          - 리턴있다: 리턴하는 값의 타입(int, boolean, String, oooDTO, List<oooDTO> 등)
       2. 매개변수
          - 메서드를 호출할 때 넘겨주는 값
          - 메서드 실행시 입력해주는 입력값이라고 생각해도 됨
       3. 메서드 이름
          - 이름을 지을 때는 camelCase로
            - hello method -> helloMethod
       4. 접근제한자(public, private)