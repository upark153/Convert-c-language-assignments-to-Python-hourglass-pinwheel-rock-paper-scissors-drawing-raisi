# Convert-c-language-assignments-to-Python
![image](https://user-images.githubusercontent.com/115389450/233531413-c1f660ac-e7ae-412b-8bcf-c2f379d9e741.png)
```
from random import choice
players = ['연재','의용'] // 리스트에 선수 넣기
print(players) // 시험 출력 해 보기

teamJ = [] // 재일 팀 빈 리스트
teamS = [] // 성일 팀 빈 리스트
playerJ = choice(players) // 재일편에 설 선수를 뽑는다
print(playerJ) // 시험 출력
teamJ.append(playerJ) // 재일 팀 빈 리스트에 뽑힌 재일팀 선수를 넣는다
players.remove(playerJ) // 선수들 중 뽑힌 재일팀 선수를 리스트에서 뺀다
print('남은 플레이어: ', players) 

playerS = choice(players) // 성일팀에 설 선수를 뽑는다
print(playerS) // 시험 출력
teamS.append(playerS) // 성일팀 빈 리스트에 뽑힌 성일팀 선수를 넣는다
players.remove(playerS) // 선수들 중 뽑힌 성일팀 선수를 리스트에서 뺀다
print('남은 플레이어: ', players) // 남은 선수는 없다. 다 뽑힘.

print('재일 팀: ', teamJ) 
print('성일 팀: ', teamS)
```
![image](https://user-images.githubusercontent.com/115389450/233531474-77b5f938-8592-4a6c-a361-c54e667c8a7e.png)
```
teamJwin = 0 # 재일팀 승리 회수
teamSwin = 0 # 성일팀 승리 회수
cnt = 0 # 전체 게임 회수

while teamJwin != 10 and teamSwin != 10: # 재일팀승리회수 10번이 아니고, 성일팀 승리회수 10번이 아닐때까지 반복
    cnt = cnt + 1
    print('가위바위보 시작 ! %d번째 판 !\n' % cnt)
    teamJ = randint(0, 2) #0은 가위, 1은 바위, 2는 보
    teamS = randint(0, 2)
    while teamJ == teamS:
        print('비겼습니다. 재경기!\n')
        teamJ = randint(0, 2)  # 0은 가위, 1은 바위, 2는 보
        teamS = randint(0, 2)
    if teamJ > teamS:
        if teamJ == 2 and teamS == 0: # 재일팀 보, 성일팀 가위
            print('성일팀 승리!\n')
            teamSwin += 1
        else: # 재일팀 보(2) 성일팀 바위(1), 재일팀 바위(1), 성일팀 가위(0)
            print('재일팀 승리!\n')
            teamJwin += 1
        teamJr = teamJwin/cnt*100
        teamSr = teamSwin/cnt*100
        print('재일팀 %d회' % teamJwin, '성일팀 %d회' % teamSwin)
        print('재일팀 승률 %.1f%%' % teamJr, '성일팀 승률 %.1f%%' % teamSr)
    else:
        if teamJ == 0 and teamS == 2: #재일팀 가위, 성일팀 보
            print('재일팀 승리 !\n')
            teamJwin += 1
        else: # 재일팀 가위(0) 성일팀 바위(1), 재일팀 바위(1) 성일팀 보(2)
            print('성일팀 승리 !\n')
            teamSwin += 1
        teamJr = teamJwin / cnt * 100
        teamSr = teamSwin / cnt * 100
        print('재일팀 %d회' % teamJwin, '성일팀 %d회' % teamSwin)
        print('재일팀 승률 %.1f%%' % teamJr, '성일팀 승률 %.1f%%' % teamSr)
if teamJwin == 10:
    print('재일팀 승리! 축하합니다.')
else:
    print('성일팀 승리! 축하합니다.')
```
![image](https://user-images.githubusercontent.com/115389450/233531511-84f3b8cd-f68d-4c2a-a3a8-adbe88eb2b07.png)
```
from random import choice
from random import randint
players = ['연재','의용']
print(players)

teamJ = []
teamS = []
playerJ = choice(players)
print(playerJ)
teamJ.append(playerJ)
players.remove(playerJ)
print('남은 플레이어 :', players)

playerS = choice(players)
print(playerS)
teamS.append(playerS)
players.remove(playerS)
print('남은 플레이어 : ', players)

print('재일팀 : ', teamJ)
print('성일팀 : ', teamS)

teamJwin = 0 # 재일팀 승리 회수
teamSwin = 0 # 성일팀 승리 회수
cnt = 0 # 전체 게임 회수

while teamJwin != 10 and teamSwin != 10: # 재일팀승리회수 10번이 아니고, 성일팀 승리회수 10번이 아닐때까지 반복
    cnt = cnt + 1
    print('가위바위보 시작 ! %d번째 판 !\n' % cnt)
    teamJ = randint(0, 2) #0은 가위, 1은 바위, 2는 보
    teamS = randint(0, 2)
    while teamJ == teamS:
        print('비겼습니다. 재경기!\n')
        teamJ = randint(0, 2)  # 0은 가위, 1은 바위, 2는 보
        teamS = randint(0, 2)
    if teamJ > teamS:
        if teamJ == 2 and teamS == 0: # 재일팀 보, 성일팀 가위
            print('성일팀 승리!\n')
            teamSwin += 1
        else: # 재일팀 보(2) 성일팀 바위(1), 재일팀 바위(1), 성일팀 가위(0)
            print('재일팀 승리!\n')
            teamJwin += 1
        teamJr = teamJwin/cnt*100
        teamSr = teamSwin/cnt*100
        print('재일팀 %d회' % teamJwin, '성일팀 %d회' % teamSwin)
        print('재일팀 승률 %.1f%%' % teamJr, '성일팀 승률 %.1f%%' % teamSr)
    else:
        if teamJ == 0 and teamS == 2: #재일팀 가위, 성일팀 보
            print('재일팀 승리 !\n')
            teamJwin += 1
        else: # 재일팀 가위(0) 성일팀 바위(1), 재일팀 바위(1) 성일팀 보(2)
            print('성일팀 승리 !\n')
            teamSwin += 1
        teamJr = teamJwin / cnt * 100
        teamSr = teamSwin / cnt * 100
        print('재일팀 %d회' % teamJwin, '성일팀 %d회' % teamSwin)
        print('재일팀 승률 %.1f%%' % teamJr, '성일팀 승률 %.1f%%' % teamSr)
if teamJwin == 10:
    print('재일팀 승리! 축하합니다.')
else:
    print('성일팀 승리! 축하합니다.')
```
![image](https://user-images.githubusercontent.com/115389450/233531550-ebd41666-f68c-470b-923d-fec0a1342459.png)
```
import random

poketball = ['피카츄', '파이리', '꼬북이', '메타몽']
final = []
metafinal = []

for i in range(1, 101): // 100번 반복
    poketmon = random.choice(poketball) // 포켓볼 리스트에서 랜덤으로 뽑는다
    print(f'{i}번째 포켓몬! {poketmon}') // 출력
    final.append(poketmon) // final 리스트에 뽑힌 포켓몬들 넣어줌.
print("피카츄 :", final.count('피카츄')) // 리스트 개수 세기
print("파이리 :", final.count('파이리'))
print("꼬북이 :", final.count('꼬북이'))
print("메타몽 :", final.count('메타몽'))
""" // 실험 삼아 코드 확인 주석처리
meta = []
for word in final:
    if '메타몽' in word:
        meta.append(word)
print(meta)
""" // 실험 삼아 코드 확인 주석처리
for i in range(1, final.count('메타몽')+1): // n-1까지 반복되므로 +1을 더해줌
    meta = random.choice(poketball) 
    print(f'{i}번째 메타몽이 진화했다! {meta}')
    metafinal.append(meta)
print("메타몽 변신 > 피카츄 :", metafinal.count('피카츄'))
print("메타몽 변신 > 파이리 :", metafinal.count('파이리'))
print("메타몽 변신 > 꼬북이 :", metafinal.count('꼬북이'))
print("메타몽 변신 > 메타몽 :", metafinal.count('메타몽'))

print("메타몽 진화 이후 최종 포켓몬은 몇명이야?")
pica = final.count('피카츄') + metafinal.count('피카츄')
pail = final.count('파이리') + metafinal.count('파이리')
kkobo = final.count('꼬북이') + metafinal.count('꼬북이')
meta = metafinal.count('메타몽')

print("피카츄 : ", pica, "파이리: ", pail, "꼬북이 : ", kkobo, "메타몽 : ", meta)
```
![image](https://user-images.githubusercontent.com/115389450/233531622-1434ac29-ba09-480a-b9ad-3435fd910d7e.png)
![image](https://user-images.githubusercontent.com/115389450/233531652-117e1452-e033-4834-9fb3-c776c8633915.png)\
```
from random import randint
import time

print("류의 애칭을 입력 해 주세요 : ")
ryw = input()
print("류의애칭 : ", ryw)
print("류의 짝꿍 애칭을 입력 해 주세요 : ")
rywPartner = input()
print("류 짝꿍의 애칭 : ", rywPartner)


cnt = 1
fishbowl = 2
finalChild = 0
time.sleep(2)
child = randint(1, 10)
female = child / 2
print("류 부부가 낳은 금붕어 :", child)
while 1:
    time.sleep(2)
    cnt = cnt + 1
    female *= randint(1, 10)
    print("%d회째 자식 낳는중 " % cnt, "낳은 자식 : %d명" % female)
    if female<=10:
        dieChild = randint(1, 5)*2
    else:
        dieChild = randint(1, 10)*2
    print("%d회째 " % cnt, "죽은 자식: %d명" % dieChild)
    finalChild += female - dieChild
    print("%d회 :" % cnt, "낳은 자식 : %d" % finalChild)
    fishbowl += finalChild+child
    if fishbowl > 1000:
        print("어항을 수용할 수 있는 물고기 수가 넘었습니다.")
        print("1000마리를 넘긴 물고기들은 죽습니다 ㅜ")
        break
```
![image](https://user-images.githubusercontent.com/115389450/233531717-f881e6dd-ee12-40ba-b111-9f8d5586d00d.png)
![image](https://user-images.githubusercontent.com/115389450/233531750-6c957d50-c946-40cc-9e91-4ae54194aa3a.png)
```
import pprint
machine = {'cola': 1200, 'spaceCola': 1900, 'zeroCola': 1200,
           'sprite': 1100, 'hwenta': 900, 'pepper': 1100, 'monster': 1800,
           'poweraid': 1900, 'nestea': 1600, 'vitaminWater': 2100,
           'minimade': 1700, 'zoziaCoffe': 900, 'ambasa': 900, 'matecha': 1700}

sum = 0
money = input("음료수를 사려면 돈을 넣어 주세요: ")
money = int(money)
while 1:
    pprint.pprint(machine)
    if money < sum:
        print("선택한 음료가 넣은 돈을 초과해서 음료수를 사지 못합니다.")
        break
    leftMoney = money - sum
    print('현재 잔액은 %d 남았습니다' % leftMoney)
    choice = input("C)음료선택 S)계산하기 X)종료하기 입력해주세요: ")
    if choice == 'X':
        print("종료합니다.")
        break
    if choice == 'S':
        print("계산합니다. 잔돈은 %d원입니다." % leftMoney)
        break
    if choice == 'C':
        drink = input("원하는 음료를 영어로 입력해 주세요: ")
        if drink == 'cola':
            sum += machine['cola']
            continue
        elif drink == 'spaceCola':
            sum += machine['spaceCola']
            continue
        elif drink == 'zeroCola':
            sum += machine['zeroCola']
            continue
        elif drink == 'sprite':
            sum += machine['sprite']
            continue
        elif drink == 'hwenta':
            sum += machine['hwenta']
            continue
        elif drink == 'pepper':
            sum += machine['pepper']
            continue
        elif drink == 'monster':
            sum += machine['monster']
            continue
        elif drink == 'poweraid':
            sum += machine['poweraid']
            continue
        elif drink == 'nestea':
            sum += machine['nestea']
            continue
        elif drink == 'vitaminWater':
            sum += machine['vitaminWater']
            continue
        elif drink == 'minimade':
            sum += machine['minimade']
            continue
        elif drink == 'zoziaCoffe':
            sum += machine['zoziaCoffe']
            continue
        elif drink == 'ambasa':
            sum += machine['ambasa']
            continue
        elif drink == 'matecha':
            sum += machine['matecha']
            continue
```
![image](https://user-images.githubusercontent.com/115389450/233531820-a72ef6b1-abc7-4b71-8b86-a49bc496f877.png)
![image](https://user-images.githubusercontent.com/115389450/233531856-2078461f-0c4e-4492-b05d-99aeb8625ba3.png)
```
from random import randint
import time

youtubeName = input("유튜브 채널 이름을 입력 해 주세요 : ")
viewerSum = 0
subscriber = 0
todayContent = input("오늘의 컨텐츠 입력을 해 주세요 : ")
for i in range(1, 21):
    sec = 10
    print("방송 송출 시작~!")
    print(f'{i}번째 방송!')
    viewerSum = 0
    while sec != 0:
        sec = sec-1
        time.sleep(1)
        viewers = randint(50, 2500)
        viewerSum += viewers
        print("현재 시청자 수 : %d명" % viewerSum)
    subscriber += int(viewerSum / randint(1, 5))
    print("%s 컨텐츠" % todayContent, "구독자 %d명입니다." % subscriber)
    if subscriber > 100000:
        print(f'{i}번째 방송송출만에 10만유튜버가 되었습니다! 축하합니다! 실버버튼 증정!')
        break
if subscriber < 100000:
    print("20번의 방송을 하였지만, 구독자수가 10만명이 안되어 유튜브 채널이 폭파되었습니다 ㅜㅜ")

```
![image](https://user-images.githubusercontent.com/115389450/233531907-618ba5d8-29cb-469a-86e0-8efe12334a53.png)
```
primeCheck = int(input("입력한 숫자까지 범위 중 소수 판별:"))

for i in range(1, primeCheck+1):
    cnt = 0
    for j in range(1, primeCheck+1):
        if i % j == 0:
            cnt = cnt + 1
    if cnt == 2:
        print(f'{i}는 소수입니다.')
```
![image](https://user-images.githubusercontent.com/115389450/233531948-20ac77a5-b45b-491d-a2ed-04778d4c7ffc.png)









