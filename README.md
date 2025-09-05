# 📘 N8N ile Ücretsiz YouTube Scraping  
*(Scraping YouTube for FREE with N8N)*  

---

## 📑 İçindekiler / Table of Contents  
1. 🎯 Amaç / Goal
2. 🛠️ Ön Hazırlık / Prerequisites
3. 📍 Adım Adım Eğitim / Step-by-Step Tutorial
   - 🔑 API Key Alma / Getting API Key  
   - ⚙️ Workflow Kurulumu / Building the Workflow  
   - 📊 Kanal ve Video Bilgilerini Getirme / Fetching Channel & Video Data  
   - 📑 Google Sheets Entegrasyonu / Exporting to Google Sheets  
   - 🔎 Analiz ve Kullanım / Data Analysis  


---

## 🎯 Amaç / Goal  

**TR:** Bu eğitimde, **N8N** kullanarak YouTube’dan ücretsiz veri çekmeyi öğreneceğiz.  
**EN:** In this tutorial, we’ll learn how to **scrape YouTube data for free using N8N**.  

**Amacımız / Our Goal:**  
- **TR:** YouTube’daki kanalları ve videoları bulmak, istatistiklerini almak, Google Sheets’e kaydetmek.  
- **EN:** Find YouTube channels/videos, fetch statistics, and store results in Google Sheets.  

---

## 🛠️ Ön Hazırlık / Prerequisites  

**TR:**  
- Bir **Google Cloud hesabınız** olmalı.  
- **YouTube Data API v3** etkinleştirilmeli.  
- **N8N kurulmuş** ve çalışıyor olmalı.  

**EN:**  
- You must have a **Google Cloud account**.  
- **YouTube Data API v3** must be enabled.  
- **N8N** must be installed and running.  

---

## 📍 Adım Adım Eğitim / Step-by-Step Tutorial  

### 🔑 Adım 1: API Key Alma / Step 1: Get API Key  

**TR:**  
1. [Google Cloud Console](https://console.cloud.google.com/) adresine gidin.  
2. Yeni bir proje oluşturun.  
3. **API & Services** bölümünden **YouTube Data API v3**’ü etkinleştirin.  
4. **Credentials** kısmından bir **API Key** oluşturun.  

**EN:**  
1. Go to [Google Cloud Console](https://console.cloud.google.com/).  
2. Create a new project.  
3. Enable **YouTube Data API v3** from **API & Services**.  
4. Generate an **API Key** under **Credentials**.  

---

### ⚙️ Adım 2: Workflow Kurulumu / Step 2: Build Workflow  

**TR:**  
1. N8N’de yeni bir workflow açın.  
2. Bir **HTTP Request** node ekleyin.  
   - URL:  
     ```
     https://www.googleapis.com/youtube/v3/search
     ```
   - Parametreler:  
     - `part=snippet`  
     - `q=fitness` (örnek arama kelimesi)  
     - `maxResults=5`  
     - `key=YOUR_API_KEY`  
3. Workflow’u çalıştırın → İlk sonuçları göreceksiniz.  

**EN:**  
1. Create a new workflow in N8N.  
2. Add an **HTTP Request** node.  
   - URL:  
     ```
     https://www.googleapis.com/youtube/v3/search
     ```
   - Parameters:  
     - `part=snippet`  
     - `q=fitness` (example search term)  
     - `maxResults=5`  
     - `key=YOUR_API_KEY`  
3. Run the workflow → You’ll see the results.  

---

### 📊 Adım 3: Kanal & Video Bilgilerini Getirme / Step 3: Fetch Channel & Video Data  

**TR:**  
- Kanal ID’si ile yeni bir **HTTP Request** node oluşturun.  
- URL:  https://www.googleapis.com/youtube/v3/channels
- - Parametreler:  
- `part=statistics`  
- `id=CHANNEL_ID`  
- `key=YOUR_API_KEY`  
- Böylece abone sayısı, toplam izlenme ve video sayısı alınır.  

**EN:**  
- Create a new **HTTP Request** node with a channel ID.  
- URL: https://www.googleapis.com/youtube/v3/channels
- Parameters:  
- `part=statistics`  
- `id=CHANNEL_ID`  
- `key=YOUR_API_KEY`  
- This retrieves subscribers, views, and video counts.  

---

### 📑 Adım 4: Google Sheets Entegrasyonu / Step 4: Export to Google Sheets  

**TR:**  
- Bir **Google Sheets** node ekleyin.  
- Kanal adı, abone sayısı, toplam izlenme, popüler video gibi bilgileri kaydedin.  

**EN:**  
- Add a **Google Sheets** node.  
- Save channel name, subscribers, total views, and top videos.  

---

### 🔎 Adım 5: Analiz ve Kullanım / Step 5: Data Analysis  

**TR:**  
- Popüler kanalları bulun.  
- Ortalama performansı ölçün.  
- Çok iyi performans gösteren videoları tespit edin.  

**EN:**  
- Find popular channels.  
- Measure average performance.  
- Identify high-performing videos.  

---

## ✅ Sonuç / Conclusion  

**TR:** Artık N8N ile YouTube verilerini ücretsiz toplayabilir ve analiz edebilirsiniz.  
**EN:** Now you can use N8N to scrape YouTube data for free and analyze it.  



---

 

