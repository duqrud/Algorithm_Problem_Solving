# GIT 관련, pip requests

git config --global user.name "username"
git config --global user.email "email"
pwd
git init

1. git status
2. git add .
3. git commit -m "msg"

git remote add orgin (https://~위치~)
git remote -v

4. git push origin master

### 가상환경

1. 프로젝트 폴더 생성
2. .gitignore => venv/
3. python -m venv venv
4. source ../../activate
  (vi .gitignore)
5. pip install django
  ....
6. pip freeze > requirements.txt
7. pip install -r requirements.txt
  (이 안에 있는걸 기반으로 인스톨)

source venv/bin/activate

source venv/Scripts/activate

가상황경 나갈땐 : deactivate

git log
git reset 일련번호 6자리 --hard
git revent 일련번호 6자리
:wq 입력
git branch 이름  (다른 미래 만들기)
git checkout 이름
git checkout master(돌아갈 이름, 원래로 돌아가기)
master에서 git merge 이름
삭제할땐 git branch -D 이름



## pip requests

pip install requests (파이썬에서 엑시오스처럼 특정 요청을 도와줌)
import requests
API_URL = ""
response = requests.get(API_URL)
jsonData = response.json()
return render(request, 'test.html')
for item in jsonData:
    article = Article()
    article.title = item.get('title')
    article.content = item.get('body')
    article.save()

shift+alt+f 누르면 json 이쁘게나옴