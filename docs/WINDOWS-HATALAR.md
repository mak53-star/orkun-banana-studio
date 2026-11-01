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
- Geçenler: `npm ci`, `npm test` (334 geçti, 4 atlandı), `typecheck`, `build`, `build:desktop`,
  `fetch-node-runtime`, `package-windows`, `test-local-generation` (mock, paralı istek yok).
