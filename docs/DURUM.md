# Durum

Son güncelleme: 2026-11-01

## Şu an
- Windows derleme görevi BİTTİ: tüm CLAUDE.md komutları hatasız geçti, `BananaStudio.exe` açılıyor,
  test anahtarı Credential Manager'a kaydoldu (`FAL_KEY`), mock üretim testi geçti.
- Ortam: .NET SDK 8.0.427 kuruldu (CLAUDE.md'deki 8.0.426'dan bir sürüm yeni, sorun yok).
- Açık hata: Provider API Keys penceresi sağdan kesik, Kaydet düğmesi görünmüyor
  (`docs/WINDOWS-HATALAR.md`).

## Sıradaki görev: Windows kullanım hataları
Bitti ölçütü:
- Provider API Keys penceresi tam görünür, Kaydet düğmesine fareyle basılır (DPI/ölçek dahil).
- Pano, dosya seçici, kısayollar, tam ekran kontrol edilir; her hata `docs/WINDOWS-HATALAR.md`'ye yazılır.

## Sonraki görevler
1. Marka profilleri (KARARLAR.md'deki açık soru netleşince).
2. Maliyet logu ve bütçe eşiği (açık soru: aylık $ ve uyarı mı durdurma mı).
