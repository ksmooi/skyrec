[ [English](high_precision_video_analysis_enus.md) ] [ 繁體中文 ]

# AIMS 影像分析的高精準度探索

## 簡介

在現代科技快速發展的背景下，影像分析技術已成為各種應用場景中的關鍵工具。高精準度的影像分析技術在各個領域中展示出其不可或缺的價值，無論是在人臉識別、人物穿著識別、車輛偵測，還是夜間影像分析等方面。本文將通過八個精選視頻，介紹 AIMS 在影像分析中的卓越精準度，展示其在不同場景和條件下的應用與挑戰。

AIMS 系統的核心模組是 AI Flow （pipeline），主要提供 AI 影像分析功能。AI Flow的主要特色包括：

- 支援彈性的 AI Flow 設定，可以根據需求調整 AI Flow 來達成各種任務。
- AI Flow 支援超過 40 種深度學習 (DL) 和 計算機視覺 (CV) 演算法，可以滿足各種不同的任務需求。
- 提供人性化的 AI Flow 設計工具，是無需編碼的工具 (No-Code Tool)，即使沒有演算法知識的人員也可以輕易使用。
- 提供完整的物件索引功能，大幅提升物件搜尋的性能。
- 整合高度自動化的 MLOps 流程，讓模型可以不斷自我學習，自動提升精準度與穩定性。

藉由這些先進的功能，AIMS在多樣的應用場景中提供高精準度的影像分析，確保其在不同條件下的有效性和可靠性。


## 戶外物件偵測 (Object Detection)

[![高精準度的戶外物件偵測](https://img.youtube.com/vi/v5wEM_DDUsU/0.jpg)](https://www.youtube.com/watch?v=v5wEM_DDUsU)

### 戶外物件偵測的常見應用

**車輛 (Vehicle)**
- 交通管理：監控交通流量，檢測違規行為。
- 停車管理：識別停車位是否被佔用。

**摩托車 (Motorcycle)**
- 交通執法：監控摩托車違規行為，如闖紅燈、逆行。
- 安全監控：識別未佩戴頭盔的騎乘者。
- 停車管理：監控摩托車停放區域。

**行人 (People)**
- 人流監控：計算行人流量，優化人流管理。
- 安全監控：檢測可疑行為，提升公共安全。

**頭部 (Head)**
- 人數統計：計算特定區域內的頭部數量，進行人數統計。
- 安全監控：檢測未佩戴安全帽的工人，保障工地安全。


### 影像分析上的挑戰

**時間段**
- **早晨 (Morning)**: 光線漸增，但可能有陰影和眩光問題，影響物體識別。
- **下午 (Afternoon)**: 光線充足，但強光和長陰影可能干擾分析。
- **傍晚 (Evening)**: 光線逐漸減少，需處理光線不足和陰影增多的情況。
- **夜晚 (Night)**: 光線微弱，依賴人工照明和紅外攝像機，挑戰包括噪點和動態範圍低。

**天氣條件**
- **下雨 (Raining)**: 雨水可能模糊鏡頭，反光增加，影像清晰度降低。
- **下雪 (Snowing)**: 雪花干擾視線，背景亮度增加，導致物體分辨困難。

**季節條件**
- **夏季 (Summer)**: 高溫可能影響攝像機性能，強光和熱氣流干擾影像穩定性。
- **冬季 (Winter)**: 低溫可能導致設備故障，雪和霜影響視覺清晰度。

這些條件下的影像分析需要應對各種環境變化和光線條件，以確保準確度和穩定性。AiMS 透過特殊的影像前處理方法，使深度學習有效偵測物件。


## 人臉偵測與識別 (Facial Analysis)

[![高精準度的人臉偵測與識別](https://img.youtube.com/vi/EKvrdf2Nc8k/0.jpg)](https://www.youtube.com/watch?v=EKvrdf2Nc8k)

### 人臉偵測與識別的常見應用

**人臉偵測 (Face Detection)**
- 店內走廊 (In-store Hallway)
- 店內手扶梯 (In-store Escalator)

**人臉分類 (Face Classification)**
- 口罩偵測 / 店面 (Mask / Storefront)
- 性別偵測 / 店面 (Gender / Storefront)
- 年齡偵測 / 店面 (Age / Storefront)

**人臉識別 (Face Recognition)**
- 店面 (Storefront)


### 影像分析上的挑戰

- 人臉擺動會降低偵測率
- 人臉移動速度太快會降低偵測率
- 人臉太小會降低識別精準度
- 人臉清晰度影響識別精準度
- 攝影機背光會降低識別精準度

AiMS 的人臉偵測與識別功能在設計軟體與深度學習模型時，已考慮到這些挑戰，因此我們的精準度相當高且穩定。


## 人物穿著識別 (Clothing Analysis)

[![高精準度的人物穿著識別](https://img.youtube.com/vi/gaAcQh8LOmo/0.jpg)](https://www.youtube.com/watch?v=gaAcQh8LOmo)

### 常見的人物穿著識別的應用

**偵測 (Detection)**:
- 室內 (Indoor)
- 室內 / 魚眼鏡頭 (Indoor / Fisheye)
- 街道 / 日間 (Street / Daytime)
- 夜視 / 下雨 (Night Vision / Raining)

**分類 (Classification)**:
- 性別 / 日間街道 (Gender / Daytime Street)
- 性別 / 夜視 (Gender / Night Vision)
- 上衣顏色 / 廣場 (Color of Upper Clothes / Plaza)
- 上衣類型 / 街道 (Upper Clothes Category / Street)
- 下衣顏色 / 街道 (Color of Lower Clothes / Street)
- 下衣類型 / 街道 (Lower Clothes Category / Street)

**識別 (Recognition)**:
- 人行道 / 冬季 (Sidewalk / Winter)
- 街道 / 夏季 (Street / Summer)

### 影像分析上的挑戰

**偵測 (Detection)**
- **室內 (Indoor)**: 照明變化和擁擠環境。
- **室內 / 魚眼鏡頭 (Indoor / Fisheye)**: 鏡頭畸變影響。
- **街道 / 日間 (Street / Daytime)**: 強光和陰影變化。
- **夜視 / 下雨 (Night Vision / Raining)**: 光線不足和雨水干擾。

**分類 (Classification)**
- **性別 / 日間街道 (Gender / Daytime Street)**: 多樣化穿著和背景干擾。
- **性別 / 夜視 (Gender / Night Vision)**: 光線不足。
- **上衣顏色 / 廣場 (Color of Upper Clothes / Plaza)**: 顏色相近物體分辨。
- **上衣類型 / 街道 (Upper Clothes Category / Street)**: 多樣化上衣樣式。
- **下衣顏色 / 街道 (Color of Lower Clothes / Street)**: 顏色變化和背景干擾。
- **下衣類型 / 街道 (Lower Clothes Category / Street)**: 多樣化下衣樣式。

**識別 (Recognition)**
- **人行道 / 冬季 (Sidewalk / Winter)**: 穿著臃腫和雪景干擾。
- **街道 / 夏季 (Street / Summer)**: 穿著多樣性和強光。


## 車輛偵測 (Vehicle Analysis)

[![高精準度的車輛偵測](https://img.youtube.com/vi/2Vd54eo3Hzs/0.jpg)](https://www.youtube.com/watch?v=2Vd54eo3Hzs)

### 車輛偵測的應用

**偵測 (Detection)**
- 低角度 / 白天
- 高角度 / 夜間

**分類 (Classification)**
- 車輛類型 / 白天
- 車輛類型 / 雪天
- 車輛類型 / 夜間
- 車輛顏色 / 高角度
- 車輛顏色 / 低角度

**識別 (Recognition)**
- 高角度
- 低角度

### 影像分析上的挑戰

**光線變化**
- 白天與夜間的光線差異，特別是低光環境下的識別。

**角度**
- 高角度和低角度拍攝可能會導致視角變形，影響識別精準度。

**天氣條件**
- 雨天和雪天的天氣影響，例如水滴或雪花模糊鏡頭。

**車輛遮擋**
- 交通擁擠或停車場中，車輛互相遮擋。

**車輛顏色與類型**
- 不同顏色和類型的車輛在分類和識別時的準確性。

**動態環境**
- 車輛高速移動會增加偵測和識別的難度。


## 夜間影像分析 (Night Vision)

[![高精準度的夜間影像分析](https://img.youtube.com/vi/SUcBZvLTtog/0.jpg)](https://www.youtube.com/watch?v=SUcBZvLTtog)

### 影像分析常見的情境

**偵測 (Detection)**
- 小雨 / 黑白
- 大雨 / 黑白
- 擁擠 / 黑白
- 逆光 / 黑白
- 低角度 / 大型物體 / 全彩
- 高角度 / 小型物體 / 全彩
- 下雪 / 低角度 / 大型物體 / 全彩

**分類 (Classification)**
- 人物性別 / 全彩
- 衣服顏色 / 全彩
- 衣服類型 / 全彩
- 車輛類型 / 小雨 / 黑白
- 車輛類型 / 大雨 / 黑白
- 車輛類型 / 低角度 / 全彩
- 車輛類型 / 高角度 / 全彩
- 車輛顏色 / 低角度 / 全彩
- 車輛顏色 / 高角度 / 全彩

**識別 (Recognition)**
- 低角度 / 大型物體 / 全彩
- 下雪 / 低角度 / 大型物體 / 全彩

### 影像分析上的挑戰
- 光線不足或光線變化
- 雨雪天氣對影像清晰度的影響
- 背光和陰影干擾
- 角度變形導致識別困難
- 高速移動物體的準確識別
- 多樣化穿著和物體類型增加了分類的難度


## 車輛識別 (Vehicle Recognition)

[![高精準度的車輛識別](https://img.youtube.com/vi/6UAjNELRPwY/0.jpg)](https://www.youtube.com/watch?v=6UAjNELRPwY)

### 影像分析常見的情境

**偵測 (Detection)**
- 低角度 / 白天
- 低角度 / 白天
- 高角度 / 夜間

**分類 (Classification)**
- 車輛類型 / 白天
- 車輛類型 / 雪天
- 車輛類型 / 夜間
- 車輛顏色 / 高角度
- 車輛顏色 / 低角度

**識別 (Recognition)**
- 高角度
- 低角度

### 影像分析上的挑戰

- 光線變化
- 角度變形
- 天氣影響
- 車輛遮擋
- 車輛顏色與類型
- 動態環境中的高速移動物體


## 人臉識別 (Face Recognition)

[![高精準度的人臉識別](https://img.youtube.com/vi/HO9UTJJ9K84/0.jpg)](https://www.youtube.com/watch?v=HO9UTJJ9K84)

### 影像分析常見的情境

- 正臉與側臉
- 有載眼鏡
- 無載眼鏡
- 戴載口罩
- 無載口罩

### 影像分析上的挑戰

- 不同光線條件下的準確度
- 不同面部遮擋情況（如眼鏡和口罩）
- 面部角度變化
- 移動中的面部識別
- 多人場景下的準確識別


## 人物識別 (Clothing Recognition)

[![高精準度的人物識別](https://img.youtube.com/vi/ldQYnIKDDNw/0.jpg)](https://www.youtube.com/watch?v=ldQYnIKDDNw)

### 人物識別常見的情境

在進行人物識別時，條件、拍攝角度、物體大小和交通流量都會對結果產生重要影響。以下是不同場景下的應用及其重要性：

| 場景 | 條件   | 拍攝角度 | 物體大小 | 交通流量 |
| ---- | ------ | -------- | -------- | -------- |
| 1    | 冬季   | 高       | 中       | 中       |
| 2    | 秋季   | 高       | 小       | 小       |
| 3    | 夏季   | 低       | 大       | 小       |
| 4    | 多雲天 | 低       | 中       | 小       |
| 5    | 多雲天 | 低       | 大       | 中       |
| 6    | 晴天   | 低       | 大       | 小       |
| 7    | 冬季   | 低       | 中       | 中       |
| 8    | 冬季   | 高       | 大       | 大       |
| 9    | 多雲天 | 低       | 大       | 大       |
| 10   | 多雲天 | 低       | 小       | 小       |
| 11   | 夏季   | 低       | 大       | 大       |
| 12   | 夏季   | 低       | 大       | 大       |

### 影像分析上的挑戰

- **光線變化**: 不同光線條件會影響影像的清晰度和識別準確度。
- **天氣條件**: 雨雪等惡劣天氣會干擾攝影機的視覺效果。
- **拍攝角度**: 高低角度可能導致物體變形，使識別變得困難。
- **移動中的物體**: 高速運動的物體容易模糊，增加識別難度。
- **多人場景的複雜性**: 在擁擠場景中區分個體更具挑戰。
- **背光和陰影干擾**: 背光和陰影可能遮蔽重要細節，影響識別效果。

