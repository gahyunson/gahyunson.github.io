---
layout: post
title:  "Web structure, HTTP, ..."
date:   2023-06-30
categories: HTTP WEB
---
## Web Structure
프로젝트를 진행하면서 클라우드에 웹을 업로드할 때 생기는 일들에 대해 좀 더 자세히 알고싶어 HTTP에 대해서 찾아보게 되었다.
### HTTP(is Protocol)

1. **Socket** 수준에서 만들어짐 = stream data = 문자열로 이루어짐 (테이프처럼)
2. **TCP**의 경우 socket을 잘게 잘라서 segment(라고하는) 하나를 **incapsulation** 한다. 이를 network로 만들어서 packet 형태로 TCP/IP 로 전송한다

<aside>
<img src="https://www.notion.so/icons/star-of-life_gray.svg" alt="https://www.notion.so/icons/star-of-life_gray.svg" width="40px" /> web은 아래와 같은 통신을 가진다.

</aside>

### Web Client → Web Server

경우1. TCP or IP 연결 후, HTTP session create

경우2. HTML doc. request (GET) 

### Web Server → Web Client

server에서 HTML doc. responce, 연결 종료

### Web is …

1. HTML = document
2. HTTP = HTML을 전달하는, stateless 인.

### Structure Layers

- PC : Client , browser
- Internet
- Server : Web
- Was : MVC architecture (Model, View, Control)
- DB

## Networking Document

1. *:: PC ← Internet → Server*
`TCP/IP` 이용한 connect, `HTTP` network 
HTML resource 통신

2. *:: PC - Internet → Server - Internet → PC*
`http.request.method == GET` 으로 document 보기
- GET은 download 개념이다
- Process : HTML(+ css) 구문분석 : text, tag .split() → tag 해석해서 내용 렌더링 
→ static(정적) document(Java Script)
- **개발시 설계원칙**이 생기면서 발전하는 파일 구조
`HTML` → `HTML, css, jpg` → `HTML, css, jpg, J.S`
- static document + (Mocha script → Live script → ) **Java script → dynamic document**
1. *:: PC - Internet → Server → Was → DB → Server → PC*
`http.request.method == POST` 으로 로그인하기 
- Was 를 통한 dynamic page(document)
- POST → 양방향 상호작용 → **상태전이** 생김 = 기억을 해야함 → Client = cookie , Server = DB
- 원격지 사용자 입력(ID, PASSWORD…) → Was 처리 → DB에서 데이터 확인 
→ found / not found → Hi! Gahyun! / Who are you?

![0701](/Users/gahyunson/Work/GahyunSon.github.io/assets/images/0701.png)
