# 5G MEC를 활용한 실시간 음악 협업 서비스

## 아이디어 개발 목적 및 의의
포스트 코로나 시대에는 원격 협업을 위해 줌, 구글 미트 등 온라인 화상회의 서비스가 활발히 활용되고 있습니다. 
하지만 이러한 서비스는 오디오 지연 시간 문제로 인해 음악 협업에는 사용할 수 없습니다.
따라서 **지연 없이 사용할 수 있는 온라인 음악 협업 서비스**가 필요했습니다.

**5G MEC**를 활용해 개별 PC 성능과 네트워크 환경에 영향을 받지 않는 안정적인 음악 협업 서비스를 제공하는 것을 목표로 하고 있습니다.  
음악 협업에 최적화된 서비스를 활용하면 밴드, 뮤지컬, 오케스트라 등에서 음악을 연주하기 위해 많은 사람이 한 곳에 모여야 하는 불편함을 해소하고, 원격 협업의 편의성을 제공할 수 있습니다.

## 아이디어 개발 내용 및 범위
- **5G 네트워크**를 활용하여 충분한 대역폭을 제공하며, MEC 서버를 사용하여 지연 시간을 최소화합니다.
- **SFU 방식**을 사용하여 미디어 서버를 MEC 서버에 업로드하고 클라이언트의 미디어 스트림을 중계합니다.
- 중앙 서버에는 웹 서버, 데이터베이스, TURN 서버를 배치합니다.
- **MEC 서버**를 사용하여 엣지단에서 콘텐츠를 처리함으로써 실시간 성능을 제공하고 지연 시간을 줄입니다.
- 5G MEC와 SFU 기반의 미디어 서버를 활용하여 저지연이며 동시에 다수의 사용자가 접속 가능한 화상회의 서비스를 개발합니다.

## 역할 담당
**고범수**: PM, 백엔드-webRTC 화상 채팅, 리팩토링 <a href="https://github.com/GoBeromsu">@GoBeromsu</a>    
**김명지**: 백엔드-webRTC 화상 채팅, 컨트롤러 구현, 리팩토링, Docker 환경 구축 <a href="https://github.com/Starlight258">@Starlight258</a>     
**김지민**: 프론트엔드- 웹 만들기, Docker 환경 구축  <a href="https://github.com/kimjimin00">@kimjimin00</a>   
**류한일**: 백엔드-media device I/O 처리, 동기화 알고리즘 구현 <a href="https://github.com/cooopang">@cooopang</a>        
  

## 개발 결과
- **5G MEC 서버**를 활용한 저지연 음악 협업 서비스를 완성했습니다.
- **NodeJS 기반의 WebRTC 실시간 온라인 협업 애플리케이션**을 제작했습니다.
- 웹 서버, 데이터베이스, TURN 서버는 중앙 서버에 배치하고 미디어 서버는 MEC에 배치하여 **엣지에서 콘텐츠를 처리**함으로써 실시간 성능을 제공하고 지연 시간을 줄였습니다.
- MEC 미디어 서버는 **도커 컨테이너 환경**에서 운영되어 가벼운 서비스 배포와 이동성을 제공합니다.
- 5G MEC 테스트 환경에서는 4인 기준 지연시간이 2ms로 측정되어 고품질, 저지연 협업이 가능했으며, 기존 서비스 대비 향상된 품질을 확인했습니다.

결론적으로 **5G MEC를 활용해 개인 PC 성능과 네트워크 환경에 영향을 받지 않는 안정적인 음악 협업 서비스**를 제공했습니다.

## Preview
![image](https://user-images.githubusercontent.com/78211281/224594008-192069d5-a996-4e74-89a1-36f8d2318bbb.png)

<iframe width="560" height="315" src="https://www.youtube.com/embed/YgTgkBeZmn4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
