# unity 3d car runner : Police and thief
---

### 게임 실행 화면
![game1](/image/game1.png) <br>
[그림1 : 게임 실행 중 화면, 맵화면 양쪽에 있는 배경을 랜덤하게 생성, 도로를 사용자 기준 앞뒤로 이동시킴 ] <br>
![car](/image/car.png) <br>
[그림2 : 컨셉에 맞는 자동차, 게임 실행중 경찰차가 도둑차를 잡으면 게임이 이김으로 끝남] <br>
![game2](/image/game2.png) <br>
[그림3 : 게임 실행 첫 화면] <br>
![game3](/image/game3.png) <br>
[그림4 : 게임 일시정지 화면] <br>
![game4](/image/game4.png) <br> 
[그림5 : 점수 기록 화면] <br>
![game5](/image/game5.png) <br>
[그림6 : 순위 화면, sqllite를 사용하여 순위를 저장, 로컬데이터베이스] <br>
![sqllite](/image/sqllite.png) <br>
[그림7 : firefox 확장프로그램 사용으로 DB생성및 관리] <br>
![item1](/image/item1.png) ![item2](/image/item2.png) ![item3](/image/item3.png) ![item4](/image/item4.png) ![item5](/image/item5.png)
[그림8 : 아이템들] <br>
![car2](/image/car2.png) <br>
[그림9 : 별아이템을 먹고 빨라진 도둑자동차] <br>


## 1. 착안점
기존의 러너게임은 코인을 먹고 점수를 올리며 장애물을 피하는 게임이 과반수이다. 
뭔가 간단하기 심플한 러너게임에 특별함을 주면 어떨까? 라는 생각을 가지고 개발에 몰입하기 시작함. 
기존의 게임은 1인용 이지만 2인용으로 러너게임을 만들어봄. 
2인용으로만 할수있는 시스템을 생각(ex 경쟁전, 싸움, 술래잡기, 경찰과 도둑 등) 이때 경찰과 도둑이 제일 재밌을거 같다는 생각에 제작을 마음먹기로 했음. 
서버를 통해서 2인용이 아닌 한컴퓨터로 2조작키를 사용하므로 플레쉬게임 느낌을 줌. 

## 2. 차별성
기존의 1인용 러너게임에서 2인용게임을 만든 것이 특징입니다. 
또한 2명의 플레이어가 무한이 달리는 것이 아니라 한플레이어가 도망가는 플레이어를 잡으면 게임이 끝나는 컨셉으로 만들었습니다. 
아이템은 기존의 게임 카트라이더라는 게임이 있는데 그 게임에 착안을 둔 아이템도 있지만 경찰차가 벽아이템을 먹고 사용하면 자기 멀리 앞에 멀리 있는 거리에 벽을 세워 도둑차의 진행을 방해하고 도둑차 또한 이와 비슷한  아이템을 먹어 사용하면 자기가 지나가는 그 위치에 벽을 둠으로 경찰차의 주행을 방해하는 새로운 아이템을 만들었습니다. 

## 3. 아쉬운점
일단 한화면에 2인용으로 플레이 하는 것이 아쉬웠다. 
네트워크서버를 두어 멀티플레이 가능하게 했으면 했는데 동기화문제라던지 서버구축이라던지 시간상 구현하지 못한 것이 아쉬웠다. 
두번째로는 그냥 한 직선도로만 구현했다는 것이 아쉬웠다. 
자동으로 길생성해주는 에셋이 있지만 그것을 몰라서 이용 못한 것이 아쉬웠다. 
좀 더 랜덤으로 길을 생성하고 직진뿐만아니라 곡선이나 방향이 있는 길을 생성하고 그에 따라 주변 환경도 바뀌면 더 임펙트 있었을 텐데 너무 아쉬운 것 같다. 

## 4. 해결해야 할 점
시간이 급박하여 몇몇 사항을 해결하지 못하였다. 
첫번째로는 도로의 양사이드 끝을 벗어 날 수 있다라는 것이다. 
또한 도로가 경찰차를 중심으로 만들어지기 때문에 도둑이 경찰차 앞의 일정거리 이상 더 나아가면 없는 도로에서 주행할 때가 있다. 
이시점을 계산해 이경우 도둑이 이겼다고 게임을 끝내야 하는데 시간상 구현하지 못하였다. 
이렇게 해서 이부분과 전에 아쉬운 부분을  좋합하여 추후에 보완하고 개선할 예정입니다.
