# Gıda Tedarik Zincirinde Otonom Karar Veren Çoklu Ajan Tabanlı Dinamik Fiyatlandırma Sistemi 🤖🍟

Bu proje, küresel bir sorun olan gıda israfına karşı, gıda tedarik zinciri süreçlerine otonom karar verme yeteneği kazandıran **Çoklu Ajan Tabanlı (Multi-Agent System)** bir dinamik fiyatlandırma ve lojistik modelidir.

---

## 📝 Proje Bilgileri
* **Kurum:** Burdur Mehmet Akif Ersoy Üniversitesi (MAKÜ), Bucak Bilgisayar ve Bilişim Fakültesi, Yazılım Mühendisliği Bölümü
* **Proje Türü:** Bitirme Projesi / Yazılım Mühendisliği Mühendislik Etiği Çalışması
* **Tarih:** Aralık 2025
* **Geliştiriciler:** Mervan Kaya, Nurullah Kılıç, Ahmet Eren Özdemir
* **Danışman:** Doç. Dr. İhsan Pençe

---

## 🎯 Küresel Sorun ve Amaç
Dünyada üretilen gıdanın yaklaşık 1/3'ü tüketiciye ulaşmadan çöpe gitmektedir. Mevcut statik fiyatlandırma yöntemleri ve marketlerdeki manuel takip süreçleri insan hatasına açık, verimsiz ve yavaştır. 

Bu projenin amacı, Son Kullanma Tarihi (SKT) yaklaşan veya çabuk bozulabilen ürünleri **Agentic AI (Ajan Tabanlı Yapay Zeka)** yaklaşımıyla gerçek zamanlı analiz ederek otonom aksiyonlar almak, yerel işletmelerdeki gıda atık oranını **tahmini %30 azaltmak** ve çöpe gidecek ürünleri ekonomiye geri kazandırmaktır.

---

## 🧠 Hibrit Ajan Mimarisi (Core Logic)
Sistem, birbiriyle entegre çalışan iki temel otonom ajandan oluşmaktadır:

1. **Dinamik Fiyatlandırma Ajanı (Pricing Agent):** Ürünün kalan tazelik ömrünü, envanter durumunu ve günün saatini analiz eder. *Time-Decay Pricing* (Zaman Bozunumlu Fiyatlandırma) prensibini temel alarak, ürün bozulma riskine girdikçe fiyatı kademeli ve otonom olarak optimum seviyeye düşürür.
2. **Akıllı Eşleştirme Ajanı (Matching Agent):** İndirime giren ürünü rastgele herkese değil; kullanıcının **konum yakınlığı**, **geçmiş tercihleri** ve **fiyat duyarlılığı** kriterlerine göre puanlayarak (*Scoring*) sadece ilgili tüketicilere dijital dağıtım (bildirim) yapar. Bildirim kirliliğini (Spam) önler.

---

## 🛠️ Canlı Demo Hakkında Önemli Not (Visual Simulation)
> ⚠️ **ÖNEMLİ:** Bu depoda yer alan **`index.html`** dosyası, sistemin arka plandaki otonom karar mekanizmasını, kural setlerini ve reaktif mantığını jüriye/kullanıcılara görsel olarak sunabilmek amacıyla **Bootstrap ve JavaScript kullanılarak hazırlanmış bir ön yüz simülasyonudur (Demo)**. 
>
> Projenin gerçek mimari tasarımı ve teknoloji yığını şu şekildedir:
> * **Mobil Arayüz:** Flutter / React Native (Platform bağımsız erişim)
> * **Backend & Veritabanı:** Google Firebase (Gerçek zamanlı stok ve veri senkronizasyonu)
> * **Yapay Zeka & Mantık:** Python (Pandas, Streamlit ve Scikit-learn kütüphaneleri ile ajan kalibrasyonu)
> * **Entegrasyon:** REST API üzerinden güvenli haberleşme

---

## 🚀 Öne Çıkan Lojistik Özellikleri
* **Akıllı Gel-Al (Smart Pick-up):** Kullanıcının günlük rotası üzerindeki indirimli ürünleri alması teşvik edilerek kurye kullanımı minimize edilir ve karbon ayak izi düşürülür.
* **Geçici Rezervasyon:** Kullanıcı "Yola Çıktım" dediğinde, ürün onun adına 15 dakika rezerve edilerek marketteki stok çakışmaları önlenir.

---

## 📊 Akademik Referans
Bu çalışmadaki dinamik fiyatlandırma modelleri ve teorik altyapı hazırlanırken aşağıdaki akademik literatür temel alınmıştır:
* *Kayikci, Y., et al. (2022). "Data-driven optimal dynamic pricing strategy for reducing perishable food waste at retailers". Journal of Cleaner Production.*
