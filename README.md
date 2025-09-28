# 📊 PySpark ile Kredi Riski Tahmini

## 🚀 Proje Özeti
Bu proje, **PySpark MLlib** kullanılarak bir kredi riski tahmin pipeline’ının nasıl kurulacağını göstermektedir.  
Amaç, bankaların riskli ve risksiz kredi başvurularını veri işleme ve makine öğrenmesi teknikleriyle ayırt edebilmelerini simüle etmektir.

---

## 📂 Veri Seti
Proje, **German Credit Data** adlı veri setine dayanmaktadır:

- Age (Yaş)  
- Job (Meslek)  
- Housing (Konut durumu)  
- Saving accounts (Tasarruf hesapları)  
- Checking account (Vadesiz hesap)  
- Credit amount (Kredi miktarı)  
- Duration (Kredi süresi)  
- Purpose (Kredi amacı)  

> Not: Veri setinde doğrudan bir **Risk** etiketi bulunmadığından, sentetik bir etiket oluşturulmuştur (örneğin, kredi miktarı yüksekse riskli kabul edilmiştir).

---

## 🛠️ Kullanılan Teknolojiler
- Google Colab + PySpark  
- Spark MLlib (Logistic Regression, Random Forest)  
- Feature Engineering (örn. `credit_per_age`, `installment_rate`)  
- `StringIndexer` ile kategorik değişken kodlama  
- AUC metriği ile model değerlendirme  
- Model kaydetme (deployment simülasyonu)  

---

## 🔑 Adımlar
1. **ETL & Feature Engineering**  
   - `credit_per_age` ve `installment_rate` gibi yeni değişkenler oluşturuldu.  
2. **Encoding**  
   - Kategorik kolonlar `StringIndexer` ile sayısallaştırıldı.  
3. **VectorAssembler**  
   - Özellikler tek bir feature vektöründe birleştirildi.  
4. **Modelleme**  
   - Logistic Regression (AUC ≈ **0.9988**)  
   - Random Forest (AUC ≈ **0.9993**)  
5. **Değerlendirme**  
   - Modeller neredeyse kusursuz AUC skorları elde etti (demo amaçlı).  
6. **Deployment Simülasyonu**  
   - Eğitilen model `.save()` ile kaydedildi.  

---

## 📊 Sonuçlar
- **Logistic Regression AUC**: `0.9988`  
- **Random Forest AUC**: `0.9993`  

Her iki model de bu veri setinde riskli ve risksiz başvuruları neredeyse mükemmel bir doğrulukla ayırdı.  

---

## 🤝 Katkı
Projeyi fork’layarak geliştirebilirsiniz:
- Daha gerçekçi finansal veri setleriyle denemeler  
- Hiperparametre optimizasyonu  
- ROC eğrisi / Confusion Matrix görselleştirmeleri  

---

## 👨‍💻 Geliştirici
📌 Geliştirici: [İbrahim Yazıcı]  
