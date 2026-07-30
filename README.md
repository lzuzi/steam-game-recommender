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
