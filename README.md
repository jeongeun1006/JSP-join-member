# JSP-join-member
<회원 정보 출력>
브라우저에서 /mem.do로 요청하면 서블릿 MemberController가 요청을 받아 MemberDAO의 listMembers() 메서드를 호출한다.
MemberDAO의 listMembers() 메서드에서 SQL문으로 회원 정보를 조회한 후 회원 정보를 MemberVO에 설정하여 반환함.
다시 MemberController에서는 조회한 회원 정보를 회원목록창(listMembers.jsp)로 포워딩함.
회원 목록창(listMembers.jsp)에서 포워딩한 회원 정보를 목록으로 출력
<회원 정보 추가>
회원 가입창에서 회원 정볼르 입력하고 URL패턴을 /member/addMember.do로 서버에 요청
MemberController에서 getPathInfo()메서드를 이용해 요청명인 /addMember.do를 받아온다
요청명에 대해 MemberDAO의 addMember()메서드를 호출
addMember()메서드에서 SQL문으로 테이블에 회원 정보를 추가
<회원 정보 수정 및 삭제>
회원정보 수정창에서 회원 정보를 수정하고 수정하기를 클릭해 /member/modMember.do로 컨트롤러에 요청
회원 목록창에서 삭제를 클릭해 요청명 /member/delMember.do와 회원 ID를 컨트롤러로 전달
