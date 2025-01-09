TransactionID: 각 거래 식별하는 ID
TransactionDate: 거래가 발생한 시간 정보, 날짜 명시는 안되어있고 시간정보만 포함
Amount: 거래 금액을 나타내며, 해당 거래에 사용된 금액
MerchantID: 거래에 참여한 상인을 고유하게 식별하는 ID
TransactionType: 거래 유형을 나타내며, refund(환불) 또는 purchase(구매)로 표시
Location: 거래가 이루어진 지리적 위치(도시)
IsFraud: 해당 거래가 사기인지 여부를 나타내는 이진 변수로, 0은 사기가 아님, 1은 사기임을 의미

#   Column           Non-Null Count   Dtype  
---  ------           --------------   -----  
 0   TransactionID    100000 non-null  int64  
 1   TransactionDate  100000 non-null  object 
 2   Amount           100000 non-null  float64
 3   MerchantID       100000 non-null  int64  
 4   TransactionType  100000 non-null  object 
 5   Location         100000 non-null  object 
 6   IsFraud          100000 non-null  int64  
dtypes: float64(1), int64(3), object(3)

결측치 없음 ㄷㄷ


제안 1: 거래 패턴 분석
문제 정의:
 거래 데이터(TransactionID, TransactionDate, Amount, MerchantID, TransactionType, Location)를 분석하여 특정 지역 또는 상점에서의 거래 패턴을 탐색합니다.
목표:
시간대별 거래량 및 금액 변화 탐구
특정 지역에서 자주 발생하는 거래 유형 분석
평균 거래 금액 및 이상치 탐지
배경:
 거래 패턴을 이해하면 판매 촉진 캠페인을 적절한 시간과 장소에 최적화할 수 있으며, 고객의 소비 습관을 파악할 수 있습니다.