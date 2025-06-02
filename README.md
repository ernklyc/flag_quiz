# Flag Quiz (Bayrak Bilgi Yarışması)

Flag Quiz/Flutter -> https://play.google.com/store/apps/details?id=com.flag.quiz.yelbegen.software

Flag Quiz, kullanıcıların dünya bayrakları hakkındaki bilgilerini test eden, Flutter ile geliştirilmiş etkileşimli ve sürükleyici bir mobil uygulamadır. Oyun, eğlenceli ve eğitici olacak şekilde tasarlanmış olup, çoklu oyun modları ve İngilizce ile Türkçe yerelleştirme seçenekleri sunar.

## Özellikler

* **Çoklu Oyun Modları:** Kullanıcılar farklı soru sayılarından birini seçebilir:
    * 40 Soru
    * 80 Soru
    * 160 Soru
* **Bayrak Tanıma:** Temel oynanış, gösterilen bayrağa karşılık gelen ülkeyi tanımlamayı içerir.
* **Etkileşimli Kullanıcı Arayüzü (UI):**
    * Mevcut soru numarasını ve toplam soru sayısını gösterir.
    * Doğru cevap sayısını (skor) gösterir.
    * Doğru ve yanlış cevaplar için "flashbang" efektleri ve seslerle anında görsel geri bildirim sağlar.
* **Yerelleştirme (Localization):** İki dili destekler:
    * İngilizce (en-US)
    * Türkçe (tr-TR)
    * Kullanıcılar uygulama içinden dili değiştirebilir.
* **Para Kazanma (Monetization):** Google Mobil Reklamlarını (Google Mobile Ads) entegre eder:
    * Çeşitli ekranlarda gösterilen banner reklamlar.
    * Oyun modu seçiminden veya iletişim ekranından geri gitme gibi belirli noktalarda gösterilen geçiş reklamları (interstitial ads).
* **Kullanıcı Arayüzü Detayları:**
    * Gradyan butonlar ve metinler için gölgelendirici (shader) efektleriyle özel temalı kullanıcı arayüzü.
    * "Oyna", "İletişim" ve "Dili Değiştir" seçeneklerini içeren bir ana menü.
    * Geliştiricinin Google Play Store sayfasına, web sitesine bağlantılar ve e-posta gönderme seçeneği içeren özel bir iletişim ekranı.
* **Ses Efektleri:** Doğru ve yanlış cevaplar için sesler içerir.
* **Çapraz Platform (Cross-Platform):** Flutter ile geliştirilmiş olup, proje yapısına bağlı olarak birden fazla platformda (Android, iOS ve potansiyel olarak diğerleri) dağıtıma olanak tanır.

## Teknoloji Yığını ve Bağımlılıklar

* **Framework:** Flutter
* **Önemli Paketler (Dependencies):**
    * `easy_localization`: Uluslararasılaştırma ve yerelleştirme için.
    * `flutter_svg`: SVG formatındaki bayrak resimlerini render etmek için.
    * `assets_audio_player`: Ses efektlerini çalmak için.
    * `font_awesome_flutter`: İkonlar için.
    * `url_launcher`: URL'leri açmak için (örn. iletişim bağlantıları).

## Proje Yapısı

Proje standart bir Flutter proje yapısını takip eder:

* `lib/`: Uygulamanın temel Dart kodunu içerir.
    * `main.dart`: Uygulamanın giriş noktasıdır.
    * `pages/`: Uygulamanın farklı ekranlarını/sayfalarını içerir (örn. `home_page.dart`, `game_mode_select.dart`, `game_screen.dart`, `contact_screen.dart`).
    * `widgets/`: Uygulama genelinde kullanılan özel yeniden kullanılabilir widget'ları içerir (örn. butonlar, logo, gölgelendirici maskeleri).
    * `ads/`: Reklam entegrasyonunu yönetir (banner ve geçiş reklamları).
    * `utils/`: Yardımcı dosyalar, sabitler, bayrak resim yolları ve metin kaynaklarını içerir.
    * `thema.dart`: Uygulamanın temasını, renklerini ve buton stillerini tanımlar.
    * `localization_checker.dart`: Dil değiştirme mantığını yönetir.
* `assets/`:
    * `translations/`: Yerelleştirme için JSON dosyalarını içerir (örn. `en-US.json`, `tr-TR.json`).
    * `images/`: Muhtemelen bayrak resimlerini (SVG) ve uygulama logosu gibi diğer resim varlıklarını depolar.
    * `sounds/`: Ses efektleri için ses dosyalarını içerir.
* `android/`, `ios/`, `linux/`, `macos/`, `web/`, `windows/`: Platforma özgü yapılandırma ve kodları içerir.

## Android'e Özgü Yapılandırma

* **İnternet İzni:** Uygulama, reklamlar ve potansiyel olarak diğer ağ istekleri için internet izni gerektirir. Bu, `AndroidManifest.xml` dosyasında beyan edilmiştir.
* **Google AdMob Uygulama Kimliği:** AdMob Uygulama Kimliği `android/app/src/main/AndroidManifest.xml` dosyasında yapılandırılmıştır.

## Yerelleştirme Detayları

Uygulama, çevirileri yönetmek için `easy_localization` paketini kullanır. Çeviri dosyaları `assets/translations/` dizininde bulunur.
* İngilizce: `en-US.json`
* Türkçe: `tr-TR.json`

## İletişim

Uygulama içindeki "İletişim" bölümünden ulaşabilirsiniz; bu bölüm Google Play Store'u, geliştiricinin web sitesini ziyaret etme veya `yelbegensoftware@gmail.com` adresine e-posta gönderme seçeneklerini içerir.

---
