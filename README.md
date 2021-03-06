# Magic-formula : 마법공식 백테스트
조엘 그린브란트의 책, '주식시장을 이기는 작은 책'에 나오는 마법 공식을 Python 환경에서 구현해보고, 과거 데이터로 백테스트하기 위한 코드입니다.

### 사용 데이터
1. 주가 데이터 : https://github.com/FinanceData 에서 제공하는 marcap 데이터를 사용합니다.
2. 재무제표 데이터 : 크롤링을 통하여 얻은 제조업의 재무제표를 정리한 csv 파일을 사용합니다.(자세한 항목은 아래와 같습니다.)
3. 종목 데이터 : 제조업에 해당하는 종목만 정리해 놓은 리스트입니다.

재무제표 데이터에는 다음과 같은 자료가 들어있습니다.
* Date : 분기/연도 표시
* 구분 : Y-연도, Q-분기, CY-연속4분기
* 코드 : 종목코드
>손익계산서 항목
* 매출, 매출총이익, 영업이익, 금융수익, 금융원가, 이자비용, 기타수익, 기타비용, 종속/관계기업손익, 세전계속사업이익, 법인세비용, 중단영업이익, 당기순이익, 지배주주순이익, 비지배주주순이익
>대차대조표 항목
* 자산총계, 유동자산, 재고자산, 매출채권및, 현금및현금성자산, 비유동자산, 유형자산, 무형자산, 부채총계, 유동부채, 단기차입금, 매입채무및, 비유동부채, 자본총계, 지배주주지분, 자본, 자본잉여금, 이익잉여금, 비지배주주지분
>현금흐름표 항목
* 영업활동현금흐름, 당기손순익, 현금유출없는비용가산, 감가상각비, 무형자산상각비, 현금유입없는수입차감, 운전자본변동, 기타영업활동현금흐름, 투자활동현금흐름, 투자활동현금유입, 투자활동현금유출, 유형자산의증가, 기타투자활동현금흐름
* 재무활동현금흐름, 재무활동현금유입, 재무활동현금유출, 기타재무활동현금흐름, 현금및현금성자산증가, 기초현금및현금성자산, 기말현금및현금성자산

재무제표 데이터
![fs_data](https://user-images.githubusercontent.com/33973546/77590051-35cd9400-6f30-11ea-95c4-a8fcb029afda.PNG)


결과

2,000만원을 가지고 1년에 한번 20종목을 조정하는 규칙으로 2004년 4월 1일부터 2019년 3월 31일까지의 결과입니다. 연평균 수익률은 14%입니다.

![fs_test_year](https://user-images.githubusercontent.com/33973546/77818247-53f3e980-7114-11ea-81b2-433322f5279b.PNG)

