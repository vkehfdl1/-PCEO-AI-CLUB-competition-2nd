사고관련 column

'Start_Time', 'End_Time', 사고가 영향 주기 시작한 시간 그리고 종료 시간
'Start_Lat', 'Start_Lng', 'End_Lat', 'End_Lng', Lat는 위도 Lng는 경도
'Distance(mi)' 사고의 영향을 받는 도로의 범위 'Description' 사고 경위
사고 경위에서 문자열만 잘 다룬다면 엄청나게 도움이 될 것 같긴 합니다.

여기부터 address field 즉 사고가 일어난 곳과 관련된 이야기

'Number' 도로번호 'Street' 거리이름 'Side' 주소지 거리의 오른쪽인지 왼쪽인지(미국의 시스템은 잘 모르겠습니다. 혹시 어떤 의미인지 아시면 공유좀..)
'City', 시 < 'County' 카운티,< 'State' 주. 캘리포니아만하니 의미없음. 'Zipcode' 약간 우편번호감성 'Country' 나라. 의미 없음.,
'Timezone' 시간대. 캘리포니아 에서만 다루므로 의미없음.

여기부터 날씨 관련

'Airport_Code' 사고장소에서 가장 가까운 공항 기상 관측소 'Weather_Timestamp' 기상 관측 기록 타임스탬프'Temperature(F)' 온도 'Wind_Chill(F)'체감온도(f(T,풍속))
'Humidity(%)' 습도 'Pressure(in)'기압 'Visibility(mi)' 가시거리
'Wind_Direction' 풍향 'Wind_Speed(mph)' 풍속
'Precipitation(in) 강수량 'Weather_Condition' 날씨 상태

여기부터 POI 관련. (Points of interest 사고 지점 근처에 이 시설들이 있었는지)

'Amenity' 편의 시설. 예를 들어 수영장, 백화점 등등 그런 시설
'Bump' 과속방지턱 'Crossing' 강 기차 도로 등 길과 교차하는 것, 그런데 아마 횡단보도로 추정 'Give_Way' 양보표지판
'Junction' 등급이 같은 도로 간의 교차로
'No_Exit' 막다른 길 'Railway' 철도
'Roundabout' 회전교차로 'Station' 기차역 'Stop' 정지표지판,
'Traffic_Calming' 트래픽을 진정시키는 것들. mini bump나 도로 바닥에 그려진 행동유도 패턴 등등 bump보다 약한 녀석들
'Traffic_Signal' 신호등 'Turning_Loop' 회전해 나올 수 있는 곳이다.

여기부턴 시간대. 정확히는 해가 떴는지 안 떴는 지를 여러 기준으로 나타내고 있음.
'Sunrise_Sunset 일출 일몰에 기반한 주야 'Civil_Twilight' 칼럼명 기반 주야 'Nautical_Twilight' 수평선 등 바다기준
'Astronomical_Twilight'우주적
상대적으로 이 순서대로 밤이 짧음. 이 네가지 칼럼은 합쳐서 5단계로 만드는 게 좋을 듯
![Twilight](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b4/Twilight-dawn_subcategories.svg/450px-Twilight-dawn_subcategories.svg.png)

![image](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Twilight_subcategories.svg/450px-Twilight_subcategories.svg.png)

# 'Severity' 예측값입니다
# 시간과 도로에 미친 영향을 바탕으로 함.

by DongGeon Han