# DENEME🚲 NYC Citi Bike Analizi: Kentsel Mobilite Optimizasyonu

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Data-Analysis-green)
![Status](https://img.shields.io/badge/Status-Tamamlandı-success)

> **Proje Özeti:** Bu çalışma, New York şehrindeki bisiklet paylaşım sisteminin verimliliğini artırmak ve talep dengesizliklerini analiz etmek amacıyla yapılmıştır.

---

## 1. Projenin Amacı
New York gibi metropollerde ulaşım yoğunluğu büyük bir sorundur. Citi Bike sistemi bu soruna çözüm olsa da, bazı istasyonların sabahları **boş**, akşamları ise **aşırı dolu** olması verimsizlik yaratmaktadır.

Bu projede şunları hedefledik:
1.  Kullanıcı davranışlarını analiz etmek (Abone vs. Turist).
2.  En yoğun rotaları tespit etmek.
3.  **Talep Tahmini (Demand Forecasting)** yaparak operasyonel öneriler sunmak.

---

## 2. Veri Seti Hakkında (Dataset)
Kullanılan veri seti **[Yıl/Ay]** dönemine aittir ve yaklaşık **[X Milyon]** satır veriden oluşmaktadır.

| Değişken Adı | Açıklama |
| :--- | :--- |
| `tripduration` | Sürüş süresi (saniye) |
| `start_station_name` | Başlangıç istasyonu |
| `end_station_name` | Bitiş istasyonu |
| `usertype` | Customer (Günlük) veya Subscriber (Yıllık) |

---

## 3. Veri Görselleştirme ve Analiz

### A. Haftalık Kullanım Yoğunluğu (Heatmap)
Aşağıdaki grafik, haftanın günlerine ve saatlerine göre bisiklet kullanım yoğunluğunu göstermektedir.
*(Buraya Python ile çizdiğin grafiğin resmini ekle: `![Heatmap](grafik1.png)`) Code kısmından 'Add file' diyerek resmi yüklemeyi unutma!*

**Bulgu:** Hafta içi sabah 08:00 ve akşam 17:00-18:00 saatlerinde (iş giriş-çıkış) zirve yaşanırken, hafta sonları kullanım gün içine yayılmaktadır.

### B. En Popüler İstasyonlar
En çok başlangıç yapılan istasyonların harita üzerindeki dağılımı:
*(Buraya harita görselini ekle)*

---

## 4. Endüstri Mühendisliği Yaklaşımı: Sorun & Çözüm

### 🔴 Tespit Edilen Sorun (Darboğaz)
Yaptığımız analizde, Manhattan merkezindeki istasyonların sabah saatlerinde **%95 doluluk** oranına ulaştığı ve kullanıcıların bisiklet bırakacak yer bulamadığı tespit edilmiştir.

### 🟢 Önerilen Çözüm
Kamyonetlerle yapılan bisiklet dağıtımının (Rebalancing) şu rotalar üzerinden yapılması önerilmektedir:
* **Rota A:** 8. Cadde -> Times Square (Sabah 07:00 - 09:00 arası)
* **Rota B:** Central Park -> Finans Merkezi

---

## 5. Kullanılan Teknolojiler
Bu projede aşağıdaki kütüphaneler kullanılmıştır:
* **Veri İşleme:** Pandas, NumPy
* **Görselleştirme:** Matplotlib, Seaborn, Folium
* **Analiz:** Scikit-Learn (Kümeleme/Clustering analizi için)

---

