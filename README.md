# HW06 플랫폼 게임

회전, 이동하는 플랫폼과 장애물을 피해 모든 🍬을 모아 종료 지점까지 도달하는 게임
## 📜게임 규칙
- 플레이어의 목숨은 3개 ❤️❤️❤️
- 플레이어가 떨어져 목숨을 잃게 되면 시작지점에서 리스폰된다.
- 해당 레벨의 모든 사탕을 모으지 못하면 종료 지점에 도달해도 레벨을 끝낼 수 없다.

## 🎬플레이 영상
 [![YouTube](https://img.youtube.com/vi/OiMeScbH7kQ/0.jpg)](https://www.youtube.com/watch?v=OiMeScbH7kQ)

## 📌구현 기능

**1. Tick 기반으로 회전, 이동하는 플랫폼, 장애물**
```
언리얼 에디터에서 값을 넣지 않은 경우 레벨에 로드될 때 
BeginPlay()에서 100~150 사이의 랜덤한 값을 속도나 이동 거리에 넣어
매번 다른 속성을 갖는다. 
```
**2. 오버랩 시 랜덤한 방향으로 회전하는 플랫폼**
```
오버랩 발생 시 원래의 회전 축을 제외한 나머지 축중 하나를 기준으로 회전한다.
```
**3. 오버랩 시 랜덤한 방향으로 이동 후 1초 뒤 사라지는 플랫폼**
```
오버랩 발생 시 원래 속도의 5배로 랜덤한 위치로 이동하고 1초 뒤 사라진다.
```
**4. 레벨에 랜덤하게 배치되는 맵 모듈**

![MapModule](https://github.com/user-attachments/assets/241e538f-b95e-4355-bed6-de8bfc5cc0df)

```
[그리드]
행 개수: 레벨 + 1
열 개수: 2 고정
각 행에 하나의 맵 모듈을 열 중 하나에 랜덤하게 배치한다.
```
**5. 아이템 랜덤 스폰**
```
맵 모듈에 설치한 스폰 볼륨에서 랜덤한 위치에 3개씩 스폰된다. 
스폰할 아이템의 수는 `HW06_GameMode`의 `Spawning` 카데고리의 `CandyToSpawn` 으로 바꿀 수 있다.
```

## 💀사용 에셋
맵: 
[Cropout Smaple Project](https://www.fab.com/ko/listings/bd733d81-7c29-44fe-b53f-65b14d06a9e2)

캐릭터: [Cemetery - Mummy - Undead Character | Free Gift December 2024](https://www.fab.com/ko/listings/b2a3ddd5-2933-4313-8131-c5e03b24fff9)

사탕 아이템: [Cute Candy](https://www.fab.com/ko/listings/f48a3022-06ee-4788-9f63-76a3850583aa)

장애물, 플랫폼: 내일배움캠프 언리얼 3/4기 제공


## 📌앞으로 추가할 기능

- 3 레벨까지 진행
- 다양한 맵 모듈
- HUD
