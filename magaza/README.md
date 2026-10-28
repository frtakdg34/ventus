# Ventus mağaza tasarımı

Bu sürüm ürün inceleme, kategori filtresi, beden seçimi ve tarayıcıda tutulan önizleme sepetini içerir. Gerçek satış, hesap oluşturma ve ödeme henüz bağlı değildir. Ürün adları ve tişört çizimleri taslaktır. Epoksi fotoğrafları kullanıcı tarafından referans olarak sağlanmıştır. Fiyat ve ürün özellikleri uydurulmamıştır.

## Gerçek satışa geçiş

- İşletme, satış ülkesi, para birimi, alan adı ve ödeme sağlayıcısı belirlenmeli.
- Ürün yönetimi, gerçek fiyat/beden/stok, kargo ve iade bilgileri girilmeli.
- Müşteri hesapları doğrulanmış bir kimlik hizmetiyle; yönetim hesabı çok faktörlü doğrulama ve sınırlı yetkilerle kurulmalı.
- Sipariş, fiyat ve stok sunucuda doğrulanmalı. Tarayıcıdaki sepet/fiyatlara güvenilmemeli.
- Kart alanları ödeme kuruluşunun barındırılan ödeme ekranında olmalı; kart numarası/CVV uygulamanın veritabanına, loglarına veya Git deposuna alınmamalı.
- Ödeme oturumu sunucuda oluşturulmalı. Ödeme sonucu sağlayıcıdan sorgulanmalı; bildirim imzası, sipariş numarası, tutar ve para birimi doğrulanmalı. Tekrar gelen bildirimler ikinci sipariş veya stok düşüşü üretmemeli.
- Başarılı/başarısız/yarıda kesilmiş ödeme, geciken ve tekrar gelen bildirim, eşzamanlı stok, iade ve hesap erişim sınırları test edilmeli.
- Gizli anahtarlar sunucu ortamında tutulmalı; yedekleme, hata izleme ve hız sınırları kurulmalı. Veri toplama başlamadan önce gerçek işletmeye uygun gizlilik ve satış metinleri tamamlanmalı.

Ödeme kuruluşu anlaşması ve canlı anahtarlar tamamlanmadan canlı ödeme açılamaz. API anahtarlarını veya kart bilgilerini sohbet mesajına yazmayın.
