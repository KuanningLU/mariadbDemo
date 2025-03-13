# MariaDB Demo 後端

## MariaDB Demo
本專案是一個使用 **Node.js + TypeScript** 開發的後端 ，主要透過 **MariaDB** 進行資料庫存取，並使用 **Postman** 進行 API 測試。

## 技術選用
- **Node.js** 
- **MariaDB**
- **Postman** 
- **DBeaver EE** 

## 安裝套件
### 1. 安裝依賴
```sh
npm install
```

### 2. 設定環境變數
改成自己的密碼
```
DBHOST = 127.0.0.1
DBPORT = 8974
DBUSER = root
DBPASSWORD = ********
SVPORT = 2083
LogPath = logs
assetsPath = /assets
HomePagePath = /index.html
```

### 3. 啟動伺服器
```sh
npm run dev
```

## 資料庫設定
### 1. 建立資料庫與資料表
 SQL 指令：
```sql
CREATE DATABASE lab_b310;
USE lab_b310;

CREATE TABLE Reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT NOT NULL,
    seat_id INT NOT NULL,
    timeslot_id INT NOT NULL,
    create_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## API 端點
### 1. 測試資料庫連線
- **方法**: `GET`
- **URL**: `http://localhost:2083/`
- **回應範例**:
```json
[
  {
    "reservation_id": 1,
    "student_id": 411630000,
    "seat_id": 5,
    "timeslot_id": 2,
    "create_time": "2025-03-13T10:00:00.000Z"
  }
]
```
