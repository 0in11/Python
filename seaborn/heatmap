- seaborn
    - heatmap
        
        ```python
        #feature들 간의 corr()을 heatmap으로 보여줌
        sns.heatmap(train[["Survived","SibSp","Parch","Age","Fare"]].corr()
        ,annot=True, fmt = ".2f", cmap = "coolwarm")
        ```
        
        - 데이터(Data) : 이차원 배열 or DataFrame
        - corr() : 각 column 사이의 상관관계를 계산하여 correlation matrix 반환
            - 1에 가까운 값 : 한 변수가 증가할 때 다른 변수도 증가하는 경향이 있음
            - 0에 가까운 값 : 두 변수 사이에 상관관계 x
            - -1에 가까운 값 : 한 변수가 증가할 때 다른 변수는 감소하는 경향이 있음
        - cmap : heatmap의 색상 지정 ex) viridis, coolwarm, YlGnBu
        - annot : heatmap의 각 셀에 값을 표시할지 여부를 지정, 기본값은 False(값 표시 X)
        - fmt : 셀 안의 값의 표시 형식 지정 ex) .2f ⇒ 소수점 2자리까지
        
        <img width="559" alt="%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-03-15_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_3 59 56" src="https://github.com/0in11/Python_library/assets/79905228/1a24c377-420e-43dd-82e8-0e93644cad7b">
