# Proje Bağlamı

## Projenin amacı

GameMatch AI, kullanıcının doğal dilde anlattığı oyun isteğini anlayıp Steam
oyunları arasından uygun seçenekler önermeyi amaçlar.

## MVP kapsamı

İlk sürümde sistem:

1. Metinden fiyat, işletim sistemi, dil ve oyun modu filtrelerini çıkaracak.
2. Veri setinde bu filtrelere uyan oyunları bulacak.
3. Uygun oyunlar arasında anlamsal arama yapacak.
4. En fazla beş oyunu, neden uygun olduklarını açıklayarak gösterecek.

## Şimdilik kapsam dışında

- Kullanıcı hesabı ve favoriler
- Steam hesabıyla giriş
- Gelişmiş öneri geçmişi
- Mobil uygulama

Bu özellikler MVP tamamlandıktan sonra yeniden değerlendirilebilir.

## Veri kaynağı

Projede Kaggle üzerinde yayımlanan
[Steam Games Dataset](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset)
kullanılmaktadır. Ham CSV ve JSON dosyaları yalnızca yerel `data/raw/`
klasöründe tutulur ve GitHub'a gönderilmez.

## İlk veri bulguları

- Toplam 125.855 kayıt bulunmaktadır.
- CSV başlığındaki iki alan birleştiği için veri okuma sırasında düzeltilmektedir.
- 8.139 kayıt Playtest olarak belirlenmiştir.
- Oyun adı, açıklama, kategori ve tür alanları dolu olan 116.281 normal kayıt
  ön aday olarak belirlenmiştir.
- Desteklenen dil alanı 8.391 kayıtta boş liste şeklindedir.
- AppID alanındaki 125.855 değerin tamamı benzersizdir.
- Fiyat alanında eksik veya negatif değer bulunmamaktadır.
- Bütün kayıtlar en az bir işletim sistemini desteklemektedir.
- Temel oyun türlerinden hiçbirini içermeyen 1.364 kayıt güçlü oyun dışı aday
  olarak belirlenmiştir.
- Adında `Dedicated Server` geçen 14 ve `SDK` geçen 3 kayıt bulunmaktadır.
- Ön kullanılabilir oyunlar arasında 110.810 tek oyunculu, 20.707 çok oyunculu,
  11.284 Co-op ve 12.953 PvP kaydı bulunmaktadır.
- Playtest olmayan 1.435 kayıtta en az bir temel alan eksiktir; bu kayıtlar
  temizlenmiş öneri havuzuna alınmayacaktır.
- Temel oyun türlerinden hiçbirini içermeyen 1.364 kayıt güçlü oyun dışı aday
  olarak belirlenmiş ve temizleme kuralına dahil edilmiştir.
- Demo, Alpha veya Beta ifadeleri 326 kaydın adında geçmektedir; örneklerde bu
  ifadelerin gerçek oyun adlarında da kullanıldığı görüldüğü için tek başına
  çıkarma ölçütü olarak kullanılmayacaktır.
- Temizleme kuralları uygulandıktan sonra 115.705 kayıt temiz öneri havuzunda
  bırakılmıştır.
- Temiz veri `data/processed/temiz_games.csv` konumuna kaydedilmiştir.

Temizleme aşaması tamamlanmış, sonraki aşama kesin filtrelerin doğal dilden
çıkarılması olarak belirlenmiştir.
