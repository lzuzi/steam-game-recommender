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
data/                 Yerel veri dosyaları (Git'e eklenmez)
notebooks/            Veri keşfi ve küçük deneyler
src/gamematch/        Uygulamanın Python kodları
tests/                Otomatik testler
PROJECT_CONTEXT.md    Projenin kapsamı ve hedefi
DECISIONS.md          Aldığımız önemli kararlar
TASKS.md              Adım adım çalışma listesi
```

## Veri seti

Kullanılması planlanan veri seti:
[Steam Games Dataset](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset)

İndirilen `games.csv` dosyası `data/raw/games.csv` konumuna yerleştirilmelidir.
Ham ve işlenmiş veri dosyaları repoya gönderilmez.

## Durum

İlk proje iskeleti oluşturuldu. Sıradaki adım veri setini Pandas ile okuyup
sütunları incelemek.
