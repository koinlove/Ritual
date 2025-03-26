# Ritual Node 설치하기(1.4.0)
현재 나와있는 가장 최신 버젼입니다!

> ### 들어가기 전에 잠깐! 노드를 돌리기 위한 최소 사양이 뭔가요?

![image](https://github.com/user-attachments/assets/35418cd5-12be-4db7-97bc-e6a0ae9502af)
리츄얼 아카데미 홈페이지에 있는 사진으로 대체하겠습니다~

참고로 VPS로 돌릴 수 있는데(대부분 VPS로 돌림) 요즘 VPS 사이트들 값이 많이 비싸져서 ㅎㅎ;;

![image](https://github.com/user-attachments/assets/2a670773-adbc-4779-9966-47bd241028f6)


개인적으로 [콘타보](https://contabo.com/en/vps/)에 들어가셔서 제가 체크한 제품 사는 걸 추천합니다!

![image](https://github.com/user-attachments/assets/df6c6ba1-61a6-41a1-9c79-15d43b320a1e)
Select 누르시면 이렇게 결제창이 뜨는데, 다른 건 다 건드릴 필요가 없고

![image](https://github.com/user-attachments/assets/89827353-3de8-450a-ac6c-fdf0bbcf8c46)
## 용량 꼭 500으로 늘리시고!!!!!! (안 하면 진짜 후회함)

![image](https://github.com/user-attachments/assets/41132724-aecc-4222-bbd6-e756e26854a9)
## Ubuntu 24.04에서 건드리시면 안 됩니다!!! 
(Apps& Panels에 도커 추가설치 가능한데, 어차피 스크립트에 설치 명령어가 있으니 건드리지 않는 걸 추천합니다)

이제 결제까지 끝나면 님의 메일 주소로 님의 **VPS 디테일**이 올 거임

## 로그인하는 방법
![image](https://github.com/user-attachments/assets/d677a814-aa9a-4647-b4c6-9fa622363741)

참고로 저는 [터미널](https://apps.microsoft.com/detail/9n0dx20hk701?hl=ko-KR&gl=KR)을 사용하고 있습니다.

터미널이 제일 편하구 다계 관리도 쉬워요! putty나 cmd, powershell 같은 건 너무 불편함.

여기에 이제 로그인을 해야되는데, 명령어는 다음과 같음

```bash
ssh root@님의.아이피.주소.넣으삼
```
참고로 IP 주소는 님 메일주소에 왔을 거임 **가끔 VNC IP 넣는 사람들 있는데, 그건 특수한 경우 아니면 안 씀. IP Address 넣으세요!!**

![image](https://github.com/user-attachments/assets/fb994adf-ec51-4d06-b7b1-6d0aba6c3014)

아이피를 넣으면 이렇게 비밀번호를 입력하라고 뜨는데, 비밀번호 입력하면 됨.
**참고로 비밀번호 쳐도 뭐 안 보이는 게 맞으니까 걱정 않고 치면 됩니다~**

![image](https://github.com/user-attachments/assets/eba2b922-7bd6-4a7d-ae7d-1cbf674a3817)

그러면 이런 화면과 함께 로그인이 완료됐다는 게 뜰 거임! 그러면 세팅 완료~

## Ritual Node 설치하는 방법
```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```
위 명령어를 **로그인한 콘타보(중요)**에 입력하면

![image](https://github.com/user-attachments/assets/75ae02d0-17ec-4cdc-b187-0b895530e20d)

이런 화면이 뜰 거에용. 여기서 1번 입력!


![image](https://github.com/user-attachments/assets/e7202531-0519-49d2-8dcc-7dad45842c11)

이런 식으로 메세지가 뜨면 설치가 완료된 것!

그 이후에
```bash
screen -S ritual
```
을 입력해서 아무 것도 없는 검은 화면이 뜨면
```bash
cd ~/infernet-container-starter && project=hello-world make deploy-container
```
를 입력해서 컨테이너 계약까지 끝마치기!

![image](https://github.com/user-attachments/assets/b650e3f4-6926-47ee-b316-fbaf527e28ba)

이런 식으로 괴상한 화면이 떠도 무시하고 > **CTRL + A + D**로 화면 나오기!

```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```
다시 이 명령어를 입력해서
![image](https://github.com/user-attachments/assets/6ed0854b-5469-43e0-94c6-6e4928172af6)

2번을 입력하면

![image](https://github.com/user-attachments/assets/7f6523af-d826-49cb-80ce-08aaa634f8c5)

이런 식으로 PRC 입력하는 곳과 Private key를 넣는 칸이 뜰 거에요!
입력하고 나면 글씨가 약간 잘릴 텐데 오류 아니니 넘어가삼

### 이 쉘 스크립트는 알케미가 아닌 퍼블릭 rpc에 최적화된 스크립트입니다. 
예전엔 알케미에서 직접 rpc 주소를 뽑아서 썼는데, 지금은 알케미가 이전보다 무료 compute unit usage를 1/3로 줄여서 베이스 메인넷 rpc를 쓰시는 걸 추천드립니다. 

참고로 무료 베이스 rpc 주소는
```bash
https://mainnet.base.org/
```
입니다.

![image](https://github.com/user-attachments/assets/61abc8ce-bc11-4448-b331-64896460bb38)

입력을 완료하면 이런 식으로 막 진행될 텐데 매우 빠르게 진행되는 게 맞으니 ㄱㅊㄱㅊ. 이후에

```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```
다시 이 명령어 입력해서
![image](https://github.com/user-attachments/assets/b9c9778c-a144-4a3e-bec7-5f8dbf6bd59d)

이렇게 입력하면 자동으로 절차가 진행될 텐데

![image](https://github.com/user-attachments/assets/5aef0b3c-facf-4e6f-9600-ca5b7ea44f06)

중간에 이런 문구가 뜰 거임 밑줄친 아이 위치 기억해 뒀다가

![image](https://github.com/user-attachments/assets/7ff50435-908e-4152-806a-fe3df15ad84c)

요런 문구가 뜨면 저 밑줄친 곳을 복사해서 붙여넣기!

그러면 또 알아서 지 혼자 진행될 거임. 잠시 대기....

![image](https://github.com/user-attachments/assets/a48f064c-f618-4dd9-bbe2-5180bcd9a803)

요런 문구가 뜨면 설치는 완료~ 

> ## 마지막으로 아까 꺼둔 도커까지 다시 켜야됨!!!

```bash
cd ~/infernet-container-starter/deploy && docker compose up
```
마지막으로 이 커맨드까지 입력해서 꺼졌던 도커를 다시 키면 

> # 진짜 끝~

## 리츄얼 꺼졌어요 ㅠ 재시작 하고 싶음...
```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```
![image](https://github.com/user-attachments/assets/c54dd4ea-9e38-4791-8ecd-fd065db5a7f7)

명령어 치고 4번 입력하면 지 혼자 도커 꺼줄 거임!

이후
```bash
cd ~/infernet-container-starter/deploy && docker compose up
```
을 입력하면 자기 혼자서 또 켜질 거임.
![image](https://github.com/user-attachments/assets/51126e1b-637e-4261-ae9f-dbd5807cab59)

이후에 이렇게 로그가 내려갈 텐데, 먼저 
> ### 1. 새로운 터미널을 추가하고 (1번) 다시 콘타보로 로그인한 다음에
> ### 2. 기존에 있는 터미널을 끄고 (2번)
> ### 3. docker ps를 쳐서 도커 5개가 잘 켜졌는지 확인하세요

## 리츄얼에 등록된 내 지갑 주소 바꾸고 싶음...
```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```
대체 그걸 왜 바꾸고 싶은지 모르겠지만 혹시나 해서 명령어 넣어봤어요~

![image](https://github.com/user-attachments/assets/4d90ebb9-c6f5-441e-a9ab-f59cb066a8bc)

이렇게 넣고 대기하면 알아서 잘 진행될 거임... 대기하고 있다가

![image](https://github.com/user-attachments/assets/e3e5b2f4-edf4-4696-b1de-afc73953d0b7)

중간에 이런 문구가 뜰 거임 밑줄친 아이 위치 기억해 뒀다가

![image](https://github.com/user-attachments/assets/a70f5ff0-9703-42d3-8999-238dbe88c9ca)

요런 문구가 뜨면 저 밑줄친 곳을 복사해서 붙여넣기!

그러면 또 알아서 지 혼자 진행될 거임. 잠시 대기....

![image](https://github.com/user-attachments/assets/3784f9a6-f3d1-4cc9-a96d-7a5d4c2894b8)

요런 문구가 뜨면 지갑주소 변경도 끝~

## 리츄얼에 등록된 RPC를 바꾸고 싶음...
```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```

![image](https://github.com/user-attachments/assets/9294f549-811f-4a59-8919-99aeb5975504)

이렇게 잘 입력하면 자기 알아서 진행이 될 거에효. 리스타트도 알아서 진행됨.

근데 만약 리스타트 했는데 RPC가 잘 안 된다? 그럴 땐 
> ### 리츄얼 꺼졌어요 ㅠ 재시작 하고 싶음...
으로 돌아가시면 됩니다~

## 리츄얼을 업데이트하고 싶어요~ (10/7일자 기준)
```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual_Node/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```
를 입력하고
![image](https://github.com/user-attachments/assets/525d9ea4-a8ad-4617-81d1-d78f0c0297b7)

7번을 선택하면 자동으로 업데이트가 돼요~

## 리츄얼 업다운을 해도 용량이 안 비워져요...

```bash
sudo du -ah / | sort -rh | head -20
```
로 용량 확인해 보시고(안 해도 됨)

```bash
sudo truncate -s 0 /var/log/syslog
sudo truncate -s 0 /var/log/syslog.1
```
하고서

```bash
df -h
```
쳐서 용량이 비워졌는지 확인하기
## 리츄얼 내 콘타보에서 지워버리고 싶음
```bash
[ -f "Ritual.sh" ] && rm Ritual.sh; wget -q https://raw.githubusercontent.com/koinlove/Ritual/main/Ritual.sh && chmod +x Ritual.sh && ./Ritual.sh
```
혹시나해서 명령어 넣었어요. 참고로 이거 해도 완벽하게 지워지는 건 아닐 거임 분명. 만약 자기가 리츄얼과 다른 노드를 같이 돌리고 있다, 근데 다른 노드는 초기화하기 어려운 노드(예를 들어, >셀레스티아 노드< 라거나, >엘릭서노드< 라거나, >하이퍼리퀴드< 라거나... 네

![image](https://github.com/user-attachments/assets/9be1c887-e542-4a10-a452-a33b52c7ddbb)

이렇게 8번 입력하면 알아서 지워줄 거임. 다 되면 다 됐다는 문구 뜨니까 걱정 ㄴㄴ혀

추가 문의사항이 있다면 제 메일로 문의하세요.

```bash
curl localhost:4000/health
```
치시면 됨.
