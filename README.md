# Python-Term project

# 1. 주제 선정 이유
응급상황이나 자연재해 발생하였을 때에는 119소방서, 119안전센터 그리고 응급실 및 응급센터의 상호작용이 중요하다.&nbsp; 응급상황 시 119소방서와 119안전센터가 정확하게 신고를 접수받고 신속하게 응급차를 보내 인근 응급실로 환자를 이동시켜야 한다. 

응급상황이 발생하는 장소는 다양하므로 119소방서와 119안전센터 그리고 응급실 및 응급센터가 효율적으로 운영되어야 한다.

Term project를 통해 ___서울시와 경기도___ 에 한해서 119소방서와 119안전센터 그리고 응급실 및 응급센터가 효율적으로 분배되어 있는지 확인한다. 

만약 그렇지 못하다면 어떠한 해결책을 통해 문제를 해결할 수 있는지 프로젝트를 통해 알아보려고 한다.

# 2. 가설 정의
서울시와 경기도 의 119소방서, 119안전센터, 응급실 및 응급센터는 기존과 더불어 추가적으로 설치되어야 한다.

# 3. 인터넷을 통한 데이터 획득
### Term project에 사용된 데이터
```
'서울 열린데이터 광장'의 '서울시 소방서관할 위치정보 (좌표계_ WGS1984).csv'
'서울 열린데이터 광장'의 '서울시 안전센터관할 위치정보 (좌표계_WGS1984).csv'
'서울 열린데이터 광장'의 '서울시 응급실 위치 정보.csv'
'공공데이터포털'의 '경기도소방서현황및관할구역현황.csv'
'공공데이터포털'의 '응급의료기관및응급의료지원센터현황.csv'
'공공데이터포털'의 '전국 119안전센터 현황.csv'
```
서울시와 경기도의 119소방서, 119안전센터, 응급실 및 응급센터의 위치값을 가져오기 위해 위의 사이트들에서 csv 파일들을 다운로드 하였다. 

다루고 있는 데이터들의 좌표값(경도,위도)과 시설명, 주소들의 정확도가 중요하였기 때문에 csv파일 속 오류가 있는 경우에는 직접 파일을 수정하였다.

하지만 오류가 아닌 누락의 경우에는 다른 방식으로 해결하였다. 예를들어 경기도의 119안전센터의 경우 좌표값이 누락되어 있었다. &nbsp;이러한 경우에는 kakao api를 통해 주소값으로 좌표값을 얻어오는 방식으로 해결하였다.

# 4. 사용한 라이브러리
```
!pip install numpy                 # numpy 패키지
!pip install pandas                # pandas 패키지
!pip install folium                # folium 패키지
!pip install seaborn               # seaborn 패키지
!pip install -U scikit-learn       # scikit-learn 패키지
!pip install branca                # branca 패키지(folium 보조)
!pip install pyOpenSSL             # pyOpenSSL 패키지
!pip install haversine              # haversine 패키지 
!pip install ndg-httpsclient
```
