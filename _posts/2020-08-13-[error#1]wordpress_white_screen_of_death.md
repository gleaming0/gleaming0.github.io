---
layout: post
title:  "워드프레스 복구 중 흰 화면이 뜨는 현상"
summary: "워드프레스 복구 중 죽음의 흰색 화면에 걸렸다."
author: aheunkim
date: '2020-08-13 09:41:00 +0900'
category: error
thumbnail: /assets/img/posts/error/thumbnail.jpg
keywords: wordpress, wordpress white screen of death, white screen of death, 죽음의 흰 화면
permalink: /blog/error/wordpress_white_screen_of_death/
usemathjax: true
---

백업해둔 파일을 복구 서버에 똑같이 복원하는 중에 문제가 생겼다.  
그냥 흰 화면만 뜨는 문제였다.
<br/>

검색을 해보니 *테마 또는 플러그인에 관한 문제*라고 하길래 내 블로그와 복구 서버의 테마·플러그인을 확인했다.  
확인해보니 복구 서버에는 블로그에 적용된 테마(generatepress)와 플러그인(elementor)이 하나씩 없었다.
<br/>

그래서 .sql 파일과 압축 파일을 지우고 다시 새로 만들어 복구 서버에 옮겼다.  
다시 백업 파일을 받아 테마와 플러그인이 똑같은지 확인하고 복구 서버에 접속했더니 해결되었다.