### Git

> > git은 분산버전관리 시스템의 일종이다
> >
> > 소스코드의 이력을 남기고 관리할 수 있다.

## 준비사항

윈도우에서 git을 쓰기위해서는 [Git for Windows · GitHub](https://github.com/git-for-windows)

컴퓨터에 처음 설치하는 경우 커밋을 하는 사람을 global로 설정해주어야함



```bash
$ git config --global user.name scool1661
$ git config --global user.email kimheewoon@naver.com


```

## 로컬저장소 활용하기

### 1. 저장소 생성

```bash
$ git init
```

![image-20191227140657229](imeges/image-20191227140657229.png)

* git 저장소를 생성하면  `.git`폴더가 생긴다.
* `(master)`는 현제작업중인 브랜치가 master라는 의미를 가지고 있다.



### 2.add

* working directory 작업공간 파일을 이동시키기 위해

```bash
$ git add aaaa
$ git add . #현제 디렉토리 모든파일
```



* add 전 상태

```bash
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Git.md

nothing added to commit but untracked files present (use "git add" to track)

```

* add 후 상태

```bash
$ git add .

HPE@DESKTOP-DFE1UPJ MINGW64 ~/Desktop/CLI (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Git.md


```

###	3.commit

* 이력을 남기기 위해서는 아래의 명령어를 입력한다.

```bash
$ git commit -m '커밋메세지'
[master (root-commit) f6b9a87] Git.md
 1 file changed, 48 insertions(+)
 create mode 100644 Git.md

```

커밋메시지는 해당 이력을 나타낼 수 있도록 작성하는 거이 중요하므로 항상 일편적으로 작성하자

커밋 내역은 아래의 명령어로 확인가능하다.

참조 

[커밋메시지]: https://www.google.com/search?ei=LZUFXt2KOIrr-QaBt6mwAQ&amp;q=%EC%BB%A4%EB%B0%8B%EB%A9%94%EC%84%B8%EC%A7%80&amp;oq=%EC%BB%A4%EB%B0%8B%EB%A9%94%EC%84%B8%EC%A7%80&amp;gs_l=psy-ab.3..0i10l4.2323.32059..32482...11.0..0.172.2425.17j7......0....1..gws-wiz.....0..0i13j0i131j0j0i131i67j0i10i30j0i5i30.YCxGRcKDRM4&amp;ved=0ahUKEwid1a_8itXmAhWKdd4KHYFbChYQ4dUDCAs&amp;uact=5	"참조"





```bash
$ git log

```

## 원격저장소 활용하기

> > 원격저장소를 제공하는 서비스는 다양하다

### 1. 원격저장소 설정하기 

```bash
$ git remote add origin 'github.url'
```

* 원격저장소를 `origin`이름으로 추가해줘
* 저장소 목록을 확인

```bash
$ git remote -v
origin  https://github.com/scool1661/test.git (fetch)
origin  https://github.com/scool1661/test.git (push)
```

### 2. push

```bash
$ git push origin master
```

* `origin`으로 설정된 url에 `master`브렌치로 `push`함
* 복습
* 

