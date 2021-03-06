# 知識_KNN

###  KNN (K(個數) nearest neighbor)

 採用測量不同特徵值之間的距離方式，進行分類
 
 - 歐肌理得距離(Euclidean Distance)  
            
            
    <img src="http://chart.googleapis.com/chart?cht=tx&chl= dist(x,y)= \sqrt{\sum_{i=1}^n(x_i - y_i)^2}" style="border:none;">

    距離越近，資料越相同。
   
  　空間複雜度與時間複雜度大，因為要批次逐步運算。
  
 　　<img src="KNN_Base.png" width="500">
   
 `sklearn`: Google出錢給與當時大學生的代碼，已維護十年的函式庫 ，沒有深度學習

 - 曼哈頓距離(Manhattan distance or Manhattan length)

  我們可以定義曼哈頓距離的正式意義為L1-距離或城市區塊距離，

  也就是在歐幾里得空間的固定直角坐標系上兩點所形成的線段對軸產生的投影的距離總和。
  算出ｙ軸與Ｘ軸的總和

<img src="http://chart.googleapis.com/chart?cht=tx&chl= d(x,y)= \left| x_1 - x_2\right|  %2B  \left|y_1 - y_2\right|" style="border:none;">

<img src="Manhattandistance.png" width="300">
