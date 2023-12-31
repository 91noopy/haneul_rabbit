# haneul_rabbit
2021 하늘고 토끼장 방범 프로젝트 

1. 동기

하늘고 운동장 외곽에는 토끼장이 있다. 축구골대와 비슷한 재질의 그물로 둘러 쌓인 토끼장이 알 수 없는 야생동물의 습격을 받아 대부분의 토끼가 죽는 사고가 발생했다. 하늘고 인근 백운산에서 우리가 추측한 포식 동물의 서식 흔적이 다수 발견된 바, 위와 같은 사건이 재발할 가능성이 높다고 판단했다. 이를 대비하기 위해 자체 방범 시스템을 개발했다. 

2. 방범 시스템 개요

아두이노를 활용하여 야생 동물이 토끼장에 유효한 충격을 가할 시 이 충격값을 데이터베이스를 통해 서버에 업로드하면 이를 감지한 프로그램이 즉각적으로 생활관 컴퓨터에 경고 화면을 표시한다. 프론트 엔드는 html과 css로 웹 페이지를 구현했다. 백 엔드는 파이썬 코드를 활용했다. 파이어베이스는 현재 구동하지 않고 소스 코드만 기록했다. 

3. 웹 페이지 'secuhigh'

앱 구성 요소

-	홈 화면 
회원가입 | 로그인:  호출 기능을 사용할 고객들을 회원제로 운영,
[사진 업로드, 방범 호출 기능 사용을 원할 시 가입]
[생태 정보는 회원 가입 없이도 프리 소스로 제공]
알림 설정, 알림 액세스: 회원 가입 시 승인 요청
갤러리 액세스: 회원 가입 시 승인 요청
	회원 정보는 DB로 저장 

호출: 
1	처음 눌렀을 때: 방범호출 시스템 유무 묻기
블루투스 설정: 방범 대상과 어플리케이션 연결

2	이용 화면

생태 지도: 지도 화면 위 서식하는 야생동물들과 그에 따른 정보 공개
		지도 위 핑 형태로 서식 동물 사진 아이콘 띄움
  
  	아이콘을 누르면 동물의 습성, 흔적 등의 정보 텍스트 파일 화면
   댓글 기능을 활용: 사용자가 직접 관련 사진으로 추가 업로드할 수 있음
  (※ 욕설과 비방 등의 문제 해결 방법 고안)
  => 일단 사진을 전송해두면 앱 업데이트 때 적절하다고 판단 시 반영해서 업로드

설정 탭: [설정/고객센터/도움말/공지사항]
		
  설정: 알림 소리 음량 조절, on/off 설정
	고객센터: 댓글 기능 활용 
    	앱 개발자에게 의견 전송, 오류 신고
    	이메일 제공(문서 형태)
  도움말: 문서 파일 활용
    	앱 사용법 정리 (일할 생각 있으면 게임 튜토리얼처럼 제작해볼까…)
    	각 문서마다 발생할 수 있는 문제상황에 대한 해결책 제공
    (필요하다면 링크 각주 달기, 최하단에 고객센터 링크 걸기)
  공지사항: 공적인 사항만 전달, 문서 형태
    	업데이트 날짜 및 현황
    	[고객센터]에서 수용된 의견 처리 결과 안내
    	개인적인 알림 사항은 [알림] 활용
