# Jolly-pingpong

## 1. 프로젝트 소개

> 핑퐁 게임과 채팅이 가능한 42Seoul 유저 기반의 웹사이트

"Jolly-pinpong" 프로젝트는 프론트엔드와 백엔드를 나누지 않고 유저, 채팅,게임을 각각 기능별로 나눠 구현하였습니다. 프론트엔드는 React와 Recoil을 활용하여 SPA 기반으로 구축되었으며, 백엔드는 NestJS 프레임워크를 이용하여 개발하였습니다. 이 웹사이트는 실시간 채팅과 pong 게임, 친구 관련 기능, 프로필 관리 등 다양한 기능을 제공합니다.

**[메인 페이지]**

<img width="1613" alt="main" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/b779f76b-c669-489f-aef8-de0ed2e06167">

<br />

**[게임 플레이]**

<img width="1091" alt="game play" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/3a6a49f8-a85a-4b32-9ddb-098aa9d1a518">

<br />
<br />

✈️ [기존 repository PR 구경하기 ](https://github.com/42-Jolly-pingpong/back-end)

## 2. 개발 기간

2023.08 - 2023.12

## 3. 개발 환경

**backend** : NestJS, PostgreSQL \
**frontend** : TypeScript, React, Recoil \
**tool** : Git, Github, Flowbite, Swagger, Figma, ERDCloud

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

<br />

## 6. 설계 및 디자인

**[ERD 설계]**

> ERDCloud를 활용하여 설계하였으며, 사이트에 공유된 타회사의 ERD를 참고하여 설계하였습니다.

<img width="1400" alt="erd" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/490c08e7-ba97-472f-bc82-ab759ee56fdb">

<br />
<br />

**[API 명세]**

> API 명세는 서버 시작 후 `localhost:5173/api` 에 접속해 swagger를 통해서도 볼 수 있습니다.

<img width="590" alt="api" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/61268bef-c749-4225-8320-d92b57874771">

## 7. 세부 기능 구현

구현 기능은 크게 4가지로 나눌 수 있으며, 구현 기능 옆에는 아이콘 🙋🏻‍♀️ 를 붙였습니다.

### 1. 로그인 / 회원가입 🙋🏻‍♀️

```
- 비로그인 메인 화면
- 42 intranet OAuth 로그인 기능
- 회원가입 할 때, 프로필 이미지 업로드 기능, 닉네임 validate
- Passport 미들웨어를 사용하여 Oauth 2.0, JWT의 인증 절차 간소화
```

**[비로그인 메인 페이지]**
<img width="1300" alt="비로그인" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/02ee9a9b-8d4f-4e19-bb9b-e41acf73d236">

**[회원가입]**

<p align="center">
    <img width="454" alt="signUp" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/e4fe563e-9668-47cd-86d6-be37943cf753">
</p>

**[Oauth2 관련 코드]**

> 보안이 필요한 데이터는 env 파일로 별도 분리하여 관리하였습니다.

<img width="1466" alt="Oauth2관련" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/c39b10ee-66cc-4b97-9461-7174d6cf495e">

### 2. 유저

**2-1.프로필 수정** 🙋🏻‍♀️

```
- 프로필 이미지, 닉네임, 소개글 변경
- 이미지 업로드 크기 설정(5mb 제한)
```

<br />

**[프로필 편집]**

<img width="795" alt="edit profile" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/58df8af0-71c3-4d9d-96ab-ce21e95a80db">

<br />

**2-2.친구 관리** 🙋🏻‍♀️

```
-   친구 사이드바, 친구 리스트 보기
-   유저와의 관계를 enum으로 관리하여 프로필 페이지 구현
-   친구 요청, 삭제, 차단 기능
```

**[친구 목록 사이드바]**

<p align="center">
    <img width="896" alt="friend2" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/32cb8dc9-785e-4402-97af-2a4fe358f67e">
</p>

**[친구인 유저의 프로필]**

<p align="center">
    <img width="833" alt="나랑 친구" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/99e9c0fb-f764-4c62-bac9-ee2548af4cb1">
</p>

**[차단한 유저의 프로필]**

<p align="center">
    <img width="1583" alt="차단 유저" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/f200058d-14dd-41bb-a1ad-946776205f5a">
</p>

```
// profile-status.enum

export enum ProfileStatus {
MINE = 'MINE',
FRIEND = 'FRIEND',
REQUESTEDBYME = 'REQUESTEDBYME',
REQUESTEDBYOTHER = 'REQUESTEDBYOTHER',
BLOCKEDBYME = 'BLOCKEDBYME',
BLOCKEDBYOTHER = 'BLOCKEDBYOTHER',
UNKNOWN = 'UNKNOWN', // 탈퇴한 유저. 없는 유저. 내가 차단당한 유저일때
UNDEFINED = 'UNDEFINED',
}

```

**2-3. 유저의 프로필** 🙋🏻‍♀️

-   유저의 최근 경기 전적
-   친구 목록(본인 프로필 페이지 일 시, 친구 요청이 있을 경우 상단에 노출)
-   차단 목록, 차단 해제(본인 프로필에 한 함)

**[유저의 게임 전적]**
<img width="1621" alt="게임 전적" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/4cb0748d-a3af-4291-acb7-ad6f408950ba">

**[유저의 친구 목록]**

<p align="center">
    <img width="732" alt="friend1" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/2f704f36-307c-4b7d-8353-2b030431fa48">
</p>

**[유저의 차단 목록]**

<p align="center">
    <img width="662" alt="차단 목록" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/201f4929-d72d-4aac-a910-99799796ffd4">
</p>

### 3. 게임

**3-1.게임 초대 기능** 🙋🏻‍♀️

-   게임 초대 모달, 게임 시작 모달 디자인 구현

<img width="1606" alt="대전자" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/57cae919-56f3-4736-aad1-4e26590a8bc0">

<br />

**3-2.게임 플레이**

**[실제 게임 플레이]**

<img width="1091" alt="game play" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/3a6a49f8-a85a-4b32-9ddb-098aa9d1a518">

<br />

**[승패에 따른 결과 화면]**

<img width="1222" alt="승패" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/ec2ef710-3e89-4a84-8bd5-3a15823555de">

<br />

### 4. 채팅

**[DM 화면]**

<img width="1689" alt="Screenshot 2024-03-15 at 2 23 31 PM" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/ea397553-5af4-4211-9fdc-d1146c8a703c">

<br />

**[채팅 유저의 프로필 보기]**
<img width="1695" alt="Screenshot 2024-03-15 at 2 24 02 PM" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/8f762be7-aeff-4810-b6b5-19ee99a4c831">

<br />

**[메시지 보낼 상대 검색]**
<img width="1701" alt="Screenshot 2024-03-15 at 2 23 50 PM" src="https://github.com/ebcode2021/Jolly-pingpong/assets/84271971/034db068-8982-4581-8c41-cc83b69c47a6">
