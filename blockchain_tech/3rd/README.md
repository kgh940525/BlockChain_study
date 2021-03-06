# YAPP 12기 블록체인 스터디 3주차 (Tech)

### 1. 진행내용  
- [KISA 핀테크 기술지원센터] [__코인스택 기반의 블록체인 기초(지갑)개발__](https://onoffmix.com/event/132771) 수강

### 2. 수강 내용 정리  
![image](https://onoffmix.com/images/event/130182/s)  

#### 1. 블록체인 정의  
##### 1.1 원론적 정의
    데이터 분산 처리 기술  
> __P2P 방식__ 을 기반으로 생성된 체인 형태의 __연결고리 기반__ 분산 데이터 저장환경에 저장됨  
> 누구도 임의로 수정될 수 없고 누구나 변경의 결과를 열람할 수 있는 __분산 컴퓨팅 기술 기반의 데이터 위변조 방지__ 기술  

##### 1.2 구조 관련 용어 정의
- 트랜잭션 : 송금 내용을 담은 거래 데이터 (A에서 B로 비트코인을 주겠다)  
           비트코인 계좌 -> 계좌로 권한 이전  
           
- 블록    : 블록 헤더와 트랜잭션의 집합  
  ![image](https://github.com/YAPP12th/BlockChain_study/blob/master/blockchain_tech/0.Reference/photo/3_tech_block.png)  
  
- 블록체인 : 블록이 연결되어 있는 연결체   
  ![image](https://github.com/YAPP12th/BlockChain_study/blob/master/blockchain_tech/0.Reference/photo/3_tech_blockchain.png)  
  
  
##### 1.3 구성원 관련 용어 정의
- 노드 (Backend 로서의 역할)  
  트랜잭션 내역 보관, 트랜잭션 승인, 분산합의  
- 클라이언트 (Frontend 로서의 역할)  
  트랜잭션 생성, 거래 내역 확인 (비트코인의 경우 지갑)  

#### 2. 블록체인 특징

- 상당한 익명성  
  > 블록체인상의 모든 노드나 사용자는 신원을 대신하는 30자 이상의 글자와 숫자로 이뤄진 고유의 주소를 가짐  
  > 사용자의 선택에 따라 익명을 유지하거나 자신의 신분을 밝힐 수도 있으며, 거래는 블록체인 주소로 진행  
  
- 신뢰가 불필요한 신뢰 네트워크  
  > 신뢰하지는 않지만 네트워크를 통해 주고받는 데이터는 신뢰를 보장함  
  > ( <=> 우리를 믿고 로그인을 해라라는 패러다임의 반대)  
  
- 불가역성  
  > 그 전에 있었던 모든 거래기록과 연결되기 때문에, 업데이트 된 새로운 기록은 변경이 불가능함  
  > 데이터베이스의 기록이 영구적으로 발생 순서에 따라 기록되고 네트워크상의 모든 사람이 이용할 수 있도록 하기 위해 다양한 컴퓨터 알고리즘과 접근법이 효율적으로 활용됨.  
  
- 모두에게 공개된 환경  
  > 모든 거래와 그 가치는 시스템에 접근할 수 있는 모든 사람이 볼 수 있음  
  > 무결한 정보를 쉽게 공유할 수 있다.  
  > (ex> 내가 먹는 소고기의 원천 파악 가능)  
  
- 타인의 관여가 어려움  
- 분산 환경에서의 신뢰성  

#### 3. 블록체인의 배경  

- INTERNET  
  > 컴퓨터를 서로 연결하여 TCP / IP라는 통신 프로토콜을 이용해 정보를 주고 받는 네트워크  
  > 중앙 통제 조직이 없는 개방형 통신망  
  > 독립적이고 고유한 IP 주소 기반  
  > 특정 주소로 손실 없는 정보 공유 보장  
  > 전세계에서 활용되고 있음  
  
- 화폐적인 가치만이 아닌 smart contract(법적인 절차를 줄이고 실행이 강제되는 형태) 등으로 재조명 받음  
  > ex> 월세를 안내면 자동으로 권한이 없어져 내 집을 강제적으로 들어갈 수 없게 됨 (돈을 내야 들어갈 수 있음)  

- 기존 활용  (Server - Client)  
  > 서버와 클라이언트의 개념을 둠 (클라이언트 : 서비스 활용 | 서버 : 서비스 제공)  
  > 
  > Centralized Trusted 3rd party  
  > - 3자가 서버를 관리 및 검열  
  > - 완성화된 데이터를 관리하고, 해커들이 뚫지 못하도록 지킴  
  > #### 
  > 한계  
  > - 많은 자원 필요  
  > - 특정 공격에 매우 취약  
  > - 데이터 무결성 검증 및 감사 어려움  
  > - 공공 / 메타 데이터 소유권 문제  

- 블록 체인 (Peer to Peer)  
  > 피어라는 개념으로 움직임  
  > 피어는 노드(서버), 클라이언트 모두가 될 수 있음  
  >  
  > 피어가 맡을 수 있는 유형  
  > 1. 풀 클라이언트/노드 (Full Client/Node)  
  >    - 비트코인 사용자들의 지갑을 관리  
  >    - 비트코인 거래 정보 전부(모든 사용자가 현재까지 진행한 거래내역 전부)를 사용자가 저장  
  >    - 비트코인 네트워크상으로 직접 거래를 만듬  
  >    - 독립형 이메일 서버와 유사  
  >	
  > 2. 라이트웨이트 클라이언트/노드 (Lightweight Client/Node)  
  >    - 사용자의 지갑을 저장  
  >    - 비트코인 거래나 네트워크에 접근하기 위해서는 제3자가 소유한 서버에 의존  
  >    - 거래내역 전부에 대한 복제본을 저장하지 않음 (ex> 시작과 끝만을 저장)   
  >    - 독립형 이메일 클라이언트와 유사  
  >	
  >	3. 웹 클라이언트/노드 (Web Client/Node)  
  >    - 웹 브라우저를 통해 접속  
  >    - 제3자가 소유한 서버상에 사용자의 지갑을 저장  
  >    - 웹 메일과 유사  

#### 4. 블록체인의 원리  

1. 분산  
   > Q : 블록체인에서 체인내용이 저장되는 공간은 어디인가요?  
   > A : 노드에 저장된다. 더불어 노드는 2개의 DB를 가지고 있다.  
   >	> 1. 블록체인 트랜잭션 보관 데이터베이스 (거래내역)  
   >	>    - Linked List 구조
   >	>    - 올바른 트랜잭션을 시간의 순서대로 연결 및 보관  
   >	> 2. 어플리케이션 데이터베이스 (잔액)  
   >	>    - 저장된 트랜잭션을 어플리케이션에 적용  
  
2. Peer to Peer
   > Q : 정말 돈(코인)을 보내는 건가요?    
   > A : 실제 화폐를 주고 받을 수 없기 때문에, 거래 내용에 맞게 장부를 갱신하는 것으로 대체  
   >	> #### 기존 은행 방식 (A와 B가 OO 은행을 이용한다고 가정)  
   >	> - A가 B에게 10만 원을 송금  
   >	> - OO 은행에 있는 장부에서 A가 B에게 10만 원을 보냈다는 기록 작성  
   >	> - A의 잔액이 10만원 감소, B의 잔액이 10만원이 증가  
   >	>  
   >	> #### 블록체인 방식 (A와 B가 OO 은행을 이용한다고 가정)
   >	> ![image](https://github.com/YAPP12th/BlockChain_study/blob/master/blockchain_tech/0.Reference/photo/3_tech_%20process2.png)  
   >	> - A가 B에게 10만 원을 송금한다는 트랜잭션 생성 후 블록체인 네트워크에 전파  
   >	> - 블록을 생성하는 노드는 트랜잭션을 모아 블록에 저장 (거래에 대한 검증 거침)  
   >	> - 노드들이 보관하는 데이터베이스 갱신    
   >	> #### ![image](https://github.com/YAPP12th/BlockChain_study/blob/master/blockchain_tech/0.Reference/photo/3_tech_%20process3.png)      
   >	>즉, 거래 내용과 잔액의 상태, 두 가지 정보() 가 있고 거래 내역이 검증되면 잔액의 상태가 변경됨
 
3. Hash
   > 일정한 값에 대해 항상 동일한 결과 값 보장  
   > 역추적은 불가능함  
   > Merkle Tree : Hash value 의 tree 그룹  
   > ![image](https://github.com/YAPP12th/BlockChain_study/blob/master/blockchain_tech/0.Reference/photo/3_tech_merkletree.png)  
   > 위와 같이 해시값과 해시값에 대한 새로운 해시값을 만듬  
   >  -> 기존 데이터 검증을 위해 4개의 해시값이 필요했으나 이걸 통해 하나의 해시값만 있으면 됨
 
 
#### 5. 블록체인의 거래 과정
트랜잭션 : 입력(여러개 가능) + 출력(여러개 가능)
> 입력 : 이전 트랙잭션의 출력
> 출력 : 돈을 받을 사람 주소 + 금액
트랜잭션들이 시간 순으로 모여 블록에 저장됨
  
과정 (A -> B 10만원 보냄)
- (의사 표시)     클라이언트가 새로운 트랜잭션 생성  
- (서명 및 유효화) A의 비밀키로 서명하여 거래 유효화
- ![image](https://github.com/YAPP12th/BlockChain_study/blob/master/blockchain_tech/0.Reference/photo/3_tech_assign.png)  
- (전송 및 전파)  비트코인 네트워크(비트코인 노드)에 전송 및 모든 노드에게도 전파
   > 분산합의 과정을 통해 인증 및 공유  
   > 트랜잭션들을 모아 __블록 생성(마이닝)__
- (검증 및 기록) 채굴을 하는 노드에 의해 검증된 후 블록에 영구적으로 기록  

#### 기타 QnA
Q : 잔고 값을 기억하고 있는가?  
A : 블록헤더를 통해 이체내역, 거래내역, 트랜잭션 등은 존재하지만 "A의 잔고는 얼마야?" 이런거는 알 수 없다.  
  
Q : 블록체인 내에서 시간의 개념이 어떻게 돌아가는지 궁금합니다.  
A : 블록체인 내에서는 시간이 존재하지 않는다  
   > 여러 평행세계는 존재하겠다만, 정확한 시간은 존재하지 않는다.  
   > (ICO) 시간이란 개념을 쓰지 않고 블록 높이를 사용한다.  
   > 2주마다 블록이 만들어질 개수가 채워지면 2주로 대략적으로 잡고 계산 (블록수를 기준으로 잡음)
  

#### 참고
- 체인 내용이 저장되는 곳 : https://steemit.com/kr-qna/@mattchoi/nzfmv-kr-qna  
- 초등학생도 이해할 수 있는 블록체인 : http://ppss.kr/archives/150114  
- 블록체인 거래 과정 : https://steemit.com/kr/@jsralph/5f59rf-1  
- [BlockChain] 블록체인에 관하여 - 2 : http://ulismoon.tistory.com/11
