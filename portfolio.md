# 최종 학력

한국기술교육대학교 컴퓨터공학부 졸업 (2020년 2월)

# 경험한 기술 스택 및 숙련도
(상 : 언어의 내부 구조를 이해하고 효율적으로 문제 해결을 할 수 있다. / 중 : 문제 해결을 위해 필요한 자료구조, 알고리즘등을 이용하여 문제를 해결할 수 있다.  / 하 : 기본 문법을 알고 있고 검색을 통해 문제를 해결할 수 있다.
  1. 파이썬
     - 19년도 서비스지향컴퓨팅 최종 웹 프로젝트와 알고리즘 문제풀이에 사용중인 언어입니다.
      - 숙련도 : 중
  2. C/C++ 
     - 대학 재학 시절 대부분의 프로젝트에 사용한 언어 입니다. 
      - 숙련도 : 하
  3. C# 
     - 유비샘 현장실습 중 기기 - PC - 서버 를 연결하는 게이트웨이 프로젝트에 사용한 언어입니다.
      - AR 수업 최종 프로젝트로 IBM의 STT를 이용하여 대화내용을 AR 텍스트로 보여주는 프로젝트에 유니티에서 사용한 언어입니다.
      - 숙련도 : 하
  4. 자바 
     - 미세먼지 현항 Web, 안드로이드 쿡북 App에 사용한 언어입니다.
      - 숙련도 : 하

# 모든 개발 관련 경험

## 블로그

https://justnoob.tistory.com/
PS 풀이, 유명 알고리즘 등을 정리

## Github

https://github.com/Just-NB?tab=repositories
대학 재학시절 프로젝트 정리

## 프로젝트 경험 및 느낀점(배운점)

  1. 미세먼지 현황 Web (2021년 05월)
     - 프로젝트 요약 : 사용자의 현재 위치(GPS기준)에서 가장 가까운 미세먼지 측정소를 에어코리아 Open API로 찾아 미세먼지 측정량을 받아와 보여주는 웹 사이트 개발 프로젝트 였습니다
      - 맡은 역할 : 백엔드 - 에어코리아의 Open API를 받아오는 역할
      - 사용 언어 : 백엔드 - Java Spring Boot, MySql
      - 자세한 내용 :
        네이버 날씨와 같은 사이트에서 제공하는 미세먼지 현황 사이트를 개발해보았습니다. 저는 open api를 통해 모든 미세먼지 측정소의 측정 데이터를 2시간 간격으로 자동으로 받아오도록 하였고 사용자의 현재 위치를 받아오면 그 위치에서 가장 가까운 미세먼지 측정소를 open api를 통해 받아오는 작업을 하였습니다.
        이 작업을 하면서 저는 2가지 트러블이 있었습니다.
        하나는 open api의 하루 제공량은 500~1000회 정도였지만 모든 측정소의 개수가 500개 가량 되어 2시간 간격으로 모든 측정소의 측정값을 가져오는데 문제가 있었습니다. 이 문제에 당면했을때 팀 회의를 통해 저는 "아마 우리 프로젝트는 실제 사용자가 얼마 없을 것이니, 모든 측정소의 측정값을 한번에 다 받아오는 구조가 아니라 A 측정소의 값을 ㄱ 사용자가 최초 요청을 했을때, A 측정소의 데이터를 가져와 DB에 저장하고, A측정소 값을 요청하는 새로운 사용자가 생겼을 때 DB에서 꺼내오는 방식 으로 하자" 하였고, 제 동료는 "우리 프로젝트가 실제 사용자가 얼마 없을지 몰라도, 많은 사람들이 이용하는 것을 목표로 하는것이 좋으니 모든 데이터를 한번에 받자" 하였습니다. 둘의 의견이 갈렸기에 어떤 방식으로 할지 남은 팀원들과 함께 고민해 보았고 각 방법의 문제점들이 어떤것이 있을지 생각해 보았습니다. 그 결과 제 방식에는 "만약 A 측정소의 값을 2주전에 받아왔고 현재는 A측정소가 고장난 상태일 때 사용자는 2주전 데이터를 보게된다" 라는 문제점이 있었고 모든 데이터를 한번에 받는 경우는 open api 운영계정으로 신청할 경우 요청량이 증가하기 때문에 해결할 수 있다는 결론이 나와 모든 데이터를 한번에 받는 방향으로 진행하였습니다.
        다른 하나는 open api에서 데이터를 항상 정상적으로 보내줄것이라 예상하고 예외처리를 하지 않아 발생하였습니다. 코드를 작성하면서 혹시 데이터를 잘못 보내주지 않을까? 하는 생각을 잠깐 했었지만 설마 잘 못 보내주겠어? 하는 생각으로 예외처리를 하지 않았었고 api사용량 초과로 인한 잘못된 데이터를 받아왔을때 에러가 생겼고, 에러처리를 제대로 하지 않아 디버깅 하는데 시간이 많이 걸렸습니다.
      - 배운 점(느낀점) : 저는 보통 친구들과 프로젝트를 하면 제 주장에 힘을 많이 주는 편이였습니다. 하지만 이번 프로젝트를 진행하면서 함께 토의하며 좀 더 옳은 방향이 어느것인지 알아가는 과정의 중요함을 알게 되었습니다. 또한 귀찮다는 이유로 예외처리를 무시하여 넘어갔던 것에 반성하게 되었습니다. 당연하다 생각한것이 당연하지 않을 수 있음을 알게되었고, 앞으로는 좀 더 꼼꼼한 개발을 하도록 마음다짐하게된 계기가 되었습니다.
      - 프로젝트 이미지 

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https://blog.kakaocdn.net/dn/2J6Hw/btq7FG0Pe6G/RXqXSaXpgb7GC4V5IGUCek/img.png" alt="enter image description here" style="zoom: 40%;" />



2. 신재생 에너지 REST OPEN API (2019년 12월)
   - 프로젝트 요약 : 기상청의 Open API와 전력거래소의 CSV파일을 이용하여 새로운 데이터를 창조하고, 이 데이터를 이용한 샘플 웹 사이트를 제작하는 프로젝트였습니다.
   - 맡은 역할 : 2인 프로젝트로 ,저는 DB의 값을 REST API로 CLIENT에게 보내주고 그 데이터와 부트스트랩을 이용하여 샘플 웹 사이트 제작하는 역할을 담당했습니다
   - 사용 언어 : 파이썬(플라스크), 부트스트랩
   - 자세한 내용 : 
     서비스지향컴퓨팅 수업의 최종 프로젝트였습니다. 목표는 기존의 데이터를 이용하여 새로운 데이터를 창출해내고, 그것을 REST API로 제공하였을때 어떻게 이용할 수 있는가를 제시하는 것이였습니다. 팀원은 새로운 데이터를 만들고 DB에 저장하고 꺼내는 것을 만들어 주었습니다. 저는 DB에서 꺼낸 데이터를 rest api로 제공하고, 제공하였을때 어떻게 사용할지를 보여주는 웹 사이트를 만들었습니다. 웹 사이트는 총 4페이지로 프로젝트 소개를 위한 메인 페이지, 저희가 제공하는 api의 설명서 페이지, 제공하는 api를 사용할 때 받는 데이터를 보여주는 페이지, 제공하는 api를 사용하여 만들 수 있는 샘플 페이지를 만들었습니다. UI적인 요소는 부트스트랩을 이용하여 해결하였습니다. 메인 페이지에서는 전체적인 프로젝트 소개를 위한 ppt를 carousel 형태로 보여주었고, 샘플페이지에서는 chart.js를 사용하여 데이터를 시각화 하였습니다.
   - 배운점(느낀점) : 이 프로젝트를 하면서 막연히 써오기만한 REST API란 무엇인지 배웠고 처음사용해본 언어인 파이썬을 이용하여 프로젝트를 완수한것처럼 지금까지 배워왔던 지식들이 있다면 새로운 언어 환경 이더라도 개발할 수 있을거라는 자신감을 얻을 수 있었습니다.
   - 프로젝트 이미지

<img src="https://user-images.githubusercontent.com/26599463/118591324-f53d7380-b7de-11eb-84ce-c0cb544434ae.png" alt="웹 사이트 첫 페이지" style="zoom:50%;" />



3. CUDA를 이용한 2D Video to 3D StereoScopic Video 변환 (2019년 12월)
   - 프로젝트 요약 : openCV로 고화질의 비디오를 CPU가 입력받아 GPU에게로 보내주고, GPU는 받은 데이터로 Barrel Distortion을 적용하여 3D 스테레오스코픽 영상으로 만들고 CPU에게 다시 돌려주어 변환된 영상을 openCV로 저장과 출력을 하는프로젝트였습니다.
   - 맡은 역할 :  2인 프로젝트로 저는 openCV로 영상을 입력받고 GPU에게 영상을 보내주는 역할을 담당하였습니다.
   - 사용 언어 : C++(CUDA)
   - 자세한 내용 : 
     처음에는 단순하게 openCV로 받은 Mat형식의 데이터를 char 2D 배열로 변환시켜 그대로 GPU에게 보내주었습니다. 단순한 과정이였기에 생각보다 금방 끝났고 과제의 핵심은 어떻게 가속화를 시키느냐 였기에 좀 더 좋은 방법이 없을까 고민했습니다. 그러던 중 openCV로 영상을 받아온 Mat 형식의 데이터는 BGRBGRBGR이 반복되는 형식인것을 알게 되었고 이런 방식 그대로 GPU에게 넘겨준다면 coalesced하지 못한 메모리 접근으로 성능 저하가 있게 된다는것을 알게되었습니다. 이를 해결하기 위해 Mat형식의 파일을 2D 배열로 단순하게 바꾸는 것이 아닌 B,G,R 각각의 데이터만을 저장할 3채널의 char 1D 배열을 만들어 GPU로 보내주었습니다. 또한 영상 변환을 위한 전처리 과정에서 openMP를 이용하여 CPU에서의 병렬처리를 추가하여 조금 더 성능향상을 성공했고 최종적으로 CPU만 이용할 경우 1 프레임 변환에 48ms 걸린것에 반해 CUDA를 적용하여 11ms의 시간이 걸려 약 4배 이상의 속도향상을 이뤄냈습니다.
   - 배운점(느낀점) : 이 프로젝트를 수행하면서 병렬 프로그래밍의 지식 뿐 아니라 오픈 라이브러리를 사용할 때 단순히 함수를 사용하는 것을 넘어서, 그 내부 구조를 이해하는것이 프로젝트 성과에 유효한 영향을 끼친다는 것을 알게 되었습니다. 그리고 다른 과목에서 배운 개념을 적용해보기도 하고, 겉에 드러난 부분을 넘어 메모리 안에서의 동작을 생각하며 개발해본 좋은 경험이였습니다.
   - 프로젝트 이미지 

<img src="https://user-images.githubusercontent.com/26599463/118616656-db128e00-b7fc-11eb-9c7c-9b5ac2b95fd9.png" alt="enter image description here"  />



4. 가상머신 시뮬레이터 (유비샘 현장실습) (2019년 1월)

   - 프로젝트 요약 : PC에서 Data를 서버에 보내어 각 Data별 시나리오를 진행 후, 결과를 웹 페이지에 출력하는 프로젝트였습니다
   - 맡은 역할 : 3인 프로젝트로 저는 팀장으로 C#을 이용한 시리얼 통신, TCP 통신과 서버를 모두 보았습니다.
   - 사용 언어 : 클라이언트 - C# / 서버 - php
   - 자세한 내용 : 서버쪽은 완성시키지 못해 성공적으로 완수시키지 못판 프로젝트입니다. PC쪽은 2가지 파트로 구분되었습니다. 하나는 가상머신의 컨트롤러, 다른 하나는 컨트롤러의 데이터를 서버로 전송시키는 게이트웨이였습니다. PC파트는 모두 C#을 이용하였고, 가상머신의 컨트롤러는 com2com이라는 프로그램을 통해 가상 시리얼 포트를 생성하고 이 포트를 게이트웨이와 연결하였습니다. 게이트웨이는 가상머신 컨트롤러와는 시리얼 통신, 서버와는 TCP 소켓 통신을 하였습니다. 서버에서는 컨트롤러에서 받아온 데이터별로 제공된 시나리오에 따라 새로운 데이터를 출력하였습니다.
   - 배운점(느낀점) : 멘토분들에게 질문하는것의 중요성을 알게 되었습니다. 기업에서 처음으로 한 아르바이트로 사장님께서는 항상 상사 분들께 모르는거 여쭤보라고 강조하셨고 실제로 여쭤보았을때 모든 분들이 친절하고 자세하게 알려주셨습니다. 하지만 제가 상사분들이라는 이유 하나만으로 지레 겁을 먹고 질문을 하지 않은 결과 프로젝트를 성공적으로 완수하지 못한것이라 생각이 들었습니다. 이 문제점을 깨닫고 복학 후 교수님과 랩 연구원들과 함께 스터디를 하며 상사분과의 심리적 거리감을 좁히도록 노력했습니다

   

5. 안드로이드 쿡북 App (2017년 12월)
   - 프로젝트 요약 : 네이버 STT를 이용하여 음성으로 화면을 이동할 수 있는 안드로이드 쿡북 어플리케이션개발 프로젝트 였습니다.
   - 사용 언어 : 안드로이드(JAVA)
   - 프로젝트 이미지 

 <img src="https://user-images.githubusercontent.com/26599463/118635048-241f0e00-b80e-11eb-95d2-5156a86f9dd4.png" alt="enter image description here" style="zoom:50%;" />
