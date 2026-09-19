# İTÜlüYüm — Gizlilik ve destek sitesi

GitHub Pages'e doğrudan yüklenebilen, Türkçe ve mobil uyumlu statik web sitesi.
Ek kurulum, paket yükleme, veritabanı veya derleme gerekmez.

**Gizlilik sözleşmesi bu pakette bulunmuyor.** Ana sayfa şu an metnin
hazırlanmakta olduğunu gösterir. Metin tamamlandığında aynı sayfaya ekleneceği
için adres değişmez. Bu hazırlık sayfasını tamamlanmış gizlilik politikası
yerine mağaza başvurusunda kullanmayın.

## 1. Bilgisayarda görüntüleme

ZIP dosyasını açın. `index.html` dosyasına çift tıklayın.
Gizlilik ve destek sayfaları internet bağlantısı olmadan da görüntülenir.

## 2. GitHub'a yükleme

1. GitHub'da `ituluyum-web` adında **Public** bir repo oluşturun. Boş repo
   oluşturursanız kurulum ekranındaki **uploading an existing file** bağlantısını;
   README ile oluşturursanız **Add file → Upload files** seçeneğini kullanın.
2. ZIP'i açın ve içindeki `index.html`, `destek.html`, `styles.css` ve `README.md`
   dosyalarını repo'nun ana dizinine yükleyin. ZIP dosyasını veya bu dosyaları
   içeren üst klasörü yüklemeyin: `index.html` doğrudan ana dizinde olmalı.
   Paketteki `.nojekyll` dosyasını da yükleyebilirsiniz; bu sade dosya yapısı
   gizli dosya yüklenmese de çalışır.
3. **Commit changes** ile kaydedin.
4. Repo'da **Settings → Pages** bölümünü açın.
5. **Build and deployment → Source → Deploy from a branch** seçin.
6. **Branch: main**, **Folder: /(root)** seçip **Save** düğmesine basın.
   Varsayılan dalınızın adı farklıysa dosyaları yüklediğiniz dalı seçin.
7. Aynı ekrandaki **Visit site** bağlantısından sitenizi açın. İlk yayın ve
   güncellemelerin görünmesi 10 dakikaya kadar sürebilir.

Bu adımlar yeni, yalnızca bu siteye ayrılmış bir repo içindir. Uygulamanın
kaynak kodunu bu repo'ya eklemeniz gerekmez.

## 3. Sayfa adresleri

`KULLANICI` yerine repo'nun sahibi olan GitHub hesabını veya organizasyonu yazın.
Repo adını değiştirdiyseniz `ituluyum-web` bölümünü de değiştirin.
Kesin adres **Settings → Pages → Visit site** bölümünde gösterilir.

| Kullanım | Adres örneği |
| --- | --- |
| Gizlilik politikası | `https://KULLANICI.github.io/ituluyum-web/` |
| Destek | `https://KULLANICI.github.io/ituluyum-web/destek.html` |

Bunlar adres biçimi örnekleridir; site henüz GitHub'a yüklenmiş değildir.
Tarayıcı adresi ile repo adresi farklıdır: mağazaya `github.com/...` repo
bağlantısını değil, yayımlanan `github.io/...` sayfa adresini ekleyin.

## 4. Gizlilik metnini sonradan ekleme

GitHub'da `index.html` dosyasını açıp düzenleme düğmesini kullanın.

1. `GIZLILIK_METNI_BASLANGIC` ve `GIZLILIK_METNI_BITIS` yorumlarının arasındaki
   mevcut `<article> ... </article>` bölümünü kaldırın.
2. Yerine `<article class="document-card policy-content">` ile açılan ve
   `</article>` ile kapanan bir bölüm ekleyin. Hazırlanan metni bu bölüme yazın.
   Paragrafları `<p>...</p>`, bölüm başlıklarını `<h2>...</h2>`, alt başlıkları
   `<h3>...</h3>` ile sarın. Madde listeleri için `<ul><li>...</li></ul>` kullanın.
   Özel HTML karakterlerini gerektiğinde kaçırın: `&` → `&amp;`, `<` → `&lt;`.
   Stil dosyası bu öğelerin hepsini biçimlendirmeye hazırdır.
3. Metnin başında isterseniz `<p class="policy-updated">Son güncelleme:
   GERÇEK TARİH</p>` alanını kullanın. Tarihi metin kesinleştiğinde doldurun.
4. Sayfanın üstündeki `<meta name="robots" content="noindex, follow">` satırını
   kaldırın. Bu satır yalnızca hazırlık sayfasının arama sonuçlarına alınmaması
   için eklenmiştir; erişimi engellemez.
5. Değişikliği kaydedin. GitHub Pages aynı adresteki sayfayı günceller.

Metni JavaScript'e, JSON'a veya başka bir servise koymanız gerekmez.
HTML içinde bulunduğu için JavaScript kapalıyken de okunabilir.

## Dosyalar

| Dosya | Görevi |
| --- | --- |
| `index.html` | Gizlilik sayfası ve metnin ekleneceği işaretli alan |
| `destek.html` | Destek e-posta adresi ve e-posta gönderme bağlantısı |
| `styles.css` | Renkler, mobil görünüm, metin düzeni ve yazdırma biçimi |
| `.nojekyll` | GitHub Pages'in Jekyll işlemesini atlamasını sağlayan boş dosya |
| `README.md` | Bu kurulum rehberi |

Destek adresi: **ituluyum.destek@gmail.com**. Adresi değiştirmek için iki HTML
dosyasında bu adresin geçtiği tüm alanları değiştirin.

Site kodu analiz aracı, harici yazı tipi, çerez, tarayıcı depolaması veya form
gönderimi içermez. E-posta bağlantıları cihazın e-posta uygulamasını açar;
sitenin kendi e-posta gönderim sunucusu yoktur. Bu teknik açıklama, GitHub'ın
barındırma altyapısında veri işleme yapmadığı anlamına gelmez ve uygulamanın
gizlilik politikası yerine geçmez.

## GitHub'ın resmi yönergeleri

- [GitHub Pages sitesi oluşturma](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Yayımlama kaynağını seçme](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
