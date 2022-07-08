# 첫번째 머신러닝 프로젝트
## 주제
미세먼지 농도를 측정하여 마스크 종류별 추천

## 주제 선정이유
한창 코로나19사태가 조금 누그러들어져 마스크착용에 대한 부담감이 조금 줄어든 시점에서, 
다시한번 마스크를 착용해야하는 사건이 찾아온다.
바로 늦겨울에서 봄사이에 발생하는 미세먼지라는 친구가 그 사건이다.
요놈의 미세먼지는 육안으로 보이지도 않지만, 그 미세먼지중에서 더 작은 초미세먼지들은
여러 기관지증상에 큰 영향을 미친다. 
평소 우리가 사용하는 일방적인 마스크들도 여러 종류의 차이가 있고
종류가 다양한 만큼 각각의 성능에도 크던 작던 차이가 존재하는데, 
미세먼지농도가 큰 날을 측정하여 그 농도에 걸맞는 마스크종류를 추천해주는 모델을 구성해보고 싶었다.

#### 데이터출처
환경부 : http://www.me.go.kr

에어코리아(실시간 대기환경) : https://www.airkorea.or.kr/web/

#### 데이터형태
불필요한칼럼, 결측치 제거 전

<img width="276" alt="기상청데이터" src="https://user-images.githubusercontent.com/98293871/177761376-90f8991a-27c7-4381-9702-40cb82652dc7.png">




#### 데이터형태
불필요한칼럼, 결측치 제거 후

<img width="268" alt="기상청데이터2" src="https://user-images.githubusercontent.com/98293871/177761752-7528074c-f7c3-41b5-990e-8973bd65e906.png">




#### EDA로 상관관계확인
![output](https://user-images.githubusercontent.com/98293871/177899970-ce285c47-b69b-4ae8-bae3-d216a63d80bf.png)


##처음 가설을 세울 때 풍속,강수량이 미세먼지에 영향을 줄 것이라 생각하여 가설을 세웠지만,
해당 pairplot을 보면 큰 영향을 끼치지 못한다는걸 깨달았음.



#### 모델을 활용하여 분석(DecisionTreeClassfier,tree)
![tree1](https://user-images.githubusercontent.com/98293871/177900387-1cec4102-c3b5-4d65-8780-1a670101737b.png)

![tree2](https://user-images.githubusercontent.com/98293871/177900393-7f3cfc5c-4906-4f0d-9596-6da10fdc2715.png)



#### 모델을 활용하여 분석(RandomForestClassifier)
<img width="473" alt="2022-07-08" src="https://user-images.githubusercontent.com/98293871/177911742-c71e50fe-08f3-40fd-b44e-b8189c77b3b7.png">

<img width="382" alt="2022-07-08 (1)" src="https://user-images.githubusercontent.com/98293871/177914067-94192915-0c23-468b-80fc-8f1641bb6e08.png">


