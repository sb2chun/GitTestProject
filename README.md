# GitTestProject

해당 Project는 
 작업자 간의 git을 통해 협업하는 경우에 관한 Sample Test입니다.
 
. 개발리더 A) Git 생성 

$git init                                 // git 초기화. (최초 1회 실행)
$git add .                                // 해당 모든 파일을 staging에 올려두기
$git commit -m "first commit blahblah"    // Local Repository에 올려두기

$git remote add origin GITHUB 주소'       // Local과 remote(gitHub) 사이의 연결 고리 생성 

$git push origin master                   // remote(gitHub)에 push.
 + Github에서 소스 올라간 것 확인 가능

-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-

. 개발자 B) 소스 변경 후 PR요청

$git clone 'GITHUB 주소' 'Folder명'       // git source 복사

~~~ 소스 수정 ~~~

$cd 'Folder명'
$git add .                                      // staging에 추가
$git commit -m "first Commit by Developer B"    // Local Repository에 Commit

$git checkout -b "Branch명"                     // Branch 생성 
$git push origin "Branch명"                     // 해당 브랜치에 push
 + github에 접속해서 PR(Push&Request) 요청       // 해당 Branch에 대해서 Master Branch에 합쳐달라고 요청하는 작업.
 
-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-

 . 개발리더 A) PR 확인 후 Merge.
 
 Fin.
