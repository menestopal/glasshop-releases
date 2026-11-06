# glasshop

Photoshop için Liquid Glass paneli. Seçili şekil, metin ya da piksel katmanına iOS'taki "Liquid Glass" görünümünü verir:
kenarda kırılma ve renk ayrışması, bulanıklık, renk tonu, kenar parlaması, iç ışıma ve gölge. Hazır ön ayarlarla gelir,
tüm ayarlar düzenlenebilir ve canlı güncellenir. Bu depoda kaynak kod yok, yalnız kurulum paketleri var.

## İndir

**[glasshop-1.1.0.ccx](https://github.com/menestopal/glasshop-releases/releases/download/v1.1.0/glasshop-1.1.0.ccx)** (sürüm 1.1.0)

Her zaman en son sürüme giden bağlantı: https://github.com/menestopal/glasshop-releases/releases/latest

Önceki sürümler: [Sürümler](https://github.com/menestopal/glasshop-releases/releases). Sürüm sayfasında yalnız `.ccx`
dosyasını indirin; "Source code" arşivlerini GitHub kendiliğinden ekler, kurulum için gerekmez.

Gereksinimler: Photoshop 24.2 (2023) ya da üstü (Photoshop 2026'da denendi), Mac ya da Windows, Creative Cloud masaüstü
uygulaması kurulu ve oturum açık. Belge RGB, 8 bit/kanal olmalı. UXP Developer Tool ya da geliştirici modu gerekmez.

## Kurulum

1. Photoshop açıksa kapatın.
2. İndirdiğiniz `glasshop-1.1.0.ccx` dosyasını çift tıklayın. Creative Cloud masaüstü uygulaması eklentiyi kurar.
   "Adobe Marketplace dışından" ya da "doğrulanmamış geliştirici" uyarısı çıkarsa **Yükle**'ye basın. Bu beklenen bir
   durum: paket Adobe Marketplace'ten değil, doğrudan geliyor.
3. Photoshop'u açın. Panel **Eklentiler (Plugins) › glasshop** menüsündedir.

Çift tıklama bir şey yapmazsa: Creative Cloud uygulamasını açın, **Stok ve Pazar Yeri › Eklentiler › Eklentileri Yönet**
sayfasına gidin ve `.ccx` dosyasını oraya sürükleyin.

Kurulum yalnız Creative Cloud'un eklenti klasörüne yazar, başka hiçbir yere dokunmaz. macOS'ta bu klasör:

```
~/Library/Application Support/Adobe/UXP/Plugins/External/com.glassshop.liquidglass_<sürüm>/
```

## İlk cam

1. Arka planın üzerinde duran bir **şekil, metin, piksel ya da smart object** katmanı seçin. Yuvarlak köşeli bir dikdörtgen
   iyi bir başlangıçtır.
2. **Ön ayarlar** galerisinden bir görünüm seçin. Ön ayarlar belge boyutuna göre kendiliğinden ölçeklenir.
3. İsterseniz **Temel** bölümündeki dört ayarı (Kırılma, Bulanıklık, Köşe, Renk tonu) ya da **Lens / Gövde / Işık / Gölge**
   sekmelerindeki diğerlerini değiştirin. Bir ayarın adına çift tıklayınca değer ön ayardakine döner.
4. **Uygula**'ya basın. Katman, `Liquid Glass · <ad>` adlı bir gruba dönüşür; orijinal katman grubun içinde gizli olarak durur.
5. Cam grubu seçiliyken **Canlı** açıksa her ayar değişikliği anında uygulanır. Camın altındaki içeriği değiştirir ya da camı
   taşırsanız **Güncelle**'ye basın: arka plan yeniden alınır.
6. **Kaldır**, efekti siler ve orijinal katmanı geri getirir. **+ Kaydet** ile kendi ön ayarlarınızı saklayabilirsiniz.

Her işlem Geçmiş panelinde tek bir adımdır, ⌘Z ile geri alınır.

## Güncelleme

Yeni bir sürüm çıkınca panelin başlığında mavi **Yeni sürüm** rozeti belirir (1.1.0 ve sonrasında); tıklayınca bu indirme
sayfası açılır. Panel hiçbir şey indirmez ya da kurmaz, yalnız haber verir: GitHub'a "en son sürüm ne?" diye sorar, o kadar.
Yeni sürümün `.ccx` dosyasını indirin, Photoshop'u kapatıp dosyaya çift tıklayın; Creative Cloud eskisinin üzerine kurar.
Kaydettiğiniz ön ayarlar ve belgelerinizdeki cam grupları olduğu gibi kalır.

## Kaldırma

Creative Cloud uygulaması › **Stok ve Pazar Yeri › Eklentiler › Eklentileri Yönet** › glasshop › **Kaldır**.
Belgelerinizdeki `Liquid Glass · …` grupları sıradan Photoshop katmanlarıdır, eklenti olmadan da açılır.

## Sorun olursa

- **Panel menüde yok:** Photoshop'u tamamen kapatıp açın. Creative Cloud'da Eklentileri Yönet sayfasında glasshop
  listeleniyor mu bakın; yoksa `.ccx` dosyasını yeniden çift tıklayın.
- **Uygula düğmesi sönük:** tek bir katman seçili olmalı; grup seçiliyse yalnız `Liquid Glass · …` grupları kabul edilir.
  Belge RGB ve 8 bit/kanal olmalı.
- **Metin katmanında köşe yuvarlama yok:** bilerek böyle, ince harf çizgilerini silerdi.
- **Cam yanlış arka planı gösteriyor:** arka plan bir anlık görüntüdür; **Güncelle**'ye basın.
- `Liquid Glass · ` ve `GS Source · ` ad önekleri panelin grubu tanıması için gerekli, bunları yeniden adlandırmayın.

Ön ayar görsellerindeki fotoğraf: "Sunset in Burano", Fabio Mangione (Unsplash), CC0.
