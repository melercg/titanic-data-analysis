# titanic-data-analysis
İlk veri bilimi projem: Titanic EDA
# 🚢 Titanic Veri Analizi: Hayatta Kalmanın Sosyal Boyutu

##  Proje Hakkında

Bu projede, Titanic faciasında hayatta kalmayı belirleyen **sosyal faktörler** analiz edilmektedir.

##  İçindekiler

### 1. Veri Hazırlığı
- Kütüphaneler (`import`)
- Veri Yükleme (`pd.read_csv`)
- İlk Bakış (`head`)
- Veri Tipleri ve Yapısı (`info`)
- İstatistiksel Özet (`describe`)

### 2. Veri Temizleme
- Eksik Veri Analizi (`isnull`)
- Eksik Değer Tamamlama (`fillna`)

### 3. Feature Engineering
- Title Çeşitliliği ve Gruplandırma (`replace`)
- Yaş Bazlı Gruplandırma (`apply`)

### 4. Analiz ve Görselleştirme
- Kategori Bazlı Hayatta Kalma (`groupby + agg`)
- Sosyal Sınıf Analizi (`groupby`)
- Sınıf × Kategori Çapraz Analiz (`heatmap`)

### 5. Sonuç ve Çıkarımlar

##  Araştırma Sorusu

> **Cinsiyet, yaş ve sosyal sınıf hayatta kalmayı nasıl etkiledi?**

##  Veri Seti

- **Kaynak:** [Kaggle - Titanic Dataset](https://www.kaggle.com/c/titanic)
- **Boyut:** 891 yolcu, 11 özellik
- **Hedef değişken:** `Survived` (0 = Öldü, 1 = Kurtuldu)

## 🛠️Kullanılan Teknolojiler

- **Python 3.x**
- **Pandas, NumPy** — Veri manipülasyonu
- **Matplotlib, Seaborn** — Görselleştirme
- **Jupyter Notebook** (Google Colab)

##  Dosya Yapısı
---

##  Projeyi Çalıştırma Rehberi

Bu projeyi farklı yöntemlerle çalıştırabilirsiniz. İhtiyacınıza göre **3 farklı yol** sunuyorum:

### Yöntem 1: Google Colab (En Kolay)

Hiçbir kurulum gerektirmez, tarayıcıdan çalıştırırsınız.

1. **Notebook'u Colab'da açın:**
   - [titanic_analysis.ipynb](titanic_analysis.ipynb) dosyasına tıklayın
   - Sağ üstte **"Open in Colab"** butonuna basın

2. **Veri setini yükleyin:**
   - Bu repository'deki `Data/` klasöründen `train.csv` ve `test.csv` indirin
   - Colab sol panelindeki klasör ikonundan **Upload** ile yükleyin
   - Veya Kaggle'dan ZIP olarak indirip yükleyin: [Kaggle Titanic](https://www.kaggle.com/c/titanic/data)

3. **Notebook'u çalıştırın:**
   - **Runtime → Run all** ile tüm hücreleri çalıştırın

###  Yöntem 2: VS Code + Virtual Environment

Lokal makinenizde profesyonel bir kurulum.

1. **Repository'yi klonlayın:**
```bash
   git clone https://github.com/melercg/titanic-data-analysis.git
   cd titanic-data-analysis
```

2. **Sanal ortam (venv) oluşturun:**

   VS Code'da terminal açın (`Ctrl + ~`):
```bash
   python -m venv venv
```

3. **Sanal ortamı aktifleştirin:**

   **Windows:**
```bash
   venv\Scripts\activate
```

   **Mac/Linux:**
```bash
   source venv/bin/activate
```

4. **Gerekli kütüphaneleri yükleyin:**
```bash
   pip install pandas numpy matplotlib seaborn jupyter ipykernel
```

5. **Jupyter Notebook'u başlatın:**
```bash
   jupyter notebook
```

   Veya VS Code'da `titanic_analysis.ipynb` dosyasına tıklayıp kernel olarak `venv`'i seçin.

6. **Çalıştırın:**
   - Hücreleri sırayla `Shift + Enter` ile çalıştırın

###  Yöntem 3: Kaggle Üzerinden

Kaggle hesabınız varsa direkt çalışabilirsiniz.

1. [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic) sayfasına gidin
2. **"New Notebook"** ile yeni notebook oluşturun
3. Bu repository'deki `titanic_analysis.ipynb` içeriğini kopyalayıp yapıştırın
4. Veri seti Kaggle'da **otomatik bağlı** gelir
5. Çalıştırın

---

##  Temel Bulgular

| Profil | Kurtulma Oranı |
|---|---|
| 1. Sınıf Yetişkin Kadın | %97.6 |
| 2. Sınıf Yetişkin Erkek | %7.5 |

**Ana Çıkarım:** "Kadınlar ve çocuklar önce" ilkesi gözlemlenmiştir, ancak bu öncelik sosyal sınıfa göre belirgin biçimde farklılaşmıştır.

---

## Yazar

**Melisa Erocagi**

İlk veri bilimi projesi — geri bildirimler için açığım. 
