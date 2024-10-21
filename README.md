# GroupChat_Project
Group Chat Project for portfolio
https://f-lab.kr/insight/understanding-git-and-github-collaboration

## 단체 채팅 프로그램 개발 계획서

### 1. **프로젝트 개요**
- **프로젝트명**: Java Swing을 이용한 단체 채팅 프로그램
- **개발 도구**: Java, Java Swing (JFrame), Socket 통신, 멀티스레딩
- **프로젝트 목적**: 
    > JFrame을 활용하여 GUI 기반의 단체 채팅 프로그램을 개발하고,  
    여러 사용자가 동시에 메시지를 주고받을 수 있는 실시간 채팅 환경 제공.
- **주요 기능**:
    - 다수 사용자 간 실시간 채팅
    - 클라이언트와 서버 간 통신
    - 사용자별 닉네임 설정
    - 메시지 전송 시 TimeStamp 표시
    - 메시지 알림 기능 | (이거 할 수 있나???)

---

### 2. **개발 범위 및 목표**
- **서버 측**:
    > 다중 클라이언트의 연결을 처리하고,  
    각 클라이언트에서 전송된 메시지를 모든 클라이언트에 전달하는 역할을 담당.
    - 클라이언트 연결 및 해제 처리
    - 메시지 브로드캐스트 기능
    - 연결된 사용자 관리
- **클라이언트 측**: 
    > 사용자가 채팅 메시지를 입력하고,  
    서버를 통해 다른 사용자와 메시지를 주고받을 수 있는 GUI를 제공.  
    - 메시지 입력 및 출력 창
    - 서버 연결 및 사용자 정보 설정
    - 메시지 전송 및 수신
    - 사용자 접속/해제 알림

---

### 3. **시스템 구성**

- **클라이언트/서버 구조**:
  - **클라이언트**: 각 사용자는 클라이언트 애플리케이션을 실행하여 서버에 접속, 메시지를 주고받음.
  - **서버**: 중앙에서 모든 클라이언트의 메시지를 수신하고, 이를 다른 모든 클라이언트에게 전달함.

- **사용 기술**:
  - **Java Swing (JFrame)**: GUI 개발을 위한 Java의 기본 라이브러리.
  - **Socket 통신**: TCP/IP를 사용한 클라이언트-서버 간 실시간 통신.
  - **멀티스레딩**: 여러 클라이언트가 동시에 접속하고 메시지를 주고받을 수 있도록 서버는 각 클라이언트에 대해 별도의 스레드를 실행.

---

### 4. **기능 상세**

- **로그인 화면**:  
  - 사용자가 서버에 접속하기 전, 닉네임을 입력하는 화면.
  - 서버에 접속 요청을 보내고, 접속 성공 시 채팅 창으로 전환.

- **메인 채팅 창**:
  - **채팅 메시지 표시 창**: 모든 사용자에게 전송된 메시지를 시간 순서대로 표시.
  - **메시지 입력 필드**: 사용자가 메시지를 입력할 수 있는 텍스트 필드.
  - **전송 버튼**: 입력된 메시지를 서버로 전송.
  - **사용자 리스트**: 현재 접속한 사용자들의 목록을 표시.

- **서버 기능**:
  - 클라이언트로부터 메시지 수신 후, 다른 모든 클라이언트에 메시지 전송.
  - 클라이언트 접속 및 접속 해제 시 알림 메시지 전송.

---

### 5. **개발 일정**

| 단계                     | 작업 내용                            | 기간 |
|--------------------------|-------------------------------------|------|
| 1. 요구사항 분석          | 요구사항 정의 및 기술 스펙 작성        | 1주 |
| 2. 서버 개발 | 서버 소켓 구현, 멀티스레딩 처리 및 메시지 브로드캐스팅 기능 구현 | 2주 |
| 3. 클라이언트 GUI 설계  | JFrame을 이용한 GUI 설계, 사용자 인터페이스 개발     | 2주 |
| 4. 클라이언트 기능 구현   | 메시지 전송, 수신, 서버 연결 기능 구현  | 2주 |
| 5. 테스트 및 버그 수정    | 통합 테스트 및 버그 수정               | 1주 |
| 6. 배포 및 유지보수       | 프로젝트 배포 및 유지보수              | 1주 |

---

#### 6. **기대 효과**
- Java 기반의 실시간 채팅 프로그램을 통해 네트워크 프로그래밍 및 GUI 개발 역량을 강화.
- 실제 응용 가능한 단체 채팅 프로그램 개발로 사용자 간의 원활한 의사소통 도구 제공.
  
---

#### 7. **추가 고려사항**
- **보안**: 데이터 암호화 및 안전한 연결 보장을 위한 SSL/TLS 적용 검토.
- **확장성**: 추후 파일 전송, 사용자 프로필 설정, 방 만들기 등의 추가 기능을 고려.

---

![image](https://github.com/user-attachments/assets/635831ff-beae-4482-b983-0352eb4f0fd2)

