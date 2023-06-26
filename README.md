# git 사용방법
-------------
### 1. 계정 연결 준비물
-이메일 주소 : gitHub 가입 했던 이메일 주소
-사용자 이름 : Giyong8504
-폴더 경로 : C:\Users\KGY\study_java\자바\git
<br>
<br>
### 2. 계정 동기화
```
git config --global user.name "github 사용자 이름"
git config --global user.email "github 이메일 주소"

참고) 나만 쓰는 컴퓨터가 아닐 경우 -> --global 제거
git config user.name "github 사용자 이름"
git config user.email "github 이메일 주소"
```
<br>
<br>
### 3. 로컬 레포지토리 생성
```
cd C:\Users\KGY\study_java\자바\git
git init 입력
```

### 4. 원격 레포지토리 연결하기
![image](https://github.com/Giyong8504/git/assets/128211712/ba304c2f-243d-4db4-82c8-eaa539b38717)

```
git remote add origin 원격 레포지토리 주소 : 원경 저장소(레포지토리) 주소 추가
git remote set-url origin 원격 레포지토리 주소 : 기존 주소 변경
```

### 5. 스테이징 단계
```
git add 파일명, 파일경로
git add . (모든파일)
```

### 6. 스냅샷 단계 (commit) - 버전 기록 : 복구할 시점 만들기
```
git commit -m "작업 내용 메모"
```

### 7. 원격 저장소에 반영 ( 로컬 -> 원격 )
```
git push origin 원격 브랜치명
```

### 8. 로컬 저장소에 반영 ( 원격 -> 로컬 )
-작업 전 확인하고 pull해서 코드 다운.
```
git pull origin 원격 브랜치명
```

-참고) 원격 -> 로컬
```
git clone 원격 저장소 주소
```

---------------
## 브랜치
-커밋로그
```
git log
git log --oneline : 로그를 한줄로 짧게 확인
```

-버전 관리
git checkout 커밋 ID
git checkout - : 직전 단계로 복구


브랜치
master 브랜치 - 기본 브랜치
git branch : 현재 생성된 브랜치 목록
git branch 브랜치명 - 현재 브랜치의 소스와 함께 브랜치가 생성
git checkout 브랜치명 - 브랜치로 이동 

git branch -d 브랜치명; - 브랜치 삭제 (해보면 에러나면서 안된다. 이떄 아래꺼로)
	 -D 브랜치명 - 브랜치 강제 삭제 

(member 기준에서 브랜치해서 추가했기 때문에 멤버 복사됨. - 멤버기준에서 작업중이다.)



나눠서 작업이 다 끝나면 다 합쳐야한다.
[브랜치 병합]
git merge 브랜치명 - 현재 브랜치에 브랜치명의 브랜치를 병합

	-테스트 브랜치 하나 생성 -> 다른 작업을 병합 -> 테스트 -> 마스터에 병합 (마스터에서 테스트르 만듬)

원격 레포지토리(원격 저장소)
 - 깃허브
 - 비트버킷
 - 깃랩




sourcetree - GIT GUT 툴 (설치해보자)

cls는 작업내용 삭제

===========
md git 폴더명
cd git 폴더명
=======
dir/w
=====





5bd47c3 (HEAD -> test) 작업4 완료
86add4e (origin/master, master) 작업3 완료  (원격에 반영하면 origin이 붙어있음)
