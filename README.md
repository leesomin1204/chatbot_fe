# 챗봇 - 프론트엔드

## 개요
AI 챗봇 대화 시스템
사용자가 입력한 메시지를 AI 백엔드 서버에 전달하고, 그에 대한 응답을 받아 채팅 인터페이스에 출력하는 React 기반의 웹 챗봇 UI입니다.
간단한 질의응답을 통해 사용자와 상호작용하며, 서버로부터 받은 메시지를 실시간으로 표시합니다.

## 기능 설명 
- 페이지 구성 흐름
  - ChatPage (/chat)
    - Helmet을 사용해 탭 제목을 AI와 대화로 설정
    - ChatContainer 렌더링
  - ChatContainer
    - 전체 채팅 UI의 중심 컴포넌트
    - ChatLog + ChatInput으로 구성
    - 사용자 메시지를 입력받고, 서버에 요청 후 응답을 출력

- ChatInput.js
  - 사용자 메시지를 입력하고 제출하는 인터페이스
  - form 요소 내부에 input과 제출 버튼 포함
  - 버튼에는 FaLocationArrow 아이콘 사용
  - 메시지 입력 중에는 비활성화 가능

- ChatLog.js
  - 채팅 내역 전체를 보여주는 UI
  - 채팅 항목 배열을 map으로 출력하며, 항목은 user와 system으로 구분
  - GiRobotGolem(챗봇), CgUserlane(사용자) 아이콘을 메시지 앞에 표시
  - 응답 대기 중에는 loading.gif 이미지를 중앙에 출력
  - useEffect를 통해 메시지가 추가될 때 자동 스크롤 처리
