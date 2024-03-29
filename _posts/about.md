---
layout: post
slug: hr example

---
기술 스택 요약
---
- 2D 게임 특화
- 게임(전투) 시스템
	- 프로토타이핑 
	- 스킬/버프 시스템 데이터 구조 설계 및 구현
- 최적화
	- 메모리 프로파일링을 통한 리소스 처리 구조 개선
- 개발 프로세스 개선
	- 클라이언트 빌드 출력 및 안티치트 툴 적용 프로세스 자동화
	- 회사 개발 프로세스에서 범용적으로 사용 가능한 클래스 명세 및 패키지화
	- 타 부서 요청 처리에 유용한 툴 구현
- 아트 리소스(유닛, 스킬 등) 구조 설계
	- 애니메이션(Spine Skeleton/Unity Animator) 구조 설계 및 조작 컴포넌트 구현
- 로그 및 리플레이
	- 인게임 전투 로그 관리 및 부정행위 탐지
	- 저장된 로그를 이용한 전투 리플레이
- 실시간 멀티플레이
	- Unity UNET / Photon / ProudNet
	- UNET을 이용한 실시간 멀티플레이 레이드/길드전 런칭 경험
- Unity 2D Advanced Feature 관련
	- 2D Lighting
	- ShaderGraph

---
마법스크롤 상인 지오 with NaverWebtoon

1. 전투 프로토타이핑
2. 최적화
- 앱 실행 직후 사용 메모리 1GB -> 680MB까지 절약
	- 광고 SDK 프리로드 관련 메모리 이슈 체크 및 처리(3개 SDK)
	- 리소스 압축 및 중복 리소스 이슈 체크
- 폰트 방식 변경
	- 글로벌 출시를 위한 다국어 지원 -> 언어별 텍스트 폰트 사용
	- TextMeshPro사용
	- static -> dynamic 방식으로 변경
- 그래픽 API
	- Vulcan / OpenGL2.0 / OpenGL3.0 우선순위에 따른 퍼포먼스 차이 이슈 확인 및 해결


전자오락수호대 Vol.2(Download 100M+) - 프로젝트 Rebuilding

1. 빌드 구조 재설계 
	- Client Base -> Server Base
		- 클라이언트에 데이터 파일 다운로드 -> 서버에서 데이터 모델 관리 방식으로 변경
		- 추가 다운로드/빌드 재배포를 통해야했던 데이터 변경을 서버 재시작으로 가능하게 구조 수정
	- Hard Coding -> Soft Coding
		- 유닛마다 개별 Prefab과 전용 함수로 이루어진 구조 개선
		- 기존 빌드에서는 불가능했던 기능 구현(Skin 시스템,  이펙트 변경)
	- Optimization
		- Resource Management / Object Pooling 
			- 기존 빌드 대비 메모리 사용량 30% 절약 달성
2. 기존 시스템 Refactoring
	- 기존 게임 시스템 / 컨텐츠 재구현


열렙전사 with NAVER WEBTOON / 각성 : 열렙전사

1. 기반 시스템
	- 외부 다운로드 구조 설계
	- 리소스 관리 시스템(Unity Addressables 사용)
	- 사운드 컨트롤
	- 로컬라이제이션
2. 전투 관련 시스템 
	- 유닛 조작 및 UI / 전투 판정 / 스테이지 중간 저장 / 승리 및 패배 처리
	- 스킬 및 버프 시스템
3. 실시간 멀티 플레이 - UNET HLAPI 기반(현 Unity Multiplay Networking)
	- 보스 레이드
		- 4인 동시 협동 보스 레이드 컨텐츠
		- 매치 메이킹 서버 기반
		- 페이즈 별 보스 패턴 구현
	- 길드전 - 20 vs 20
		- 최대 20 vs 20 실시간 길드전 컨텐츠
		- AI 몬스터 리젠 시스템 / 플레이어 참가 및 
		- 관전 시스템
4. 기타
	- 인게임 전투 로그
	- 맵 / 컷씬 제작 툴 구현



---
{: data-content="discussions"}

This article has been discussed here:
- [lobste.rs](#)
- [/r/webdev](#)

Feel free to reach out at my email to leave feedback and talk about the article.

---
{: data-content="footnotes"}

[^1]: a.k.a 3hreeman.
[^2]: Based on Unity Engine.
