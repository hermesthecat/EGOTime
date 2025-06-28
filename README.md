# EgoTime 🚌

Ankara'daki EGO otobüslerinin gerçek zamanlı bilgilerini sesli olarak sunan Python uygulaması.

## 📋 Özellikler

- **Gerçek Zamanlı Veri**: EGO'nun resmi API'sinden anlık otobüs bilgileri
- **Çok Dilli Destek**: Türkçe ve İngilizce sesli bildirimler
- **Sesli Geri Bildirim**: Google Text-to-Speech (gTTS) ile otomatik sesli okuma
- **Basit Kullanım**: Durak numarası girmeniz yeterli

## 🚀 Kurulum

### Gereksinimler

- Python 3.6 veya üzeri
- İnternet bağlantısı (API erişimi ve TTS için)

### Bağımlılıkları Yükleme

```bash
pip install -r requirements.txt
```

## 💻 Kullanım

### Türkçe Sesli Bildirim

```bash
python tr_EgoTTS.py
```

- Durak numaranızı girin
- Otobüs bilgileri Türkçe olarak sesli şekilde bildirilir

### İngilizce Sesli Bildirim

```bash
python en_EgoTTS.py
```

- Durak numaranızı girin
- Otobüs bilgileri İngilizce olarak sesli şekilde bildirilir
- Türkçe veriler otomatik olarak İngilizceye çevrilir

### Veri Toplama (Sessiz Mod)

```bash
python collectdata.py
```

- Ham JSON verisini konsola yazdırır
- Sesli bildirim yapmaz

## 📁 Dosya Yapısı

```bash
egotime/
├── tr_EgoTTS.py      # Türkçe sesli bildirim modülü
├── en_EgoTTS.py      # İngilizce sesli bildirim modülü
├── collectdata.py    # Veri toplama modülü
├── requirements.txt  # Python bağımlılıkları
├── README.md         # Proje dokümantasyonu
└── LICENSE          # Lisans dosyası
```

## 🔧 Teknik Detaylar

### Kullanılan Kütüphaneler

- **requests**: HTTP API istekleri için
- **gTTS**: Google Text-to-Speech servisi
- **playsound**: Ses dosyalarını oynatma
- **translate**: Türkçe-İngilizce çeviri

### API Endpoint

```bash
http://88.255.141.66/mblSrv14/service.asp?FNC=Otobusler&VER=3.1.0&LAN={dil}&DURAK={durak_no}
```

## 📝 Örnek Çıktı

Uygulama çalıştırıldığında:

1. Durak numarası istenir
2. API'den veriler çekilir
3. Her otobüs için hat kodu ve varış süresi sesli olarak bildirilir

## ⚠️ Notlar

- Bu uygulama EGO'nun resmi API'sini kullanır
- İnternet bağlantısı gereklidir
- Ses çıkışı için hoparlör/kulaklık gereklidir
- API'nin kullanılabilirliği EGO'ya bağlıdır

## 📄 Lisans

Bu proje açık kaynak kodludur. Özgürce kullanabilir ve değiştirebilirsiniz.

## 🤝 Katkıda Bulunma

Katkılarınızı memnuniyetle karşılıyoruz! Lütfen:

1. Fork yapın
2. Feature branch oluşturun
3. Değişikliklerinizi commit edin
4. Pull request gönderin

## 📞 İletişim

Sorularınız için issue açabilirsiniz.

---
*Ankara EGO otobüs bilgileri için geliştirilmiştir.*
