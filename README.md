# mbcac_project


## 팀 프로젝트 안내
* 주제 : 열심히 하자
* 기간 : 3달
  +1달 : 분석
  +1달 : 설계
  +1달 : 구현
   -1주 : 로그인
   -2주 : 게시판
   -3주 : 뉴스

##아래의 코드를 참고하세요
```jsp
<%@ page language="java" contentType="application/json; charset=UTF-8" pageEncoding="UTF-8"
	trimDirectiveWhitespaces="true"%>
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<%@ taglib prefix="fmt" uri="http://java.sun.com/jsp/jstl/fmt" %>

<jsp:useBean id="dao" class="com.mbcac.board.BoardDAO"/>
<jsp:useBean id="board" class="com.mbcac.board.BoardVO">
   
   <jsp:setProperty name="board" property="title" param="title" />
   <jsp:setProperty name="board" property="author" param="author" />
   <jsp:setProperty name="board" property="contents" param="contents" />
   <jsp:setProperty name="board" property="parent" param="parent" />
   
</jsp:useBean>

<c:set var="saved" value="${dao.addReply(board)}"/>

{"saved":${saved},"bnum":${saved}}
```
<h3 style="background-color
