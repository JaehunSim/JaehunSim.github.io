---

layout: post
title: "Discord 롤 챗봇"
date: 2018-12-29 15:08:30
image: "/assets/images/league_logo.jpg"
sitemap: 
  changefreq: daily
  priority: 1.0
comments: true

---

# #Discord #디스코드 #RIOT_API #라이엇 API #전적검색 #Chatbot #챗봇

### 깃허브 주소: [RiotDiscordAPI](https://github.com/JaehunSim/RiotDiscordAPI)  

# 디스코드 롤 챗봇

python 으로 만든 discord bot입니다. 간략한 소스코드 설명입니다.

1. main.py: 디스코드 봇을 실행시키는 스크립트입니다. 명령어를 불러오고 작동하게 합니다.
2. discord_command.py: 명령어 함수가 들어있는 스크립트입니다. 반복 사용하는 함수는 따로 저장하고 불러와서 씁니다.
3. summoner_info.py: riotAPI를 다룰때 쓰는 스크립트입니다. 
4. util.py: db를 초기화시키거나, 경로 설정 및 불러오기를 할 때 쓰는 스크립트입니다. 토큰코드는 CREDENTIAL.py 에 저장해서 불러와야 합니다.

> discord 봇 토큰이나 riotAPI에 쓸 토큰의 경우 깃허브에 올리면 큰일납니다!! 

> 도용가능성 99%. 반드시 따로 저장하고 업로드 하지 맙시다.

이외에 discord_func.py, minDiffPartitioning.py는 명령어에서 자주 쓰이는 함수를 저장한 코드고  
discord_logging.py는 디버깅용 로그를 남길때 쓰는 스크립트입니다. 

사용한 라이브러리
1. numpy, pandas, sklearn 
2. discord

1번의 라이브러리는 https://winpython.github.io/ 에서 3.6.7버젼 다운받으면 있을거에요. 

[winPython](https://winpython.github.io/)이나 [Anaconda](https://www.anaconda.com/download/#windows) 통합 환경 파이썬을 이용하면 
대부분의 라이브러리가 설치되어서 나옵니다!  

2번의 경우 discord.py-rewrite.zip 파일을 다운받아서 다음 명령어로 설치해줍니다.  
`python -m pip install discord.py-rewrite.zip`

마지막으로 predict 명령어를 이용하기 위해 쓸 머신러닝 모델을 다운받아야 합니다. [링크](https://drive.google.com/open?id=1dAQR8RUW2D3CZ57UK5mlhw3LlBDIS_v0)  
이 파일을 db파일에 넣어줍시다!

---

위 봇은 아래와 같이 작동합니다.
  
`!guide` : 명령어 입력 방법을 출력해줍니다.
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/01.%20guide.gif)

`!dice` : 주사위 1~100 까지 굴리기
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/02.%20dice.gif)


`!voice` : 자신이 있는 채널 맴버들 출력
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/03.%20voice.gif)


`!rank` : !rank 아이디: Rank 확인하기
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/04.%20rank.gif)


`!most` : !most 아이디: MostN 확인하기. default: N=3, 기간=1
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/05.%20most.gif)


`!most N 기간` :  !most 아이디 N 기간: MostN 확인하기. 기간은 0~5 사이 지정. default: N=3, 기간=1
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/06.%20mostN.gif)


`!position` :  !position id1 id2 id3 id4 id5: 5명 팀일때 포지션 자동 분배하기
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/07.%20position.gif)


`!team` :  !team id1 id2 ... id10: 내전 10명일때 팀,포지션 자동 분배하기
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/08.%20team.gif)


`!setrank` : !setrank id1 rank number: id1의 rank를 수정합니다.
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/09.%20setrank.gif)


`!register` : !register id1: 자신의 discord 아이디를 id1으로 등록합니다.
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/10.%20register.gif)


`!register2` : !register2 id#tag id1: id#tag의 discord 아이디를 id1으로 등록합니다.
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/11.%20register2.gif)


`!predict` : !predict chmp1 chmp2 ... chmp10: 탑, 정글, 미드, 원딜, 서폿 순으로 두팀씩 조합을 제시해줬을 때, 어느 팀이 유리한지 예측해줍니다.
![](https://raw.githubusercontent.com/JaehunSim/RiotDiscordAPI/master/images/12.%20predict.gif)

---

## 사용법

### !명령어

명령어를 입력하면 게임에서(특히 내전) 필요한 기능을 이용할 수 있습니다.

### 명령어 모음

`guide`,`dice`,`voice`, `rank` , `most`, `position`, `team`, `setrank`, `register`, `register2`, `predict`
1. !dice : 주사위 1~100 까지 굴리기
2. !voice: 자신이 있는 채널 맴버들 출력
3. !rank 아이디: Rank 확인하기
4. !most 아이디 N 기간: MostN 확인하기. 기간은 0~5 사이 지정. default: N=3, 기간=1
5. !position id1 id2 id3 id4 id5: 5명 팀일때 포지션 자동 분배하기
6. !team id1 id2 ... id10: 내전 10명일때 팀,포지션 자동 분배하기
7. !setrank id1 rank number: id1의 rank를 수정합니다.
    ex). !setrank 타푸고양이 PLATINUM III
8. !register id1: 자신의 discord 아이디를 id1으로 등록합니다.
9. !register2 id#tag id1: id#tag의 discord 아이디를 id1으로 등록합니다.
10. !predict chmp1 chmp2 ... chmp10: 탑, 정글, 미드, 원딜, 서폿 순으로 두팀씩 조합을 제시해줬을 때, 어느 팀이 유리한지 예측해줍니다.

---

## 디스코드 앱 설정법

1. 디스코드 앱부터 만듭니다.(https://discordapp.com/developers/applications/)

2. 봇을 만들게 되면 BOT_CLIENT_ID로 자신의 봇을 채널에 추가할 수 있습니다. 밑에서 설명 더 합니다!

3. Settings - Bot 메뉴에서 TOKEN키를 확인할 수 있습니다.

CREDENTIAL.py 에 DISCORD_TOKEN 명으로 해당 토큰값을 저장해줍시다!

4. 봇을 자신의 채널에 초대하기
https://discordapp.com/oauth2/authorize?client_id=YOUR_CLIENT_ID&scope=bot
YOUR_CLIENT_ID을 자신의 것에 맞게 변경하고 들어가면 됩니다.

---

## 라이엇 API 설정법

1. 라이엇 개발자 포털에 들어갑니다. (https://developer.riotgames.com/)

2. DEVELOPMENT API KEY를 발급 받습니다. reCaptcha 버튼을 누르시고 REGENERATE API KEY를 누르시면 돼요.

3. 키를 복사하고 CREDENTIAL.py 에  RIOT_API_KEY명으로 해당 토큰값을 저장해줍시다!

> RIOT API 토큰은 24시간 내로 만료되기 때문에 주기적으로 REGENERATE 하거나 APP 신청을 해서 반영구적 API KEY를 얻을 수 있습니다.

---

## 챗봇 24시간 구동시키기 (feat AWS EC2)

아마존 웹 서비스(AWS)를 처음 가입하게 되면 프리티어로 1년간 AWS의 다양한 기능을 이용할 수 있어요.  

우리는 그중에서 EC2(Elastic Compute Cloud) 기능을 이용해보려고 해요.  

제가 간단히 이해한 바로는 CPU - RAM - SSD용량 을 다양하게 조합해서 컴퓨터를 구성한 후(instance라고 불려요) 

필요한 때에 필요한 만큼 쓸 수 있는 기능이에요.  

우리는 최소사양이면 챗봇을 가동시킬 수 있어서 프리티어급 EC2면 충분해요!  

세팅법은 복잡하니 [링크](http://blog.poin2.com/2016/02/%ED%81%AC%EB%A1%AC%EB%B6%81%EC%9C%88%EB%8F%84%EC%9A%B0%EC%82%AC%EC%9A%A91/)에서 확인!  

EC2를 설치하셨으면 똑같이 파이썬, 소스코드를 받고 실행시키면 돼요.  

프리티어가 쓸 수 있는 t2.micro 를 이용한다면 1년간 24/7 무료로 챗봇을 구동시킬 수 있어요.  

EC2 instance는 반드시 하나만 생성하고 더 만들면 stop이나 terminate(완전 삭제)를 하셔야 과금이 안돼요.  

---

### 소스 설명

```
#main.py: 봇을 실행시킬때 쓰는 소스입니다. 
1. 로그 기록을 시작.
2. 봇 command_prefix 정의 # "!"으로 지정했음
3. 봇 command 작성
4. 디스코드 토큰으로 봇 실행

#discord_command.py: 봇에 명령어를 추가하고 싶을 때 여기에 넣으면 됩니다.
1. dice
2. guide
3. register
  1. discordNickNameChange.csv 파일에 아이디#tag와 arg1을 저장
  2. 이미 db에 아이디#tag가 있으면 확인후 수정, 없으면 생성
4. register2
  1. 3번에서 남의 아이디까지 수정할 수 있도록 기능 확장 (class로 구현하면 확장이 편했을 것 같다.)
5. voice
  1. discordNickNameChange.csv에서 키가 있다면 해당 값 출력
  2. 없으면 기본 닉네임 출력
6. most
7. rank
8. setrank
  1. summonerNameData.csv에서 티어 부분 수동 수정
9. position
  1. 플레이어들의 전적 검색을 통해 주요 플레이 포지션을 구해온다.
  2. 선호 포지션 TOP2를 각각 찾는다.
  3. 선호 포지션에 배치될 수 있게 각 플레이어들의 포지션을 배치해준다.
10. team #position과 겹치는 부분이 있다. 
  1. 10명의 플레이어들을 먼저 티어에 맞게 나누고 (min_diff_sets, getUniqueDivSets)
  2. 선호 포지션에 따라 플레이어들의 포지션을 배치해준다.
  3. 3가지 경우를 출력해준다.
11. team2 #15명일때 5,5,5 씩 나누는 방법
12. predict
  1. 예측에 필요한 모델, 데이터 가공에 필요한 데이터를 불러온다. 각각 RF_MODEL, ptpDFList다.
  2. 10명의 챔피언이 탑, 정글, 미드, 원딜, 서폿 *2 순으로 들어왔을 때 이를 가공한다.
  3. 가공한 데이터를 모델에 넣고 승리확률을 예측한다. #winRate = RF_MODEL.predict_proba(data4)[:,1]
  
#discord_func.py: 
1. updateSummoner: 소환사 이름을 API를 통해 검색하고 rank를 받아온다. 이를 summonerNameData에 저장한다.
2. getDivTeamList: 포지션, 랭크를 고려해 10명의 플레이어들을 나누는 방법

#summoner_info.py: 
1. getDataFromURL
2. getSummonerId
3. getSummonerRank
4. getRankScore
5. getRankLog
6. getMostN
7. getPositionPreference
8. getChampionPlayedList
9. predictPosition

#minDiffPartitioning.py
팀을 나눌때 쓰인다.

#util.py
db를 초기화시키거나, 경로 설정 및 불러오기를 할 때 쓰는 스크립트입니다. 토큰코드는 CREDENTIAL.py 에 저장해서 불러와야 합니다.

```

---

추가 태그

# #승부 예측 #Machine Learning #ML #Random Forest Classification

---

##### 질문이나 안되는 기능은 이슈에 적어 주세요.
