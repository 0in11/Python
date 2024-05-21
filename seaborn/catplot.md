 - catplot
   -     
    ```python
     #ex)
    g = sns.catplot(x="Sex", y="Age", data=train, kind="box",hue="Survived",
    col="Embarked", height=6)
    ```
        
   <img width="851" alt="%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-03-18_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_5 08 11" src="https://github.com/0in11/Python_library/assets/79905228/dc25b8db-a056-4bc2-99f8-23e35b59a872">
        
   - 필수
     - x: x축에 표시할 column
     - y: y축에 표시할 column
     - data: 사용할 DataFrame
     - kind: 그래프의 종류(”strip”,  “swarm”, “box”, “bar”, “violin”, “boxen”, “point”, “count”)
       - strip
       - swarm
       - box
                    
         ![boxplot](https://github.com/0in11/Python_library/assets/79905228/17052b21-6351-4f52-8c1b-f97dd1d38df0)
                    
         - 데이터의 분포를 상자 모양의 상자 안에 표시
         - Upper fense(최대값)
         - Lower fense(최소값)
         - Q1(1사분위수) : 전체 데이터의 25% 지점
         - **Q2(2사분위수)** : 전체 데이터의 50% 지점
         - Q3(3사분위수) : 전체 데이터의 75% 지점
         - 이상점(Outliers) : 특이한 분포를 보이는 이상치
         - 극단점 : 이상치 중에서 유달리 높거나 낮은 값을 보이는 특이한 데이터
       - bar
         - 데이터의 평균을 계산하고 표시, 단, estimator=sum으로 지정할시 합을 표시
         - violin
         - boxen
         - point
         - count
           - 각 범주별 데이터의 개수를 막대 그래프로 표시
       - distplot
         - 주로 연속형 데이터의 분포를 시각화하는데 사용
                    
           ```python
           sns.distplot(train["Fare"])
           ```
                    
           <img width="670" alt="%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-03-18_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_6 05 48" src="https://github.com/0in11/Python_library/assets/79905228/1b0e95fa-22d6-4f38-9f7d-0b030181ce1a">
                    
         - scatter
                    
                    
    - 옵션
      - hue: 범주형 데이터에 대해서 추가적인 분할
                
        ```python
        g = sns.catplot(x="Sex", data=train, kind="count", hue="Survived)
        g.set_ylabels("Counts")
        ```
                
        <img width="606" alt="%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-03-18_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4 53 36" src="https://github.com/0in11/Python_library/assets/79905228/9e65df9c-fbc8-415c-9986-1e654e4562f3">

                
      - col: column에 따라 그래프 분할
                
         ```python
         g = sns.catplot(x="Sex", data=train, kind="count", col="Survived")
         g.set_ylabels("Counts")
         ```
                
        <img width="875" alt="%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-03-18_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4 53 25" src="https://github.com/0in11/Python_library/assets/79905228/97c8c208-76dd-4e77-9653-61e36ee12518">
                
      - palette: 색상 팔레트
      - height: 그래프의 높이
      - order: x 데이터의 순서
      - hue_order: hue 데이터의 순서
      - aspect: 그래프의 종횡비
