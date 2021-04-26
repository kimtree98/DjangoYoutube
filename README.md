# DjangoYoutube
장고를 활용한 유튜브 개인 영상 모음 사이트

* https://youtubestorage.herokuapp.com/video

## 구현내용

  - 회원가입/로그인/로그아웃 기능 구현
  - video create/read/delete
  - Ajax를 이용한 비동기적 '좋아요' 기능 구현
  - 카테고리별로 video 분류/'좋아요' Ascending order로 정렬해서 보여주기
  - javascript로 비디오 로딩 지연시 '로딩중' 메세지 띄우기
  - 나의 비디오/좋아요한 비디오 관리 페이지 제공
  - PostgreSQL 연동
  - 저장된 유튜브 영상의 정보 (제목, 업로더, 언어 등) 제공


## 사용법

### Local에서 실행 시
```sh
$git clone https://github.com/kimtree98/DjangoYoutube.git
$cd DjangoYoutube/MyYoutubeStore/MyYoutubeStore/
$python -m venv venv (Python 가상환경 설치)
$pip install -r local_requirements.txt (구동에 필요한 Library 설치)
$python manage.py migrate(Django 실행시 migration 과정)
$$python manage.py runserver --settings=MyYoutubeStore.local_settings (Local Setting 파일로 서버 구동)
```
* 중요
<br>'YoutubeAPI' 키와  'Django SecretKey' </br> 를 수정하여 사용
```sh
DjangoYoutube/MyYoutubeStore/MyYoutubeStore/settings.py
```
<br>'SECRET_KEY'</br>와 <br>'YOUTUBE_DATA_API_KEY'</br> 수정 후 사용
<br>
(참고: https://wayhome25.github.io/django/2017/07/11/django-settings-secret-key/, 
https://developers.google.com/youtube/v3/getting-started?hl=ko )




셋팅 후 https://127.0.0.1:8000/video 링크로 접속 가능

### Heroku를 활용하여 호스팅 하기

https://egg-money.tistory.com/115 참고

## 실행환경
* Windows 10
* Python 3.8.1

## 참고 자료
* https://github.com/JisunParkRea/my_djangotube (Django 활용 사이트 구축 방법)
* https://youtu.be/lc2KvFbbfAQ (Django에서 YoutubeAPI 활용 관련)





