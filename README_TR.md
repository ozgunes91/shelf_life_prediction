# 🥫 Gıda Raf Ömrü Tahmini Projesi

Bu proje, gıda ürünlerinin **saklama sıcaklığı**, **nem oranı**, **ürün tipi**, **ambalaj türü** ve **koruyucu madde** içerip içermediği gibi özelliklere göre kaç gün taze kalacağını tahmin etmeyi amaçlar. Amaç, bu değişkenlere dayalı olarak bir makine öğrenmesi modeli geliştirerek ürünün raf ömrünü tahmin etmektir.

---

## 📌 Proje Özeti

Veri kümesinde aşağıdaki sütunlar yer alır:

- **storage_temperature**: Ürünün saklandığı sıcaklık (°C)
- **humidity**: Saklama ortamının nem oranı (%)
- **product_type**: Gıda ürününün tipi (örnek: süt, et, sebze)
- **package_type**: Ambalaj türü (örnek: vakumlu, plastik kutu)
- **preservatives**: Üründe koruyucu madde olup olmadığı (evet/hayır)
- **shelf_life_days**: Hedef değişken — ürünün kaç gün boyunca taze kaldığı

---

## 📁 Veri Seti

Veri kümesi hem sayısal hem de kategorik veriler içerir. Bu veri seti, notebook içinde rastgele veriler oluşturularak otomatik şekilde üretilir. Dolayısıyla dışarıdan manuel bir veri yüklemeye gerek yoktur.

Veri kümesi proje dizinine otomatik olarak `shelf_life_dataset.csv` adıyla kaydedilir. 

---

## 🧰 Kullanılan Teknolojiler

- **Python**  
- **Pandas** – Veri işleme ve analiz  
- **Scikit-learn** – Makine öğrenmesi algoritmaları ve veri ön işleme  
- **Matplotlib / Seaborn** – Görselleştirme  
- **RandomForestRegressor** – Regresyon modellemesi için kullanılan algoritma

---

## ⚙️ Adım Adım Uygulama

### 1. Veri Ön İşleme
- Kategorik değişkenler `OneHotEncoding` yöntemiyle sayısal forma dönüştürülür.  
- Sayısal değişkenler doğrudan modele verilir.

### 2. Modelin Performansı
Modelin tahmin ettiği değerler ile gerçek raf ömrü değerleri karşılaştırılmıştır.

**MAE (Ortalama Mutlak Hata)**: `0.90`  
Bu değer, modelin tahminlerinde ortalama 0.90 günlük bir hata olduğunu göstermektedir.

📈 Tahmin – Gerçek karşılaştırma grafiği:  
![Actual vs Predicted Shelf Life](actual_vs_predicted_shelf_life.png)

---

## ▶️ Nasıl Çalıştırılır?

### 1. Notebook'u Aç
Proje klasöründe yer alan `Food-Shelf-Life-Prediction.ipynb` dosyasını Jupyter Notebook ortamında aç.  
Tüm hücreleri sırasıyla çalıştırarak veri üretimi, model eğitimi ve sonuçları görebilirsin.

### 2. Gerekli Kütüphaneleri Kur

Terminal ya da komut satırına şu komutu yazman yeterlidir:

```bash
pip install -r requirements.txt
```

## 📂 Dosya Açıklamaları

| 📄 Dosya Adı                    | 📌 Açıklama                                                |
|-------------------------------|------------------------------------------------------------|
| `Food-Shelf-Life-Prediction.ipynb` | Tüm işlemleri içeren Jupyter Notebook dosyası              |
| `requirements.txt`                 | Gerekli Python kütüphaneleri listesi                       |
| `shelf_life_dataset.csv`          | Otomatik olarak oluşturulan veri kümesi                    |
| `README.md`                       | İngilizce proje açıklama dosyası                           |
| `README_TR.md`                    | Türkçe proje açıklama dosyası (bu dosya)                   |

---

## 📄 Lisans

Bu proje **MIT Lisansı** ile lisanslanmıştır.  
Daha fazla bilgi için [LICENSE](LICENSE) dosyasını inceleyebilirsiniz.