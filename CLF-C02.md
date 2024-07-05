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

## What is AWS Regions

[Regions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-regions)

 a cluster of [Data centers](https://aws.amazon.com/tw/what-is/data-center/)
 ![alt text](image.png)

並且也包含只針對某些區域提供的服務 [AWS Regional Services](https://aws.amazon.com/tw/about-aws/global-infrastructure/regional-product-services/?p=ngi&loc=4)

一個Regions由三個以上的AZs組成

## AWS Availability Zones (AZs) 可用區域

每個AZ都由額外一個或多個的數據中心組成，用於提升容錯，也可以將應用程式從單個AZ擴展到多個，AZ之間是低延遲的

is composed of one or more discrete data centers with redundant power, networking, and connectivity, and are used to deploy infrastructure

## Region v.s. AZs

[Regions and Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)

| 特性      | Region  | Availability Zone (AZ)       |
|-----------|---------|------------------------------|
| **定義**  | 一個地理區域，包含多個獨立的Availability Zones。 | Region內的一個或多個獨立的物理數據中心。 |
| **目的**  | 提供服務和數據的地理隔離。 | 增加冗餘和高可用性，以防單個數據中心故障。 |
| **隔離**  | 不同Region間是完全隔離的。 | 同一Region內的AZs透過低延遲的連結互相連接，但彼此物理隔離。 |
| **連接**  | Region間通常透過互聯網或專用網路連接。 | AZ之間通過高速私有光纖連接。 |
| **用途範例** | 可根據法律、政策或延遲需求選擇適合的Region。 | 在同一Region內部署應用，以透過多個AZ達到高可用性。 |

## 全球範圍（Global Scope）v.s. 區域範圍（Regional Scope）

| 特性           | 全球範圍 (Global Scope)  | 區域範圍 (Regional Scope) |
|---------------|--------------------------|----------------------------|
| **定義**       | 服務配置和管理在所有Regions間共享。 | 服務配置和管理限定在單個Region內。 |
| **數據共享**   | 數據和設置是全球統一的。 | 數據和設置是依Region分開管理的。 |
| **連接性**     | 服務不受地理位置限制，可在全球範圍內訪問。 | 服務通常只能在配置的Region內訪問。 |
| **管理**       | 通過一個中央點管理，方便全球操作和監控。 | 需要在每個Region分別進行管理和配置。 |
| **範例服務**   | IAM, Route 53, CloudFront | EC2, RDS, VPC |
| **主要優勢**   | 管理簡化，全球統一的策略和設置。 | 促進地理隔離，增強災難恢復能力，符合地域法規。 |
