# 홈페이지에 “뉴스” 포스팅 하는법
## 준비물
1. `.jpg`이미지 파일, (너무 크면 사이트가 터져요... 대충 가로 길이 10cm로 맞추면 되는듯)
2. `.md` 마크다운파일

## 이미지 올리기
블로그 포스팅용 이미지는 한곳으로 통일합니다.  
`snuxlab.github.io/website/assets/images/news/` 디렉토리를 이용합니다. 
(디렉토리 안에 개인폴더를 만드셔도 됩니다)   
올릴 이미지의 파일명은 날짜 + 몇번째 사진인지로 표기하기  
ex) `2019-11-22-01.jpg` or `2019-10-23-03.jpg`  

**중요: 세로로 긴 직사각형 이미지는 가로 길이를 400px로 맞춥니다! (세로는 무관)**
**배너처럼 가로로 엄청 긴 이미지는 딱히 문제 없지만, 이미지 크기만 좀 신경써주세요**

깃허브에 로그인해서 업로드하면 됩니다.  

## 글 작성 (마크다운)
```
---
layout: post
title: 'UX Lab인데 사진찍기가 과제라고?'
author: UXLab
categories: 
image: assets/images/news/2019-11-22-01.jpeg
---
```

글 작성에는 항상 위 헤더가 있어야한다.  
`layout: post`는 이 파일이 “post” 형태인걸 알려줌  
`title`에는 적고 싶은 제목 쓰기  
`author`는 두가지 경로로 설정이 가능함.
1. `UX Lab`으로 글쓰기: `author` 부분에 `UX Lab`으로 적으면 됨
2. 자기 이름으로 글쓰기: 자기가 원하는 이름을 `website/_config.yml`파일의 `# Authors` 부분에 자기 이름을 추가한다. 내어쓰기 되어있는 부분에는 스페이스 없이 만든후, `name` 및 `display_name` 을 쓰면 된다. `display_name`이 웹사이트 상에 보이는 이름이다.

`image`는 대표 이미지 경로로, github 디렉토리에서, `assets/images/news/파일이름.jpg` 형태로 하면된다.  

아랫 `---` 밑에다가 원하는 내용을 쓰면 됩니다.  

본문 이미지 삽입 예시:  
`<img src="{{site.baseurl}}/assets/images/news/파일명.jpg" style="float: left; margin-right: 5%;">`  
`<img src="{{site.baseurl}}/assets/images/news/개인디렉토리/파일명.jpg" style="float: left; margin-right: 5%;>`  

예시의 `style` 부분은 작은 이미지를 쓰실때 저대로 꼭 써주세요. 
css 스타일링 가능하신분은 각자 알아서 이쁘게...

위에 header 부분의 `image`는 대표사진임 (메인페이지에서 보이는 미리보기)  

링크 삽입 방법
[링크 제목 예: 슬라이드쉐어 링크입니다](https://www.google.com)

파일 저장은: `날짜-제목.md`  
파일명에 날짜를 써줘야 홈피에서 퍼블리쉬 날짜가 찍힘.  
다른 날짜로 퍼블리쉬하고 싶으면 파일명의 날짜를 바꾸면 됨.  
예시: `2019-11-22-zero-depth.md`  

## 글 업로드
업로드 경로는  
`_posts` 폴더안에 넣으면 됩니다.


