# Derin Öğrenme ile Tıbbi Görüntü Sınıflandırması

## 📋 Genel Bakış

Göğüs röntgen görüntülerinden akciğer hastalıklarını teşhis etmek için Evrişimli Sinir Ağları (CNN) kullanarak tıbbi görüntü sınıflandırması için derin öğrenme projesi.

## 🎯 Amaç

Göğüs röntgen görüntülerini dört kategoriye sınıflandırmak:
- **COVID19**: COVID-19 enfeksiyonlu görüntüler
- **NORMAL**: Normal görüntüler
- **PNEUMONIA**: Zatürre enfeksiyonlu görüntüler
- **TURBERCULOSIS**: Tüberküloz enfeksiyonlu görüntüler

## 🏗️ Mimari

Proje özel bir CNN modeli kullanmaktadır:
- Batch Normalization ile 8 Evrişimli Katman
- 4 MaxPooling Katmanı
- 3 Tam Bağlı Katman
- Overfitting'i azaltmak için Dropout katmanları

## 📁 Proje Yapısı

```
Dev.Grup/
│
├── Ahmed_Ahmed_22040301122_Dev.Grup_1.ipynb
├── AHMED_ELSAYED_22040301142_Dev.Grup_1.ipynb
├── Ahmet__22040301174_Dev.Grup_1.ipynb
├── Dirar_Ahmed_22040301123_Dev.Grup_1.ipynb
│
└── test/
    ├── COVID19/
    ├── NORMAL/
    ├── PNEUMONIA/
    └── TURBERCULOSIS/
```

## 🚀 Gereksinimler

```bash
torch
torchvision
PIL
matplotlib
seaborn
numpy
scikit-learn
tqdm
```

Gereksinimleri yüklemek için:
```bash
pip install torch torchvision pillow matplotlib seaborn numpy scikit-learn tqdm
```

## 💻 Kullanım

1. **Veri Hazırlama**
   - Eğitim verilerini her sınıf için klasörlerle birlikte `train/` klasörüne yerleştirin
   - Doğrulama verilerini her sınıf için klasörlerle birlikte `val/` klasörüne yerleştirin
   - Test verilerini her sınıf için klasörlerle birlikte `test/` klasörüne yerleştirin

2. **Notebook Çalıştırma**
   - Jupyter Notebook dosyasını açın
   - Hücreleri sırayla çalıştırın

3. **Eğitim**
   - Model, veri dengesizliğini ele almak için Ağırlıklı Örnekleme (Weighted Sampling) destekler
   - En iyi model doğrulama doğruluğuna göre kaydedilir

4. **Değerlendirme**
   - Modeli test verileri üzerinde değerlendirin
   - Karışıklık Matrisi (Confusion Matrix) ve ROC Eğrisi gösterin
   - Accuracy, Precision, Recall, F1-Score, AUC-ROC hesaplayın

## 📊 Özellikler

- ✅ Veri Artırma (döndürme, çevirme, renk değişikliği, vb.)
- ✅ Dengesiz veri için Ağırlıklı Örnekleme
- ✅ Batch Normalization
- ✅ Overfitting'i azaltmak için Dropout
- ✅ Çoklu metriklerle kapsamlı değerlendirme
- ✅ Sonuç görselleştirme (Karışıklık Matrisi, ROC Eğrisi)
- ✅ Tek görüntü tahmini

## 📈 Metrikler

Model şu metriklerle değerlendirilir:
- Accuracy (Doğruluk)
- Precision (Kesinlik)
- Recall (Duyarlılık)
- F1-Score
- AUC-ROC
- Confusion Matrix (Karışıklık Matrisi)

## 🔧 Model Parametreleri

- **Görüntü Boyutu**: 224x224 piksel
- **Batch Size**: 32 (varsayılan)
- **Öğrenme Oranı**: Model eğitimi sırasında ayarlanır
- **Epoch Sayısı**: Eğitim sırasında belirlenir

## 📝 Veri Artırma Teknikleri

- Rastgele Yatay Çevirme
- Rastgele Dikey Çevirme
- Rastgele Döndürme (±15 derece)
- Rastgele Ölçeklendirme
- Renk Değişiklikleri
- Rastgele Silme (Random Erasing)

## 👥 Katkıda Bulunanlar

- Ahmed Ahmed (22040301122)
- Ahmed Elsayed (22040301142)
- Ahmet (22040301174)
- Dirar Ahmed (22040301123)

## 📝 Notlar

- Daha hızlı eğitim için GPU kullanımı önerilir
- Veriler sınıflara göre klasörlerde organize edilmelidir
- Desteklenen görüntü boyutu: 224x224 piksel
- Model, farklı sayıda sınıf için yapılandırılabilir



