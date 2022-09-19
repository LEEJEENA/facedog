<h3 align="center"><b>페이스독(Facedog)</b></h3>

<h4 align="center">📆 2022.09.19 ~ </h4>
<br>

---

<h3><b>🎫 프로젝트 소개 🎫</b></h3>
 **반려견의 일상을 사진과 글로 기록하고, 다른 견주들과 소통할 수 있는 커뮤니티**

 - 상세 설명 : - 반려견의 일상을 찍은 사진과 반려견에 관한 글을 업로드 할 수 있습니다.
 - 글에서는 댓글을 통해 서로 소통할 수 있습니다.
			
<br><br> 

<h3><b>🎞 프로젝트 시연영상 🎞</b></h3>


---

<br><br>
<h3 align="center"><b>🎬 Getting Started 🎬</b></h3>
<pre>
<code>
</code>
</pre>

<br>
<h3 align="center"><b>📂 Project Directory Structure 📁</b></h3>
<pre>
<code>
</code>
</pre>
<br>

---

<h3 align="center"><b>📢 Main function 📢</b></h3>
<br>
<h4><b>📰 Login Page 📰</b></h4>

<table width="100%">
    <tr>
        <td width="50%"></td>
        <td width="50%">
            <h5>로그인</h5>
            <ul>
                <li>JWT 방식으로 구현</li>
                <li>회원가입 버튼 클릭 시 회원가입 페이지로 이동</li>
            </ul>
        </td>
    </tr>
</table>

---

<br>
<h4><b>📰 Join Membership Page 📰</b></h4>

<table width="100%">
    <tr>
        <td width="50%"><img src="<img src="https://user-images.githubusercontent.com/113873156/190961302-544e72bb-9b87-4b9b-bdcb-b0eb225bf315.png"></td>
        <td width="50%">
            <h5>회원가입</h5>
            <ul>
                <li></li>
                <li></li>                
                <li></li>
                <li></li>
            </ul>
        </td>
    </tr>
</table>

---

<br>
<h4><b>📰 Post Section Page 📰</b></h4>

<table width="100%">
    <tr>
        <td width="50%"></td>
        <td width="50%">
            <h5>메인 화면</h5>
            <ul>
                <li></li>
                <li></li>                
                <li></li>
                <li></li>
            </ul>
        </td>
    </tr>
</table>

---

<br>
<h4><b>📰 Post Writing Page 📰</b></h4>
<table width="100%">
    <tr>
        <td width="50%"></td>
        <td width="50%">
            <h5>글쓰기 화면</h5>
            <ul>
                <li></li>
                <li></li>                
                <li></li>
                <li></li>
            </ul>
        </td>
    </tr>
    <tr>
        <td width="50%"></td>
        <td width="50%">
            <h5>글쓰기 화면</h5>
            <ul>
                <li>글 작성 후의 모습</li>
            </ul>
        </td>
    </tr>
</table>

---

<br>
<h4><b>📰 Post Detail Page 📰</b></h4>

<table width="100%">
    <tr>
        <td width="50%"></td>
        <td width="50%">
            <h5>포스트 상세 화면</h5>
            <ul>
                <li></li>
                <li></li>                
		<li></li>
            </ul>
        </td>
    </tr>
</table>
<br>

---

<br>
<h3 align="center"><b>🏷 API Table 🏷</b></h3>
<table width="100%">
    <tr align="center">
	<td width="12%"><b>기능</b></td>
        <td width="5%"><b>Method</b></td>
        <td width="12%"><b>URL</b></td>
        <td width="30%"><b>Request</b></td>
        <td width="31%"><b>Response</b></td>
    </tr>
    <tr>
        <td width="12%">메인화면 페이지 로드</td>
        <td width="5%">GET</td>
        <td width="12%">/</td>
        <td width="30%"></td>
        <td width="31%">Token 검증됨 - render_template("layout_postlist.html", postdata=postdata)<br>Token 검증 안됨 - url_for("login", msg="로그인 정보가 존재하지 않습니다.")</td>
    </tr>
    <tr>
        <td width="12%">로그인 페이지 로드</td>
        <td width="5%">GET</td>
        <td width="12%">/login</td>
        <td width="30%">msg</td>
        <td width="31%">render_template('login.html', msg=msg)</td>
    </tr>
    <tr>
        <td width="12%">회원가입 페이지 로드</td>
        <td width="5%">GET</td>
        <td width="12%">/joinMembership</td>
        <td width="30%"></td>
        <td width="31%">render_template('join_membership.html')</td>
    </tr>
    <tr>
        <td width="12%">글쓰기 페이지 로드</td>
        <td width="5%">GET</td>
        <td width="12%">/writing</td>
        <td width="30%"></td>
        <td width="31%">Token 검증됨 - render_template('layout_writing.html')<br>Token 검증 안됨 - url_for("login", msg="로그인 정보가 존재하지 않습니다.")</td>
    </tr>
    <tr>
        <td width="12%">회원가입</td>
        <td width="5%">POST</td>
        <td width="12%">/signUp</td>
        <td width="30%">{'id': user_id,  'pw': user_password}</td>
        <td width="31%">{'msg': '회원가입이 완료되었습니다.'}</td>
    </tr>
    <tr>
        <td width="12%">ID 중복검사</td>
        <td width="5%">POST</td>
        <td width="12%">/check_dup</td>
        <td width="30%">{'id': check_id}</td>
        <td width="31%">중복 시 - {'msg': "사용 가능한 아이디 입니다."}<br>중복 아닐 시 - {'exists': "이미 존재하는 아이디 입니다."}</td>
    </tr>
    <tr>
        <td width="12%">로그인</td>
        <td width="5%">POST</td>
        <td width="12%">/api/login</td>
        <td width="30%">{'id': username_give, 'pw': password_give}</td>
        <td width="31%">로그인 성공 - {'result': 'success', 'token': token}<br>로그인 실패 - {'result': 'fail', 'msg': '아이디/비밀번호가 일치하지 않습니다.'}</td>
    </tr>
    <tr>
        <td width="12%">글 저장</td>
        <td width="5%">POST</td>
        <td width="12%">/api/writing</td>
        <td width="30%">{'writer_name': writer_name, 'cafe_name': cafe_name, 'cafe_address': cafe_address, 'cafe_coment': cafe_coment, 'cafe_img': cafe_img, 'user_mentlist': user_mentlist}</td>
        <td width="31%">Token 검증됨 - {'msg': '저장되었습니다.'}<br>Token 검증 안됨 - url_for("login", msg="로그인 정보가 존재하지 않습니다.")</td>
    </tr>
    <tr>
        <td width="12%">상세 페이지 로드</td>
        <td width="5%">POST</td>
        <td width="12%">/<writer_name>/<cafe_name></td>
        <td width="30%">{'writer_name': writer_name, 'cafe_name': cafe_name}</td>
        <td width="31%">Token 검증됨 - render_template("layout_postview.html", writer_id=writer_id, cafe_name=cafe_name, cafe_address=cafe_address, cafe_img=cafe_img, cafe_coment=cafe_coment, user_mentlist=user_mentlist, current_user=user_id)<br>Token 검증 안됨 - url_for("login", msg="로그인 정보가 존재하지 않습니다.")</td>
    </tr>
    <tr>
        <td width="12%">댓글 저장</td>
        <td width="5%">POST</td>
        <td width="12%">/api/userment</td>
        <td width="30%">{'writer_name': writer_name, 'cafe_name': cafe_name, 'ment': user_ment_info}</td>
        <td width="31%">{'msg': '댓글이 저장되었습니다.'}</td>
    </tr>
    <tr>
        <td width="12%">댓글 삭제</td>
        <td width="5%">POST</td>
        <td width="12%">/api/delment</td>
        <td width="30%">{'writer_name': writer_name, 'cafe_name': cafe_name, 'ment': user_ment_info}</td>
        <td width="31%">{'msg': '댓글이 삭제되었습니다.'}</td>
    </tr>
    <tr>
        <td width="12%">현재 사용자 조회</td>
        <td width="5%">GET</td>
        <td width="12%">/api/getid</td>
        <td width="30%"></td>
        <td width="31%">Token 검증됨 - {'user_id': user_id}<br>Token 검증 안됨 - url_for("login", msg="로그인 정보가 존재하지 않습니다.")</td>
    </tr>
</table>

<br>

---


<h3 align="center"><b>✏ Trouble Shooting ✏</b></h3>
<br>
<details>
    <summary>
        <b></b>
    </summary>
  
</details>

<details>
    <summary>
        <b></b>
    </summary>
  <br><b></b>
    
```html
    <!-- File : "../templates/join_membership.html" -->
    <button id="joinBox" onclick="signup()" type="button"></button>
```

</details>

<details>
    <summary>
        <b></b>
    </summary>
<br><b></b>


</details>
	
<details>
    <summary>
        <b></b>
    </summary>
<br><b></b>


</details>

<details>
    <summary>
        <b></b>
    </summary>

<br><b></b>
    
</details>

<details>
    <summary>
        <b></b>
    </summary>
<br><b></b>
<br>

</details>

<details>
    <summary>
        <b></b>
    </summary>
<br><b></b>
<br>
 

</details>


