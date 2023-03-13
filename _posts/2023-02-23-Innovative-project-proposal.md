---
layout: post
title: Innovative Project Proposal
author: [賴柏邑]
category: [Lecture]
tags: [jekyll, ai]
---

This homework is to propose an innovative project and describe the key features, list all Design Considerations and the required technologies, then draw the System Block Diagram.

---
## Homework Report Format
**Contents:**<br>
* **應用與功能說明**
  - Specify the future home application, and Describe the key features
  - Describe the key features which may be applied to the home space (kitchen, living room, play room, study room, bed room)
* **設計考量與所需相關技術**
  - List all design considerations and the required technologies
* **系統方塊圖**
  - Draw a System Block Diagram

---
## 物品運送裝置
### 應用功能說明
1. 收納物品：有掛勾和托盤可以放置書包、衣物、用具、電器等
2. 定點遙控傳輸物品：可用手機指定時間將所需物品送達指定位置  ex:廚房到客廳、客廳到臥室等
4. 物品辨識:自動歸納出已儲存物品的項目並整理成表

### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:手機遙控
2. 移動方式:滑軌懸吊
3. 供電方式:鋰電池
4. 聯網方式:WiFi

**所需相關技術：**
1. 滑軌移動軌道、掛勾、托盤
2. 滑軌控制:ESP32
3. 影像辨識：Jetson-Nano + IMX219
4. 服務器: SmartPhone + Cloud database
5. 任務規劃與控制: Mission Planner with Floorplan

### 系統方塊圖
![](https://github.com/phantom3035/MCU-HW/blob/main/images/%E7%A5%9E%E5%A5%87%E6%96%B9%E5%A1%8A%E5%9C%96.png?raw=true)



<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


