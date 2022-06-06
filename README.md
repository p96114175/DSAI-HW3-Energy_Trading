# DSAI-HW3-Energy_Trading

# data analyze

target0 ~ target49 為50戶家庭1~8月用電量資訊，接著針對target0 ~ target49 進行平均以消除偏差值，得出以下結果，用於協助判斷分析

![consumption_avg](https://user-images.githubusercontent.com/102530486/172163056-7ba5bf54-9770-47c5-946c-948eff6ae447.png)

![generation_avg](https://user-images.githubusercontent.com/102530486/172163069-c019a0c3-2909-41e2-a156-9a3e039efec1.png)

![both_avg](https://user-images.githubusercontent.com/102530486/172163558-57ccddf1-9ed2-4e27-aec0-e064594bacb3.png)


    從上圖可發現，1~4月產電量高於用電量，從4月以後用電量呈現上升的狀態，4~8月處於用電量高峰期，呈現用電量高於產電量的狀態

# Trade Strategy

## 每日交易策略

    每日電量狀態 = 每日用電量-每日產電量
    每日電量狀態 > 0 決策為 action = 'buy'
    每日電量狀態 < 0 決策為 action = 'sell'
   
## 每日交易價格

根據採取行動之差異(action)，所設定的交易價格有所不同

     當 action = 'buy' 
     交易價格 = 1.5
     當 action = 'sell'
     交易價格 = 2
# Run the code

在pipenv環境下執行main.py Python版本為:Python 3.8

    pipenv install --python3.8

    pipenv shell

在pipenv直接執行main.py:

    pipenv run python main.py

安裝套件:

    pipenv install requests
