# tint website

GitHub Pages için bağımsız, statik uygulama tanıtım sitesi. Build, npm, API anahtarı veya backend gerektirmez. Uygulama projesinden ve App Store görsel stüdyosundan ayrıdır.

## Yerel önizleme

Bu klasörde `python3 -m http.server 8770` çalıştır ve `http://localhost:8770` adresini aç.

## GitHub Pages ile yayınlama

1. GitHub'da `tint-app` gibi yeni bir repository oluştur. Ücretsiz GitHub Pages kullanımı için public seç.
2. **Yalnızca bu klasörün içeriğini** repository köküne yükle. Swift uygulamasını, anahtarları veya üst klasörü ekleme.
3. Repository → Settings → Pages → Source: **Deploy from a branch**.
4. Branch: **main**, folder: **/ (root)** seç ve Save'e bas.
5. Dağıtım tamamlandığında Pages bölümünde verilen adresi aç. `tint-app` adı kullanılırsa adres `https://Muhammetkocaman.github.io/tint-app/` olur. Bu adres henüz oluşturulmuş/yayınlanmış değildir.

Sayfalar relative bağlantılar kullanır; repository adının değişmesi bağlantıları bozmaz. Destek adresi `/support.html`, gizlilik adresi `/privacy.html`, kullanım koşulları `/terms.html` dosyalarıdır; App Store Connect için bunları sitenin gerçek yayın URL'sinin sonuna ekle.

## İçerik

- `index.html`: tanıtım, gerçek tint çıktıları ve ücretsiz/Pro kapsamı.
- `support.html`: e-posta, restore, abonelik, export yardımı.
- `privacy.html`: yerel fotoğraf işleme ve RevenueCat/Apple satın alma verileri ayrı açıklanır.
- `terms.html`: Apple standart EULA bağlantısı ve planların açıklaması.
- `style.css`: ortak tasarım ve responsive düzen.
- `assets/`: tint görselleri, ikon ve OFL lisanslı Space Mono fontları.

App Store yayını doğrulanmadığından ana sayfa `Coming to the App Store` gösterir. Uygulama yayınlandıktan sonra `.availability` bölümünü `https://apps.apple.com/app/id6809603452` adresine giden gerçek indirme bağlantısıyla değiştir. Sabit fiyat yazılmadı; uygulama yerelleştirilmiş fiyatları gösterir.

Başka dil eklemek için örneğin `tr/` klasöründe çevrilmiş sayfalar oluştur, `lang="tr"` kullan ve o klasördeki varlık yollarını `../assets/` olarak ayarla. Mevcut İngilizce sayfaları koru.

## İçerik dayanakları

Referansın kısa tanıtım/destek yapısı: https://aduman.github.io/pressed-app/

Ürün bilgileri yerel `docs/product/PRODUCT.md`, `MonetizationStore.swift`, paywall/export ekranlarından alındı. Gizlilik metni yayımlanmadan önce panelde sonradan eklenmiş entegrasyonlar/analiz araçları varsa bunlarla eşleştirilmeli. Bu siteyi oluşturmak uygulama içindeki PrivacyPolicyURL veya App Store Connect alanlarını otomatik değiştirmez.

RevenueCat veri açıklaması: https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/apple-app-privacy

Görseller bu uygulamanın tanıtımına aittir; yeniden kullanım lisansı verilmez. Font lisansı `assets/OFL.txt` içindedir.
