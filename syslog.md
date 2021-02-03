# 💬 Syslog

* 로깅 메세지 프로그램의 표준.

* Syslog는 다양한 프로그램들이 생성하는 메세지들을 저장하고, 메세지들을 이용해서 다양한 분석 등이 가능하도록 로그 메세지들을 제공한다. 

      프로그램 뿐만 아니라 device와 같은 장비들도 Syslog를 사용할 수 있도록 제공.
      관리자는 device 장비에서의 로그 메세지들을 통해 문제사항이나, 성능 등을 확인할 수 있다.

* 컴퓨터 시스템의 관리, 보안 알림 뿐만 아니라 일반적인 정보, 분석, 디버깅 메세지 등을 제공해준다. 프린터나 라우터와 같은 다양한 장비 뿐만 아니라 다양한 플랫폼을 지원한다.

      이런 이유로 syslog는 중앙 저장소에 다양한 타입의 시스템들의 로그 데이터의 저장소로 사용됨.

* Syslog에서는 메세지를 생성해내는 주체(facility)에 따라 다음과 같이 나눈다.

      auth, authpriv, daemon, cron, ftp, lpr, kern, mail, news, syslog, user, uucp, local0.. local7

<img src="https://user-images.githubusercontent.com/62328584/106685338-8c553580-660b-11eb-8655-b1d05869e95e.JPG" width="600px" height="450px"></img><br/>
      
* 메세지의 우선순위 / 메세지 중요도(level)에 따라 다음과 같이 나뉘어 진다.

      Emergency, Alert, Critical, Error, Warning, Notice, Info or Debug

      Emergency = 응급상황, 시스템 전면중단 -우선순위1
      Alert = 즉각적인 조치가 필요  -우선순위2
      Critical = 하드웨어 등의 심각한 오류발생  -우선순위3
      Error = 일반적인 에러/ 오류   -우선순위4
      Warning = 경고 메세지 -우선순위5
      Notice = 에러나 오류는 아니나, 관리자의 조치가 필요   -우선순위6
      Info = 의미 있는 정보 관련 메시지 -우선순위7
      Debug = 디버깅용 메시지   -우선순위8
      * = 모든 상황의 메세지    -우선순위9

      ▶각 우선순위들은 포함관계를 나타낸다.
      ex)
      -9단계인 *는 모든 메시지를 의미함.(1부터 9까지의 모든 상황을 포함.)   
      -8단계인 debug는 1부터 8까지의 상황을 모두 포함한다. 