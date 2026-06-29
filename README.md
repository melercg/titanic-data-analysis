#  Titanik Veri Analizi: Hayatta Kalmanın Sosyal Boyutu

Jupyter notebook tabanlı, Python veri bilimi kütüphaneleri kullanılarak Titanic veri kümesi üzerinde gerçekleştirilen kapsamlı bir keşifsel veri analizi (EDA) ve görselleştirme projesidir.

## Genel Bakış

Bu projede, Titanic faciasında hayatta kalmayı belirleyen **sosyal faktörler** incelenmektedir. Veri yükleme, temizleme, eksik değer analizi, feature engineering ve veri içindeki kalıpları anlamak için çeşitli istatistiksel ve görsel incelemeler gerçekleştirilmiştir.

## Araştırma Sorusu

> **Cinsiyet, yaş ve sosyal sınıf hayatta kalmayı nasıl etkiledi?**

## Veri Kümesi

Bu proje, klasik Titanic veri setini kullanmaktadır. İki CSV dosyasından oluşmaktadır:

- **train.csv** — Hayatta kalma sonuçlarını içeren eğitim veri seti
- **test.csv** — Tahminler için test veri seti

Veri seti `Data/` klasörü altında bulunmaktadır. Aynı zamanda [Kaggle - Titanic Competition](https://www.kaggle.com/c/titanic) sayfasından da indirilebilir.

## Kullanılan Teknolojiler

- **Python 3.x** — Programlama dili
- **Jupyter Notebook** — Etkileşimli hesaplama ortamı
- **Pandas** — Veri işleme
- **NumPy** — Sayısal işlemler
- **Matplotlib** — Grafik çizim kütüphanesi
- **Seaborn** — İstatistiksel görselleştirme
## Kurulum ve Ayarlar

### 1. Sanal Ortamı Oluştur/Etkinleştir

Henüz sanal ortamı kurmadıysanız:

```bash
python -m venv venv
```

Sanal ortamı etkinleştirin:

**Windows (PowerShell):**
```bash
.\venv\Scripts\Activate.ps1
```

**Windows (Komut İstemi):**
```bash
.\venv\Scripts\activate.bat
```

**Mac/Linux:**
```bash
source venv/bin/activate
```

### 2. Bağımlılıkları Yükleyin

```bash
pip install pandas numpy matplotlib seaborn jupyter notebook
```

### 3. Notebook'u Başlatın

```bash
jupyter notebook
```

Ardından `titanic_analysis.ipynb` dosyasını açın.

## Defter İçeriği

Analiz defteri aşağıdaki bölümleri içermektedir:

### 1. Veri Hazırlığı
- **Kütüphaneler** (`import`) — Gerekli kütüphanelerin yüklenmesi
- **Veri Yükleme** (`pd.read_csv`) — Eğitim veri setinin içe aktarımı
- **İlk Bakış** (`head`) — Verinin ilk satırlarının incelenmesi
- **Veri Tipleri ve Yapısı** (`info`) — Sütun tipleri ve eksik değer özeti
- **İstatistiksel Özet** (`describe`) — Sayısal sütunların istatistikleri

### 2. Veri Temizleme
- **Eksik Veri Analizi** (`isnull`) — Eksik değerlerin yüzde olarak hesaplanması
- **Eksik Değer Tamamlama** (`fillna`) — Sayısal için `mean`, kategorik için `mode` yöntemi

### 3. Feature Engineering
- **Title Çıkarımı** — `Name` sütunundan unvan bilgisinin elde edilmesi
- **Title Çeşitliliği ve Gruplandırma** (`replace`) — 17 farklı unvanın 5 kategoriye indirgenmesi
- **Yaş Bazlı Gruplandırma** (`apply`) — Çocuk, Yaşlı, Yetişkin Kadın, Yetişkin Erkek kategorileri

### 4. Analiz ve Görselleştirme
- **Kategori Bazlı Hayatta Kalma** (`groupby + agg`) — Her kategorinin kurtulma oranı
- **Sosyal Sınıf Analizi** (`groupby`) — Pclass'a göre hayatta kalma
- **Sınıf × Kategori Çapraz Analiz** (`heatmap`) — İki boyutlu görselleştirme

### 5. Sonuç ve Çıkarımlar

## Başlıca Analiz Alanları

- **Veri Kalitesi** — Eksik değer kalıpları ve veri eksiksizliği
- **Yolcu Demografisi** — Yaş, cinsiyet ve sınıf analizi
- **Hayatta Kalma Kalıpları** — Hayatta kalmayı etkileyen sosyal faktörler
- **Çapraz Analizler** — Sınıf ve kategori birleşiminin etkisi
- **Görselleştirmeler** — Bar chart, heatmap ve karşılaştırmalı grafikler

## Temel Bulgular

| Profil | Kurtulma Oranı |
|---|---|
| 1. Sınıf Yetişkin Kadın | %97.6 |
| 2. Sınıf Yetişkin Erkek | %7.5 |

**Ana Çıkarım:** "Kadınlar ve çocuklar önce" ilkesi gözlemlenmiştir, ancak bu öncelik sosyal sınıfa göre belirgin biçimde farklılaşmıştır.



## Dosya Yapısı
