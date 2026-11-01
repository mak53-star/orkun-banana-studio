# Geçmiş

## 2026-11-01 — Fork'un çıkış noktası (sohbet özeti)

**Kaynak:** Orkun Işıtmak'ın "Kendi yapay zeka araçlarımı sizlere ücretsiz açıyorum"
YouTube videosu. Üç açık kaynak araç tanıtıldı:
- **Banana Studio:** Higgsfield alternatifi AI görsel/video stüdyosu. Kendi API anahtarınla
  çalışıyor (fal, EvoLink, OpenRouter, Google).
- **Nashi:** Tangerine kopyası sürükle-bırak dosya dönüştürücü (Swift + native Windows).
- **Clipboardline:** Screenshot, metin ve link askısı; Raycast clipboard alternatifi.

**Videodan alınan yöntem:** Ücretli bir uygulamayı incele, eksiğini bul, AI kodlama
ajanıyla kendi versiyonunu yap. Orkun, Codex'in "goal" modunu kullanıyor (6–8 saat
otonom çalışma).

**Banana Studio'nun öne çıkan özellikleri:**
- YouTube linkinden kapak brief'i çıkarma
- Kişi kütüphanesi (kişi başı 3–5 referans foto)
- Beyin fırtınası ile toplu üretim (ör. 5 fikir × 4 görsel)
- Prompt iyileştirme, maskeli düzenleme, karşılaştırma görünümü

**Bilinen riskler:**
- Mac sürümü notarize değil; Windows derlemesi imzasız ve upstream'de fiziksel
  Windows'ta test edilmemiş.
- Toplu üretimde API maliyeti hızla büyür.

**Neden bu sıra (KARARLAR.md):**
- Mehmet Windows kullanıyor; Windows çalışmazsa diğer hiçbir şeyin anlamı yok.
- Marka profilleri, kendi girişimlerinin (Mevora, Skeylap, Vetorax) görsel üretimi için.
- Maliyet logu, genel çalışma kuralı 10 gereği.

**Nasıl çalışılıyor:**
- Analiz ve kararlar claude.ai sohbetinde veriliyor.
- Kod ve Windows testi Claude Code'da, Mehmet'in PC'sinde yapılıyor.
- Sohbet bulut ortamında çalıştığı için Windows'u derleyip test edemiyor.
