This doc define what kind of function exist in mobile project.

1. Home Page

- move_to_loginPage(로그인 페이지로 이동)
- move_to_buttonPage(해당 버튼 페이지로 이동 ex. 인기 가이드 리스트, 내 가이드 리스트 등)

2. Login Page

- log_in_web(웹에 로그인하기)
- move_to_joinPage(가입 페이지로 이동)
- move_to_homePage(홈 페이지로 이동)

3. Join Page

- join_in_web(웹에 가입하기)
- check_for_idDuplicate(아이디 중복검사하기)
- password_check(It is validation, not function

4. Menu bar
- move_to_home (홈 화면으로 이동)
- move_to_List (리스트 화면으로 이동)
- move_to_Popular (미구현)
- move_to_Search (미구현)
- move_to_Freinds (미구현)
- move_to_Mypage (마이페이지 화면으로 이동)

5. PlaceBook List
- move_to_PlaceBookMain   (클릭시 해당 리스트 페이지(5번)으로 이동)
- create_NewList  (클릭시 리스트 생성)

6. Placebook Main Page (6page include)
- read_PlacePost   (완성되어있는화면(7번)으로 이동)
- create_NewPost    (편집화면으로 이동 (8번) )
- click_MapMarker  (마크 클릭시 타이틀,평점  ->title ->points)

7. Create Post 

- confirm_post(글 게시하기)
- cancel_post(글 작성 취소하기)
- upload_image(이미지 업로드하기)
- select_mainImage(해당이미지 메인이미지로 선택하기)
- confirm_position(해당 위치 게시글 위치로 확정하기)

8. Show post

- move_to_editPost(글 편집 페이지로 이동하기)
- show_delete_confirmDialog(삭제 확인 메세지 띄우기 정말 삭제하시겠습니까?)
- delete_post(게시글 삭제하기)
- close_dialog(다이알로그 취소하기)
- toggle_likeButton(좋아요 버튼 클릭 선택 취소)
- show_total_like(전체 좋아요 숫자 보여주기)

9. Edit post

- confirm_post(게시글 편집 확정하기)
- cancel_post(글 편집하기 취소)
- upload_image(이미지 업로드하기)
- select_mainImage(메인이미지 선택하기)
- confirm_position(해당 위치 게시글 위치로 확정하기)

10. Mypage       

- move_to_editMyInfo(마이페이지로 이동하기)
- move_to_showMyList(내 리스트 보기로 이동하기)

11. Edit MyInfo

- confirm_myInfo(내 정보 수정 확정하기)
- cancel_myInfo(내정보 수정 취소하기)