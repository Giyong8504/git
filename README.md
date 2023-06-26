# git 사용방법
-------------
### 1. 계정 연결 준비물
-이메일 주소 : gitHub 가입 했던 이메일 주소
-사용자 이름 : kky5163
-폴더 경로 : C:\Users\KGY\study_java\자바\git


### 2. 로컬 레포지토리 생성
```
git init 입력
```



cls는 작업내용 삭제

===========
md git 폴더명
cd git 폴더명
=======
dir/w
=====



계정을 동기화하기 위해 설정
계정연결 설정
	git config user.name "kky5163" 
git config --global user.name "kky5163"  (나만쓸때 --global 사용.)
git config --global user.email "kky5163@naver.com"	

스냅샷 방식 

스테이징 단계
git add 파일명, 파일경로
git add . (모든파일)

스냅샷 단계 (커밋) - 버전 기록  -(사용하는 이유 복구할 시점 만들기)
git commit -m "작업 내용 메모"


커밋로그
git log
git log --oneline : 로그를 한줄로 짧게 확인

버전 관리
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



원격 레포지토리 연결하기
git remote add origin 원격 레포지토리 주소   (주소 복사해서 cmd창에 오른쪽 마우스 클릭) : 원경 저장소(레포지토리) 주소 추가
git remote set-url origin 원격 레포지토리 주소 : 기존 주소 변경 (잘못 입력하면 사용하자)


로컬 저장소(레포지토리) 상태 -> 원격 저장소(레포지토리)에 반영
git push origin 원격 브랜치명


원격 저장소(레포지토리) 상태 -> 로컬 저장소(레포지토리)에 반영 (먼저 git pull을 해서 코드 다운)
git pull origin 원격 브랜치명


원격 저장소 -> 로컬 저장소 복사
git clone 원격 저장소 주소


sourcetree - GIT GUT 툴 (설치해보자)





5bd47c3 (HEAD -> test) 작업4 완료
86add4e (origin/master, master) 작업3 완료  (원격에 반영하면 origin이 붙어있음)
