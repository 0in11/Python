- `figure`()
    - 
    - 복수 개의 그림을 동시에 그리고 싶을 때
    - 그림의 크기, 해상도 등의 속성을 직접 지정하고 싶을 때
    
    ```python
    #Example
    picher_features_df = picher[['승', '패', '세', '홀드', '블론', '경기', '선발', '이닝', '삼진/9',
           '볼넷/9', '홈런/9', 'BABIP', 'LOB%', 'ERA', 'RA9-WAR', 'FIP', 'kFIP', 'WAR',
           '연봉(2018)', '연봉(2017)']]
    
    #피처 각각에 대한 히스토그램 출력
    def plot_hist_each_column(df):
        plt.rcParams['figure.figsize'] = [20,16]
        fig = plt.figure(1)
        
        for i in range(len(df.columns)):
            ax = fig.add_subplot(5, 5, i + 1)
            plt.hist(df[df.columns[i]], bins = 50)
            ax.set_title(df.columns[i])
        plt.show()
    plot_hist_each_column(picher_features_df)
    ```
    
    ```python
    figure(num, figsize, dpi, facecolor, edgecolor, frameon)
    #num : 그림(figure)의 번호 저장
    #figsize : 그림의 크기 저장, 단위는 인치
    #dpi : 그림의 해상도 저장
    #facecolor : 그림의 배경석 지정
    #edgecolor : 그림의 테두리색 지정
    #frameon : 그림의 테두리를 그릴지 여부 결정
    ```
    
    ![figure](https://github.com/0in11/Python_library/assets/79905228/c526526c-960f-4787-b0fa-5c6f3399bcbc)

    
    - `fig.add_subplot`(nrows, ncols, index) : 그림(figure)을 nrows x ncols로 나누고 index번째 위치에 서브플롯 추가
    - **`plt.hist`**는 히스토그램을 그릴 때 현재 활성 그림(figure)과 서브플롯(subplot)에 그립
- `rcParams` : 그래프의 기본 스타일, 폰트, 크기, 색상, 축의 레이아웃, 마진, 마커 스타일 등과 같은 다양한 그래프 설정을 조정
    - 
    
    ```python
    plt.rcParams['figure.figsize'] = [10, 6]  # 그래프 크기 설정
    plt.rcParams['axes.titleweight'] = 'bold'  # 그래프 제목 글꼴을 굵게 설정
    plt.rcParams['axes.grid'] = True  # 축에 그리드를 표시
    ```
