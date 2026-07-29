# GameMatch AI

GameMatch AI, kullanıcının doğal dilde yazdığı isteğe göre Steam oyunları
önermeyi amaçlayan bir RAG projesidir. Proje şu anda geliştirme aşamasındadır.

## Planlanan temel akış

1. Kullanıcının isteğinden fiyat, işletim sistemi, dil ve oyun modu bilgilerini çıkar.
2. Bu koşullara uymayan oyunları ele.
3. Kalan oyunlar arasında anlamsal arama yap.
4. En uygun en fazla beş oyunu kısa nedenleriyle öner.

## Proje yapısı

```text
data/                    Yerel veri dosyaları (Git'e eklenmez)
notebooks/               Veri inceleme çalışmaları
README.md                Projenin genel açıklaması
PROJECT_CONTEXT.md       Projenin kapsamı ve hedefi
DECISIONS.md             Projede alınan önemli kararlar
TASKS.md                 Adım adım çalışma listesi
CHANGELOG.md             Önemli proje değişiklikleri
requirements.txt         Temel Python bağımlılıkları
```

## Veri seti

Projede kullanılan veri seti:
[Steam Games Dataset](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset)

İndirilen `games.csv` dosyası `data/raw/games.csv` konumuna yerleştirilmelidir.
Ham ve işlenmiş veri dosyaları repoya gönderilmez.

## Kurulum

Proje Python 3.10 ile geliştirilmektedir. Temel bağımlılıklar aşağıdaki komutla
kurulabilir:

```bash
pip install -r requirements.txt
```

İlk veri inceleme notebook'u:
`notebooks/01_veri_inceleme.ipynb`

## İlk veri incelemesi

- Veri setinde 125.855 kayıt ve düzeltilmiş hâliyle 40 sütun bulunmaktadır.
- CSV başlığında `Discount` ve `DLC count` alanlarının birleştiği görülmüştür.
- Ham veri değiştirilmeden başlık okuma sırasında iki alana ayrılmıştır.
- 8.139 Playtest kaydı belirlenmiştir.
- Temel alanları dolu ve Playtest olmayan 116.281 ön aday kayıt bulunmuştur.
- 8.391 kayıtta desteklenen dil bilgisi boş liste olarak tutulmaktadır.
- AppID alanında tekrar eden kayıt bulunmamıştır.

## Durum

İlk veri kalitesi incelemesi tamamlandı. Sıradaki adım temizleme kurallarını
kesinleştirip tekrar kullanılabilir bir veri hazırlama işlemi oluşturmaktır.
