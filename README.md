# Rust Cheat Sheet

Türkçe açıklamalar ve İngilizce kod örnekleriyle, A4 yatay baskıya uygun Rust çalışma notları. HTML dosyaları CSS ve çizimleri kendi içinde barındırır; kurulum gerektirmez.

**[Tüm notları tarayıcıda aç](https://saadettinberber.github.io/rust-cheat-sheet/)** · [Ownership](https://saadettinberber.github.io/rust-cheat-sheet/rust-ownership-a4.html) · [References & Borrowing](https://saadettinberber.github.io/rust-cheat-sheet/rust-borrowing-a4.html)

## Dosyalar

| Dosya | Kapsam | Sayfa |
| --- | --- | --- |
| [rust-a4.html](rust-a4.html) | Temel konular, ownership ve borrowing birlikte | 15 |
| [rust-ownership-a4.html](rust-ownership-a4.html) | Stack, heap, Copy, Box, move, drop ve String | 3 |
| [rust-borrowing-a4.html](rust-borrowing-a4.html) | Referanslar, dereference, izin değişimleri, reborrow, lifetime ve alıştırmalar | 10 |

Temel notlar, [Brown sürümü The Rust Book](https://rust-book.cs.brown.edu/) kitabının 1–3. bölümlerini; ownership notları, [4.1 içinde “Collections Use Boxes” başlığı](https://rust-book.cs.brown.edu/ch04-01-what-is-ownership.html#collections-use-boxes) dahil önceki konuları kapsar. Borrowing notları ise [4.2 içinde “Permissions Are Returned At The End of a Reference’s Lifetime” başlığının](https://rust-book.cs.brown.edu/ch04-02-references-and-borrowing.html#permissions-are-returned-at-the-end-of-a-references-lifetime) sonuna kadar ilerler. Sonraki başlıklar ve açık lifetime parametreleri (`'a`) bu setin kapsamında değildir.

Şemalar kavramsaldır; fiziksel bellek yerleşimi garantisi vermez. R/W/O tabloları kitabın derleme zamanı erişim modelini kullanır. “Derlenmez” olarak işaretlenen örnekler, ilgili derleyici hatasını göstermek için özellikle hatalıdır.

## References & Borrowing çalışma sırası

1. **Sayfa 1–3:** Sahiplik aktarılmadan kullanım, pointer katmanları ve `Vec::push` ile geçersiz referans riski.
2. **[Sayfa 4–6](https://saadettinberber.github.io/rust-cheat-sheet/rust-borrowing-a4.html#borrowing-4):** Her satırdan sonra R/W/O izinleri; shared ve mutable borrow; reborrow sırasında `RW → R → RW` değişimi.
3. **[Sayfa 7–8](https://saadettinberber.github.io/rust-cheat-sheet/rust-borrowing-a4.html#borrowing-7):** Referansın kapsamı, borrow’un son kullanımı ve verinin drop edilmesi; `if` dallarında farklı bitiş noktaları.
4. **[Sayfa 9–10](https://saadettinberber.github.io/rust-cheat-sheet/rust-borrowing-a4.html#borrowing-9):** Altı özgün soru ve ayrı sayfada gerekçeli cevapları.

Borrowing setindeki 12 geçerli kod örneği derlenip çıktıları kontrol edildi; 6 hatalı örneğin beklenen derleyici hata kodlarını verdiği doğrulandı. A4 baskıda sayfa sayıları ve taşmalar da kontrol edildi.

## Kullanım

1. [Canlı sayfayı](https://saadettinberber.github.io/rust-cheat-sheet/) açın; dosya indirmeniz gerekmez.
2. İsterseniz **Yazdır / PDF kaydet** düğmesini kullanın.

Çevrimdışı kullanım için repoyu indirip veya klonlayıp istediğiniz HTML dosyasını tarayıcıda açabilirsiniz.

Baskı için A4, yatay yön ve %100 ölçek seçin. Tarayıcının üstbilgi ve altbilgilerini kapatın; renkli kutular için arka plan grafikleri seçeneğini açın. Sayfa ölçüleri 297 × 210 mm olarak sabittir. Dar ekranlarda yatay kaydırma kullanılabilir.

GitHub Pages, `main` dalının kök dizininden yayımlanır. Bu dala gönderilen güncellemeler otomatik olarak siteye yansır.

## Kaynaklar

İçerik, Brown sürümü The Rust Book ve [resmî Rust dokümantasyonuna](https://doc.rust-lang.org/) dayanır. İncelenen tasarımlar ve ilgili kaynak bağlantıları HTML dosyalarının sonundaki kaynaklar bölümünde bulunur.
