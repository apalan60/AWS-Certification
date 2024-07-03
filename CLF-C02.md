# Q&A

## How WebSites Work

客戶端輸入一段網址後，透過網路，將封包、資料、IP位置傳遞至伺服器的所在IP，伺服器也可根據請求，將資料傳回給客戶端

## 伺服器(Server)由什麼組成

CPU, RAM, Data, Network(Routers, Switch, DNS server)

## 如何把訊息透過網路傳遞至伺服器

透過[數據機(Moden)](https://zh.wikipedia.org/wiki/%E8%B0%83%E5%88%B6%E8%A7%A3%E8%B0%83%E5%99%A8)把電腦/手機的數字訊號轉換為類比訊號
-> (Optional)Router負責在內網和外網之間轉發數據包
-> 傳遞至ISP(網路基礎建設供應商)建立的基地台
-> 資料從網際網路傳回時，數據機將類比信號重新轉換回數字信號

- [Chat](https://chatgpt.com/share/8e727e30-a768-4961-9154-a9183bc31ede)
- [Modem vs Router](https://www.youtube.com/watch?v=Mad4kQ5835Y)

## What is Cloud Computing

提供一種按需求獲取的計算資源、儲存空間、應用程式等IT資源，自選適當的規格、數量，並付對應的價錢

當使用者要操作Web Application時，AWS會提供對應網路連接所需的硬體

Dropbox(儲存空間)、Netflix(影片服務)皆算是日常生活中可見的雲端服務

## 雲端有哪幾種部屬模型

Private Cloud: 私有雲，運作環境是專屬於一個組織或企業私人使用的 e.g. racksapce

Public Cloud: 公有雲，將計算資源公開給多租戶使用 e.g. AWS, GCP, Azure

Hybrid Cloud: 混合雲，保留一些地端的Server，但也採用公有雲的服務，同時維護Infra來保存敏感資產、但也不失雲端的靈活性
