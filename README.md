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

## 🔎 Açıklama Sistemi Nasıl Çalışır?

* Tahminin ardından sistem:

  * Güvenilir kaynaklardan (*bbc.com, cnn.com, who.int, wikipedia.org*) haberle ilgili **destekleyici ya da çürütücü içerik** arar
  * İçerik bulunamazsa **Wikipedia özetini** döner
  * Sonuçta kullanıcıya **açıklama + kaynak linki** sunar

---

## 📜 Lisans

Bu proje tamamen **eğitim amacıyla** geliştirilmiştir. Herhangi bir haber kuruluşu ya da medya platformu ile ilişkili değildir.
