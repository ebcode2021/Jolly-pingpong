# Jolly-pingpong

## 1. 프로젝트 소개

> 핑퐁 게임과 채팅이 가능한 42Seoul 유저 기반의 웹사이트

"Jolly-pinpong" 프로젝트는 프론트엔드와 백엔드를 나누지 않고 유저, 채팅,게임을 각각 기능별로 나눠 구현하였습니다. 프론트엔드는 React와 Recoil을 활용하여 SPA 기반으로 구축되었으며, 백엔드는 NestJS 프레임워크를 이용하여 개발하였습니다. 이 웹사이트는 실시간 채팅과 pong 게임, 친구 관련 기능, 프로필 관리 등 다양한 기능을 제공합니다.

<img width="1613" alt="main" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/b779f76b-c669-489f-aef8-de0ed2e06167">

<br />
<img width="1091" alt="game play" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/3a6a49f8-a85a-4b32-9ddb-098aa9d1a518">

✈️ [기존 repository PR 구경하기 ](https://github.com/42-Jolly-pingpong/back-end)

## 2. 개발 기간

2023.08 - 2023.12

## 3. 개발 환경

**backend** : NestJS, PostgreSQL \
**frontend** : TypeScript, React, Recoil \
**tool** : Git, Github, Flowbite, Swagger, Figma, ERDCloud

<br />

## 4. 멤버 구성

<div align="center">
  <table style="font-weight : bold">
      <tr>
          <td align="center">
              <a href="https://github.com/get6">                 
                  <img alt="p1" src="https://avatars.githubusercontent.com/get6" width="80" />
              </a>
          </td>
          <td align="center">
              <a href="https://github.com/ebcode2021">                 
                  <img alt="p2" src="https://avatars.githubusercontent.com/ebcode2021" width="80" />            
              </a>
          </td>
          <td align="center">
              <a href="https://github.com/">                 
                  <img alt="p3" src="https://avatars.githubusercontent.com/yujelee" width="80" />            
              </a>
          </td>
		   <td align="center">
              <a href="https://github.com/minsukan">                 
                  <img alt="p4" src="https://avatars.githubusercontent.com/minsubro" width="80" />            
              </a>
          </td>
      </tr>
      <tr>
          <td align="center">sunhwang</td>
          <td align="center">eunson</td>
          <td align="center">yujelee</td>
		  <td align="center">minsukan</td>
      </tr>
	   <tr>
          <td align="center">PM 및 디자인</td>
          <td align="center">유저, 인증</td>
          <td align="center">채팅</td>
		  <td align="center">게임</td>
      </tr>
  </table>
</div>

## 5. 사용법

### 설치

```
$ git clone git@github.com:ebcode2021/Jolly-pingpong.git
$ cd Jolly-pingpong
```

### Backend

```
$ cd back-end
$ npm update
$ npm run start
```

### Frontend

```
$ cd front-end
$ npm update
$ npm run start
```

<br />

**🏁 서버 시작 후 사이트 접속** \
-> http://localhost:5173

## 6. 설계 및 디자인

**[ERD 설계]**

> ERDCloud를 활용하여 설계하였으며, 사이트에 공유된 타회사의 ERD를 참고하여 설계하였습니다.

<img width="1400" alt="erd" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/490c08e7-ba97-472f-bc82-ab759ee56fdb">

**[API 명세]**

> API 명세는 서버 시작 후 `localhost:5173/api` 에 접속해 swagger를 통해서도 볼 수 있습니다.

<img width="590" alt="api" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/61268bef-c749-4225-8320-d92b57874771">

## 7. 세부 기능 구현

구현 기능은 크게 4가지로 나눌 수 있으며, 구현 기능 옆에는 아이콘 🙋🏻‍♀️ 를 붙였습니다.

### 1. 로그인 / 회원가입 🙋🏻‍♀️

### 2. 유저

**2-1.프로필 수정** 🙋🏻‍♀️

**2-2.친구 관리** 🙋🏻‍♀️

**2-3. 친구 사이드바** 🙋🏻‍♀️

**2-4.2차 인증**

### 3. 게임

**3-1.게임 초대 기능** 🙋🏻‍♀️

**3-2.게임 플레이**

### 4. 채팅
