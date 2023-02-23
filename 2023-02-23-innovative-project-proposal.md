---
layout: post
title: Innovative Project Proposal
author: [Toto Chen]
category: [Lecture]
tags: [jekyll, ai]
---

This homework is to specify a INnovative Project Proposal and describe the key features, list all Design Considerations and the required technologies, then draw the System Block Diagram.

---
## Futre Home Applications

### Nextflix movie: Big Bug
<iframe width="993" height="559" src="https://www.youtube.com/embed/FWUkh23vBhs" title="BIGBUG Trailer (2022)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

**Service Robots:**<br>

![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_robots.png?raw=true)

---
**Home Spaces:**<br>

![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_spaces.png?raw=true)

---
### Homework Report
**Contents:**<br>
* **應用與功能說明**
  - Specify the future home application, and Describe the key features
  - Describe the key features which may be applied to the home space (kitchen, living room, play room, study room, bed room)
* **設計考量與所需相關技術**
  - List all design considerations and the required technologies
* **系統方塊圖**
  - Draw a System Block Diagram
<iframe width="1280" height="720" src="https://www.youtube.com/embed/C5ZnJYRwllE" title="今天也很舒適，也很舒適🌼祝您有美好的一天|內心的平靜" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
---
## 家用飛行機器人
### 應用功能說明
1. 居家監控：外出時可隨時查看家裡各處狀況
2. 環境監測：溫濕度感測+瓦斯偵測+空氣品質偵測 
3. 清潔環境：撢灰塵, 除臭
4. 丟棄垃圾：丟棄小型垃圾袋至垃圾車或社區資源回收區
5. 餐飲服務：遞送調味料, 可樂, 水果, 零食

### 設計考量與相關技術
**系統設計考量：**<br>
1. 移動方式:共軸雙旋翼
2. 供電方式:電池＋自動充電
3. 聯網方式: WiFi 或 BLE to中控電腦

**所需相關技術：**
1. 飛行姿態偵測與控制: ESP32 + MPU6050 + PID controller
2. 溫濕度感測 & 氣體偵測: HTU21D + MQ2 + MQ7 + MQ135
3. 紅外線遙控: IR-LED 
4. 影像傳輸: ESP32-CAM模組
5. 物品夾具：懸吊掛勾, 磁鐵吸吊
6. 服務器: 具AI加速(GPU)
  - 影像物件偵測辨識: CSL-YOLO
  - 任務規劃控制: Mission Planner with Floorplan

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/FutureHome_flying_robot.png?raw=true)

---
## 花房照護機器人
### 應用功能說明
1. 查看各植物生長情形
2. 溫濕度感測+二氧化碳感測+照度感測
3. 噴霧器施肥+澆水
4. 遙控照明裝置
5. 雷射殺蟲

### 設計考量與相關技術
**系統設計考量：**<br>
1. 移動方式:共軸雙旋翼
2. 供電方式:電池＋自動充電
3. 聯網方式: WiFi

**所需相關技術：**
1. 飛行姿態偵測與控制: ESP32 + MPU6050 + PID controller
2. 溫濕度感測 & 空氣品質感測: HTU21D + MQ135
3. 紅外線遙控: IR-LED 
4. 影像辨識: Jetson Nano + IMX219(攝影頭)
5. 服務器: SmartPhone + Cloud database
   - 任務規劃與控制: Mission Planner with Floorplan

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_greenhouse_keeper.png?raw=true)

---
## 料理機器人
### 應用功能說明
1. 操作廚具：咖啡機＋果汁機＋烤麵包機＋微波爐+烤箱+氣炸鍋
2. 存取冰箱：辨識食物, 存放食材，或取出食材, 送至廚具

### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:垂直升降式手臂 or 懸吊式手臂
2. 移動方式:兩輪 or 滑軌懸吊
3. 供電方式:鋰電池
4. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 滑軌式機器手臂 ＆ 軟式夾具
2. 食物辨識分類：Jetson-Nano + IMX219
3. 電子鼻：氣味感測與辨識 MQ2

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/FutureHome_kitchen_robot.png?raw=true)

---
## 早晨喚醒系統
### 應用功能說明
1. 照度偵測
2. 藍牙手環監測睡眠品質,並保存睡眠動態紀錄
3. 手勢偵測與遙控
3. 鬧鐘喚醒功能：播放預設音檔.Wav, 或播放網路電台(PAM8403+8ohm speaker)
4. 遙控電動窗簾：紅外線遙控 (IR-LED)
5. 操控燈光：智慧燈泡＋手勢辨識 (TinyML)

### 設計考量與相關技術
**系統設計考量：**<br>
1. 感測方式:照度,手環動態及手勢
2. 供電方式:音箱用有線電源,手環用電池
3. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 照度感測: ADC界面讀取光敏電阻(GL5516)
2. 睡眠品質監測：藍牙穿戴式手環(ESP32+MPU6050), 運用三軸加速器偵測睡眠動態
3. 手勢偵測：MPU6050感測手勢動作之三軸加速器數值, 利用TinyML進行AI手勢辨識
4. 網路電台播放：ESP32 Internet Radio player
5. 智慧燈泡連接：AWS Alexa介接, 或藍牙命令操控燈光

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_morning_alarm_system.png?raw=true)

---
## 互動伴學機器人
### 應用功能說明
1. 外語學習
2. 學齡前遊戲互動

### 設計考量與相關技術
**系統設計考量：**<br>
1. 移動方式：球形滾動
2. 供電方式：鋰電池
3. 互動方式：LCD顯示模組 + 語音輸出入 + 肢體動作 + 指頭操作
4. 作業系統：採用Android OS

**所需相關技術：**
1. 影像物件識別： 執行 CSL-YOLO模型進行辨識(Jetson Nano)
2. 語音辨識與輸出： Speech Recognition & Text-To-Speech (AppInventor 2)
3. 外語教學：AI對答
4. 指頭操作：觸控 & 吸盤式電磁頭
5. 互動教具：字卡, 跳棋, ...

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_companion_robot.png?raw=true)

---
## Design Methodology (設計方法)
* Top-Down Design  ：由上層應用分析再區分出下層個別功能及所需軟硬體設計
* Bottom-Up Design ：由底層軟硬體元件往上組合出上層所需應用功能

---
## Market Analysis (市場分析)
![](https://blog.hubspot.com/hs-fs/hubfs/tam-sam-som.png?width=1200&name=tam-sam-som.png)

---
### TAM of Future Home Products
The Target Market size (TAM) of Future Home Products is the number of household.<br>

---
### Taiwan Households = 8.93M (台灣 9百萬戶）
* [Total number of households in Taiwan from 2010 to 2020(in 1,000s)](https://www.statista.com/statistics/330804/taiwan-national-total-number-of-households/#:~:text=By%20the%20end%20of%202020,households%20in%20the%20previous%20year.)

### Japan Households = 57.2M (日本 5千7百萬戶)
* [Number of Households in Japan](https://www.helgilibrary.com/indicators/number-of-households/japan/) 

### South Korea Households = 19.9M (南韓 2千萬戶)
* [Number of Households in South Korea](https://www.helgilibrary.com/indicators/number-of-households/south-korea/)

---
### American Households = 129.93M (美國 1.3億戶)
* [Number of households in the U.S. from 1960 to 2021(in millions)](https://www.statista.com/statistics/183635/number-of-households-in-the-us/)<br>
* [The average American household consisted of 2.51 people in 2021.](https://www.statista.com/statistics/183648/average-size-of-households-in-the-us/)<br>

---
### [Number of private households in selected European countries in 2020](https://www.statista.com/statistics/868008/number-of-private-households-in-the-eu/)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Households_number_Europe2020.png?raw=true)
* Germany households = 40,120.9K **(德國 4千萬戶)**
* France households  = 30,304K **(法國 3千萬戶)**
* United Kingdom households = 27,792K **(英國 2千8百萬戶)**
* Italy households = 26,079K **(義大利 2千6百萬戶)**
* Turkey households = 24,920.1K **(土耳其 2千5百萬戶)**
* Spain households = 18,793.9K **(西班牙 1千9百萬戶)**
* Poland households = 14,723.6K **(波蘭 1千5百萬戶)**

---
### Germany Households = 40.546M (in 2020)
* [Number of households in Germany from 2000 to 2020, by size(in 1,000)](https://www.statista.com/statistics/464187/households-by-size-germany/) 
  - one person: 16,476K
  - two persons: 13,778K
  - three persons: 4,915K
  - four persons: 3,970K
  - five persons: 1,407K
  
---
### France Households = 29.7M 
* [Number of Households in France](https://www.helgilibrary.com/indicators/number-of-households/france/)
* The average household size in France in 2020 is **2.2** people per household.

---
### UK Households = 28.267M 
* [Number of Households in UK ](https://www.ibisworld.com/uk/bed/number-of-households/44090/)
* [Number of households in the United Kingdom in 2020, by type of household(in 1,000s)](https://www.statista.com/statistics/961002/households-in-the-united-kingdom-uk-by-type/)<br>

---
### Canada Households = 10.5M (加拿大 1千萬戶)
* [Number of families in Canada from 2006 to 2021(in millions)](https://www.statista.com/statistics/443323/families-in-canada/)

### Mexico Households = 34.8M (墨西哥 3千4百萬戶)
* [Number of Households in Mexico](https://www.helgilibrary.com/indicators/number-of-households/mexico/) 

---
### Brazil Households = 72.4M (巴西 7千2百萬戶)
* [Number of households in Brazil from 2012 to 2019(in 1,000s)](https://www.statista.com/statistics/870646/brazil-number-households/)

### Argentina Households = 13.8M (阿根廷 1千3百萬戶)
* [Number of Households in Argentina](https://www.helgilibrary.com/indicators/number-of-households/argentina/)

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


