#TIL
- 오늘 공부한 내용을 남깁니다.

    - CLI : git 서치, cli 사용해 보기

    - CLI 관련 용어 학습
        / : Root Directory
        ~ : Home directory
        절대 경로 vs 상대 경로
        ./ : 현재 작업하는 폴더
        ../ : 부모폴더

    - 터미널 명령어
        touch : file 생성
        mkdir : folder 생성
        ls : list segments 작업 중 디렉토리의 폴더/파일목록 조회
        -a ; all, -l ; long, 
        mv ; move(이동, 이름변경), 
        cd; change directory, 
        rm: remove, 
        remove -r : 폴더 지우기
        start, open : folder, file 열기

    - vscode 설치

    - typora 설치
        -markdown 용어 사용해보기
        -makrdown 문법
            - headings : #~ ######
            - list : -, *, +, 1, 2, 3 사용
                    tab키 이용하여 들여쓰기 가능
            - 강조(emphasis) :
                기울임; *글자*
                굵게 : **글자**
                취소 : ~~글자~~
            - 코드
                한 줄의 인라인 코드 : `` 안에
                블록코드 : ``` 백틱 3번 입력하고 코드종류 사용
            - 링크
                [표시할 글자](이동할 주소)
            - 이미지
                ![대체 텍스트](이미지 주소)
            - 인용 : >, 중첩가능
            - 표 : ctrl + t, 파이프와 하이픈 이용가능
            - 수평선 : - * _ 3번 이상 작성

    - Git 기초
        - 커밋 작성자 설정
          git config --global user.name
          git config --global user.email
        - 확인법 : git config --global --list
        - Working directory : 작업공간
        - Staging area : 커밋을 위한 파일 폴더가 추가되는 곳
        - Repository : Staging area의 변경사항 저장
        - Git은 WD->SA->R로 버전 관리를 수행
        - git init : 현재 작업 중 디렉토리를 git으로 관리, .git 생성하고 (master) 표현됨
        - git status : 현재 상태 표현
        - untracked(git에서 관리안함) / tracked(git에서 관리함)
        - unmodified -> modified -> staged

        - git add
            git add a.txt : 특정 파일 생성
            git add my_folder : 폴더 생성
            git add . : 폴더/파일 전부 생성
        - git commit
            git commit -m " first commit" : 변경 사항을 커밋으로 저장하는 명령어
            SHA-1 algorithm으로 변환된 ID 가짐
        - git log
            커밋 내역 조회 가능(ID, writer, time, msg..)
            --oneline : 한줄로 조회
            --graph : branch, merge 내역을 그래프로
            --all : 모든 브랜치 내역 표출
            --reverse : 최신을 가장 아래로
            -p : 변경 내용도 표출
            -2 : 변하는 개수 만큼(n 숫자)

    -Github 가입 및 연결하기
        - 원격 저장소(remote repository) 생성
            + -> New repository
            vscode 에서
            git init 통해 로컬 저장소 만들기
            git remote 통해 원격 저장소 등록
            (git remote add origin 주소)
            git remote -v : 조회
            git remote rm <name> : 삭제
            
        - 원격 저장소에 커밋 업로드
            git push <저장소 이름> <브랜치 이름> 형식
            -u : 다음 커밋부터 옵션 생략
            (git push origin master)
            (git push -u origin master) : 다음부터
            (git push) 라고만 작성해도 push 올라감
        - 확인법 : github에서 업로드 확인
            drag->upload 하지 않기
            git add->git commit->git push 단계 이용