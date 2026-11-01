# Durum

Son güncelleme: 2026-11-01

## Şu an
- Windows derleme görevi BİTTİ: tüm CLAUDE.md komutları hatasız geçti, `BananaStudio.exe` açılıyor,
  test anahtarı Credential Manager'a kaydoldu (`FAL_KEY`), mock üretim testi geçti.
- Ortam: .NET SDK 8.0.427 kuruldu (CLAUDE.md'deki 8.0.426'dan bir sürüm yeni, sorun yok).
- Provider API Keys penceresi düzeltildi (DPI/otomatik boyut), ekranda doğrulandı.
  Save'e fareyle basma ve kalan kontroller aşağıda. Ayrıntı: `docs/WINDOWS-HATALAR.md`.
- Kod değişikliği yalnızca `desktop/windows/Program.cs`. Commit edilmedi (testler çalıştırılmadı).

## Sıradaki görev: Windows kullanım hataları
Bitti ölçütü:
- [x] Provider API Keys penceresi tam görünür (Save'e fareyle basma ayrıca denenecek).
- Elle kontrol sonucu: F11/Esc, metin ve görsel pano ÇALIŞTI. Açık: Saved References paneli
  ilk açılışta kesik görünüyor; Save'e fareyle basma ve web odaklıyken Ctrl+, denenmedi;
  indirme ve ikinci monitör test edilemedi (galeri boş, ikinci ekran yok).
- [ ] Pano, dosya seçici, kısayollar, tam ekran kontrol edilir; her hata `docs/WINDOWS-HATALAR.md`'ye yazılır.

## Sonraki görevler
1. Marka profilleri (KARARLAR.md'deki açık soru netleşince).
2. Maliyet logu ve bütçe eşiği (açık soru: aylık $ ve uyarı mı durdurma mı).
