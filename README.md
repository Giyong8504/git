# git 사용방법
-------------

### 1. 계정 연결 준비물
- 이메일 주소 : gitHub 가입 했던 이메일 주소
- 사용자 이름 : Giyong8504
- 폴더 경로 : C:\Users\KGY\study_java\자바\git
<br>

### 2. 계정 동기화
```
git config --global user.name "github 사용자 이름"
git config --global user.email "github 이메일 주소"

참고) 나만 쓰는 컴퓨터가 아닐 경우 -> --global 제거
git config user.name "github 사용자 이름"
git config user.email "github 이메일 주소"

참고2) user 삭제
git config --unset user.name
git config --unset user.email

git config --unset --global user.name
git config --unset --global user.email
```
<br>

### 3. 로컬 레포지토리 생성
```
cd C:\Users\KGY\study_java\자바\git
git init
```
<br>

### 4. 원격 레포지토리 연결하기
![image](https://github.com/Giyong8504/git/assets/128211712/ba304c2f-243d-4db4-82c8-eaa539b38717)

```
git remote add origin 원격 레포지토리 주소 : 원격 저장소(레포지토리) 주소 추가
git remote set-url origin 원격 레포지토리 주소 : 기존 주소 변경
```
<br>

### 5. 스테이징 단계
```
git add 파일명, 파일경로
git add . (모든파일)
```
<br>

### 6. 스냅샷 단계 (commit) - 버전 기록 : 복구할 시점 만들기
```
git commit -m "작업 내용 메모"
```
<br>

### 7. 원격 저장소에 반영 ( 로컬 -> 원격 )
```
git push origin 원격 브랜치명
```
<br>

### 8. 로컬 저장소에 반영 ( 원격 -> 로컬 )
- 작업 전 확인하고 pull해서 코드 다운.
```
git pull origin 원격 브랜치명
```

- 참고) 원격 -> 로컬
```
git clone 원격 저장소 주소
```

---------------
# 브랜치
### 1. 커밋로그
```
git log
git log --oneline : 로그를 한줄로 짧게 확인
```
![image](https://github.com/Giyong8504/git/assets/128211712/b0f2d476-8d0d-4451-96b8-4d7aaa111c39)
- HEAD - master (현재 작업중인 branch)
- origin/master (origin은 원격을 의미)
<br>

### 2. 버전 관리
```
git checkout 커밋 ID
git checkout - : 직전 단계로 복구
```
<br>

### 3. 브랜치 사용
- master 브랜치 - 기본 브랜치
```
git branch : 현재 생성된 브랜치 목록
git branch 브랜치명 : 현재 브랜치의 소스와 함께 브랜치가 생성 (선택된 브랜치 기준 파일복사)
git checkout 브랜치명 : 브랜치로 이동
git branch -d 브랜치명 : 브랜치 삭제 
	   -D 브랜치명 : 브랜치 강제 삭제 (위 에러시 안될 경우)
git checkout -t origin/브랜치명 : 원격 브랜치 가져오기
```
<br>

### 4. 브랜치 병합 (테스트 후 master에 병합)
- 병합 주의) 테스트 브랜치 하나 생성 -> 다른 작업을 병합 -> 테스트 완료 -> 마스터에 병합
```
git merge 브랜치명 - 현재 브랜치에 브랜치명의 브랜치를 병합
```

### 5. commit 되돌리기
```
git reset --soft HEAD~1 : 한칸 앞의 commit 으로 되돌리기
git reset --soft HEAD~숫자 : 원하는 commit으로 되돌리기
```

##### 참고) 명령어
```
cls : 작업내용 삭제
cd 폴더명 : 경로이동
cd .. : 이전 폴더이동
dir/w : 해당 폴더 자료 확인
```
