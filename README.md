# 📰 Fake News Detection – Sahte Haber Tespit Sistemi

Bu proje, kullanıcıdan alınan **Türkçe veya İngilizce haber metinlerini** analiz ederek *doğruluğunu tahmin eden* ve neden o şekilde sınıflandırıldığını açıklayan bir yapay zeka sistemidir. Model, sahte haberle mücadele amacıyla geliştirilmiştir.

---

## 🎯 Proje Amacı

Günümüzde internet ortamında hızla yayılan doğruluğu şüpheli haberlerin tespiti oldukça önemlidir. Bu sistem:

- Bir haberin **"Gerçek"** mi yoksa **"Sahte"** mi olduğunu belirler
- Sonuca dair **kaynak destekli açıklamalar** sunar
- Kullanıcının **metin veya URL** girmesine olanak tanır

---

## 🧰 Kullanılan Teknolojiler

| Teknoloji/Kütüphane       | Açıklama                                      |
|---------------------------|-----------------------------------------------|
| Python                    | Ana programlama dili                          |
| Transformers              | DistilBERT modeli için                        |
| Datasets                  | Eğitim verilerinin hazırlanması               |
| Scikit-learn              | Veri ayırımı ve metrik hesaplamaları          |
| Gradio                    | Web arayüzü                                   |
| BeautifulSoup             | URL'den metin çekimi                          |
| Wikipedia API             | Alternatif açıklama kaynağı                   |
| GoogleSearch-Python       | Güvenilir kaynaklardan arama yapılması        |

---

## 🧠 Model Özeti

- **Model:** distilbert-base-multilingual-cased  
- **Diller:** Türkçe ve İngilizce  
- **Eğitim Süresi:** 4 Epoch  
- **Doğruluk:** %95.5 (dengelenmiş test verisi)  
- **Tokenizer ile birlikte kaydedildi**

---

## 📁 Klasör Yapısı

```

fakeNewsDetector/
├── distilBert\_model/          → Tahmin ve model dosyaları
│   └── saved\_model/           → Eğitilmiş model + tokenizer
├── explanation/               → Açıklama motoru ve cache
│   └── fact\_checker.py
├── FakeDetectAI/              → Web arayüzü (Gradio)
├── data/                      → Temizlenmiş veri setleri
│   ├── dataSet\_TR\_cleaned.csv
│   └── dataSet\_EN\_cleaned.csv
└── requirements.txt           → Gerekli kütüphaneler

````

---

## 🚀 Nasıl Çalıştırılır?

### 1. Gerekli Kütüphaneleri Kurun
```bash
pip install -r requirements.txt
````

### 2. Terminal Üzerinden Tahmin Yapmak İçin

```bash
cd distilBert_model
python predict.py
```

### 3. Web Arayüzünü Çalıştırmak İçin

```bash
cd FakeDetectAI
python web.py
```

---

## 🔎 Açıklama Sistemi Nasıl Çalışır?

* Tahminin ardından sistem:

  * Güvenilir kaynaklardan (*bbc.com, cnn.com, who.int, wikipedia.org*) haberle ilgili **destekleyici ya da çürütücü içerik** arar
  * İçerik bulunamazsa **Wikipedia özetini** döner
  * Sonuçta kullanıcıya **açıklama + kaynak linki** sunar

---

## 📋 Geliştirme Durumu

* ✅ Model eğitildi
* ✅ Açıklama mekanizması geliştirildi
* ✅ Web arayüzü çalışıyor
* ✅ URL ve metin girişleri destekleniyor

---

## 📜 Lisans

Bu proje tamamen **eğitim amacıyla** geliştirilmiştir. Herhangi bir haber kuruluşu ya da medya platformu ile ilişkili değildir.
