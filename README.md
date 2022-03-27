# Netpractice

This project is a general practical exercise to let you discover networking

## Topic


<details>
<summary> Lv. 1 </summary>
서브넷 마스크를 보고 네트워크부 아이피를 계산하여 같은 네트워크 부를 가지는 아이피를 할당해주면 됨.
</details>
<details>
<summary> Lv. 2 </summary>
Lv.1 과 동일
</details>
<details>
<summary> Lv. 3 </summary>
스위치가 여러개의 네트워크를 한 네트워크 대역으로 묶어줌. 
스위치는 2계층 장비로서 MAC 주소를 이용하여 연결된 네트워크를 구분함.(L2 스위치 한정)
loop가 탐지되는데, 이는 처음 스위치가 작동할때 네트워크 내 장비들의 MAC 주소를 갖고 있지 않아서 일어나는 현상으로 추정
</details>
<details>
<summary> Lv. 4 </summary>
라우터는 WAN 대역으로 다른 네트워크와 연결해줌. 이때 라우터의 인터페이스 IP는 서로 다른 영역 이여야 함.
</details>
<details>
<summary> Lv. 5 </summary>
Lv.4 와 동일
</details>
<details>
<summary> Lv. 6 </summary>
라우팅 테이블은 [SRC] -> [DST] 형태로 구성되며 SRC에 해당하는 IP를 가진 패킷이 오면 DST로 전송됨.
0.0.0.0/0 or default 는 모든 네트워크를 의미함.
또한 클라이언트 A에서 인터넷으로 요청을 보낸다면, 패킷은 인터넷의 IP를 갖고 클라이언트 A에서 출발하여 인터넷의 IP까지 찾아감.
인터넷에서 클라이언트 A로 응답하는 과정도 동일.
</details>
<details>
<summary> Lv. 7 </summary>
연결된 라우터도 같은 네트워크 대역에 있어야 함. 그러지 않으면 라우팅 테이블이 설정되어 있어도 패킷이 나가는 gateway가 적절하지 않아서 패킷이 사라짐.
</details>
<details>
<summary> Lv. 8 </summary>
기본적으로 각 대역폭당 독립적인 ip 영역을 가지고 있으면 됨.
하지만 인터넷과 통신하므로, private ip를 갖고 있으면 요청을 보낼 순 있지만 받을 순 없음.
따라서 범위를 잘 지정해서 넣어야함.
</details>
<details>
<summary> Lv. 9 </summary>
Lv.1 ~ Lv.8 응용
</details>
<details>
<summary> Lv. 10 </summary>
Lv.1 ~ Lv.8 응용
</details>


<details>
<summary> network 관련  </summary>

`traceroute` 명령어로 라우팅 되는 과정 볼 수 있음 (8.8.8.8 = google)
![img](asset/img.png)

`nslookup` 명령어로 특정 도메인의 ip or 그 반대를 알 수 있음

`net-server` 서버를 열어줌...?

`nettop` 소켓과 라우터들의 리스트를 보여줌

`netbios` 넷 바이오스...?

`networksetup` 컴퓨터에 연결된 네트워크 정보들

`netstat` network status

`netstat -rn` route table

`netstat -an` 포트 확인

`lsof -i -n` 인터넷과 네트워크 파일들의 listening 상태확인
`lsof -i TCP ` TCP 상태 확인

`nc [HOST] [PORT] ` TCP 연결, UDP 패킷 전송 등등 TCP UDP 관련 많은걸 하게 해줌.

`wireshark` 라는 프로그램을 이용하여 패킷 캡쳐 가능. 패킷들의 구조를 알 수 있고, TCP 같은 프로토콜이 어떤식으로 진행되는지 파악하기 쉬움.

</details>

# Reference

[IBM TCP/IP](https://www.ibm.com/docs/ko/aix/7.1?topic=management-transmission-control-protocolinternet-protocol)

[네트워크 강의](https://www.youtube.com/playlist?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)