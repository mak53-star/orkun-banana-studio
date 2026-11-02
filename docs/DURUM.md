# Durum

Son güncelleme: 2026-11-02

## Son yapılan
- Windows derleme görevi BİTTİ: CLAUDE.md komutları geçti, `BananaStudio.exe` açılıyor,
  `FAL_KEY` Credential Manager'a kaydoldu, mock üretim testi geçti.
- Windows kullanım hataları görevi BİTTİ: Provider API Keys penceresi DPI'ya göre
  ölçekleniyor ve otomatik boyutlanıyor (`desktop/windows/Program.cs`, `ShowKeys`).
  Elle doğrulandı: Save'e fareyle basma, `Ctrl+,`, `F11`/`Esc`, metin ve görsel pano.
  `npm test`: 334 geçti, 0 hata, 4 atlandı.
- Dal: `windows-kullanim-hatalari` (fork'a push edildi, PR açılmadı).
- Ortam: .NET SDK 8.0.427 kurulu (CLAUDE.md 8.0.426 diyor, sorun yok). Başlat menüsüne
  "Banana Studio" kısayolu eklendi (proje dışı, kullanıcı klasörü).
- Not: paketlemeden önce `BananaStudio.exe` kapalı olmalı, yoksa `EPERM`.
- Hata kayıtları: `docs/WINDOWS-HATALAR.md`.

## Sıradaki 3 iş
1. Saved References paneli ilk açılışta kesik görünüyor, "Edit" deyince düzeliyor
   (web arayüzü, `src/`). Bitti ölçütü: panel ilk açılışta tam görünür.
   Ayrı oturum: bu web arayüzü işi, Windows kabuğundan farklı.
2. Marka profilleri (KARARLAR.md'deki açık soru netleşince).
3. Maliyet logu ve bütçe eşiği.

## Test edilemeyenler
- Görsel indirme ("Farklı kaydet") ve ikinci monitör/DPI: galeri boş, ikinci ekran yok.
  Veri ve donanım olunca tekrar bakılacak.

## Bekleyen kararlar
- Marka profilleri: KARARLAR.md'deki açık soru.
- Maliyet logu: aylık $ bütçe ve uyarı mı durdurma mı.
- `windows-kullanim-hatalari` dalı `main`'e alınsın mı (PR/merge)?
