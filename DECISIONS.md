# Proje Kararları

## 28 Temmuz 2026

- Projenin çalışma adı **GameMatch AI** olarak kullanılacak.
- Kesin filtreler ayrı bir kenar çubuğundan alınmayacak; kullanıcının doğal dilde
  yazdığı istekten çıkarılacak.
- İlk sürümde fiyat, işletim sistemi, dil ve oyun modu ele alınacak.
- Anlamsal arama yalnızca kesin filtrelere uyan oyunlar üzerinde çalışacak.
- Kullanıcıya en fazla beş öneri ve her öneri için kısa bir neden gösterilecek.
- Büyük veri dosyaları ve üretilen indeksler Git'e eklenmeyecek.

## 29 Temmuz 2026

- Ham CSV dosyası doğrudan değiştirilmeyecek.
- Birleşmiş `DiscountDLC count` başlığı veri okunurken `Discount` ve `DLC count`
  olarak iki alana ayrılacak.
- Büyük veri dosyası ilk incelemede gerekli sütunlar seçilerek veya parçalar
  hâlinde okunacak.
- Playtest ve temel alanları eksik kayıtlar, temizleme kuralı kesinleşmeden
  doğrudan silinmeyecek.

## 30 Temmuz 2026

- Eksik veya negatif fiyat bulunmadığı için fiyat alanında düzeltme yapılmayacak.
- Bütün kayıtlar en az bir işletim sistemini desteklediği için işletim sistemi
  bilgisi nedeniyle kayıt çıkarılmayacak.
- Adında `Dedicated Server` veya `SDK` geçen oyun dışı uygulamalar temizleme
  aşamasında çıkarılacak.
- `Editor` ifadesi bazı gerçek oyunların adında da bulunduğu için tek başına
  çıkarma ölçütü olarak kullanılmayacak.
- Dil listesi boş olan kayıtların dili İngilizce kabul edilmeyecek ve
  `Bilinmiyor` olarak ele alınacak. Kullanıcı belirli bir dil istediğinde bu
  kayıtlar doğrulanmış eşleşme sayılmayacak.
- Oyun modu filtresinde `Single-player`, `Multi-player`, `Co-op` ve `PvP`
  kategorileri kullanılacak.
