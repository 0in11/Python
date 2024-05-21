
-  FacetGrid
    -
    ```python
    g = sns.FacetGrid(data=train,col="Survived")
    g.map(sns.histplot,"age")
    ```
    
    - 데이터: 사용할 DataFrame
    - 행(row): 데이터를 행(row)로 분할하는데 사용할 행(row)의 이름
    - 열(col): 데이터를 열(column)로 분할하는데 사용할 열(column)의 이름
 
