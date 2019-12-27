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



## 2.add

* working directory 작업공간 파일을 이동시키기 위해

```bash
$ git add aaaa
$ git add . #현제 디렉토리 모든파일
```



* add 전 상태