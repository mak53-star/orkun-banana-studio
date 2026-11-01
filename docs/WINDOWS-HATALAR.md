# Windows hataları

Biçim: adım · hata mesajı · düzeltme.

## 2026-11-01 — İlk derleme (hata yok, 2 not)

- **Ortam:** `dotnet` komutu yoktu. `winget install Microsoft.DotNet.SDK.8` ile 8.0.427 kuruldu
  (CLAUDE.md 8.0.426 diyor, fark sorun çıkarmadı). Kurulumdan sonra açık terminallerde
  `dotnet` PATH'te görünmez; yeni terminal aç.
- **`package-windows.mjs`:** İlk `dotnet` çalıştırması ASP.NET HTTPS geliştirme sertifikası
  yükledi (yan etki, zararsız). Güvenmek gerekmez.
- **Provider API Keys penceresi (AÇIK HATA, düzeltilmedi):** Pencere sağdan kesik ("Remove"
  yarım görünüyor), Kaydet düğmesi görünmüyor. Mouse ile bulunamadı; Tab ile ilerleyip
  Enter'a basınca kayıt çalıştı (`FAL_KEY`, Credential Manager'da doğrulandı).
  Büyük olasılıkla DPI/ölçek ya da sabit pencere boyutu sorunu. Düzeltme: sonraki görev
  "Windows kullanım hataları" (DPI) içinde, `desktop/windows/` WebView2 diyalog boyutu.
- **Provider API Keys penceresi — DÜZELTİLDİ (2026-11-01):** Neden: sabit 670×480 piksel
  boyut, DPI ölçeklemesi yok. Düzeltme (`desktop/windows/Program.cs`, `ShowKeys`): `AutoScaleMode.Dpi`,
  `AutoSize`/`GrowAndShrink`, ızgara dock'suz (`Dock.Top` pencereyi daralttı, işe yaramadı),
  alta boşluk, düğmeler en az 88×34. Ekran görüntüsüyle doğrulandı: metin, alanlar, Remove,
  Cancel ve Save tam görünüyor. Not: paketlemeden önce BananaStudio.exe kapalı olmalı
  (açıkken `package-windows.mjs` `EPERM` verir).
## 2026-11-01 — Elle kullanım kontrolü (Mehmet, ekranda)

- **Tam ekran:** `F11` ile girer, `Esc` ile çıkar. ÇALIŞTI.
- **Pano:** Türkçe metin yapıştırma ÇALIŞTI. Görsel yapıştırma ÇALIŞTI.
- **Dosya seçici (Saved References paneli):** Panel ilk açılışta biraz kesik görünüyor, "Edit"
  deyince tam hali açılıyor. AÇIK, küçük. Panel WinForms değil, web arayüzünün parçası
  (`src/`); büyük olasılıkla WebView2 ilk yerleşim/boyut sorunu. Henüz incelenmedi.
- **İndirme/kaydet:** Test edilemedi, galeri boş.
- **İkinci monitör/DPI:** Test edilemedi, ikinci ekran yok.
- **Denenmedi:** Save'e fareyle basma; web odaklıyken `Ctrl+,`.
- **Araç notu:** Başlat menüsüne "Banana Studio" kısayolu eklendi (kullanıcı klasörü,
  `Start Menu\Programs`), bilgisayar kontrolü aracı bu oturumda göremedi, yeni oturumda görür.
- Geçenler: `npm ci`, `npm test` (334 geçti, 4 atlandı), `typecheck`, `build`, `build:desktop`,
  `fetch-node-runtime`, `package-windows`, `test-local-generation` (mock, paralı istek yok).
