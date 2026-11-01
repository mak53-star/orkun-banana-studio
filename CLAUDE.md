# Banana Studio (Mehmet fork)

DURUM: AKTİF
Upstream: orkunisitmak/banana-studio (MIT) · Fork: mak53-star/orkun-banana-studio

## Ne bu
Kendi API anahtarınla çalışan AI görsel/video stüdyosu. React/TS arayüz (`src/`),
yerel Node sunucu (`desktop/server/`), Mac kabuğu Swift (`desktop/macos/`),
Windows kabuğu .NET 8 + WebView2 (`desktop/windows/`).

## Önce oku
- `docs/KARARLAR.md` — sohbette verilen kararlar. Kararı buradan oku, kendin değiştirme.
- `docs/DURUM.md` — şu an neredeyiz, sıradaki iş.
- `AGENTS.md` — upstream'in güvenlik kuralları (geçerli).
- Uzun geçmiş: `docs/GECMIS.md`.

## Ortam
- Geliştirici makinesi Windows x64. Mac komutlarını (`swift`, `test:macos`) çalıştırma.
- Gerekli: Node 24.x, .NET SDK 8.0.426, Git, WebView2 Runtime.

## Windows derleme / test
```sh
npm ci --ignore-scripts
npm test
npm run typecheck
npm run build
npm run build:desktop
node scripts/fetch-node-runtime.mjs
node scripts/package-windows.mjs
node scripts/test-local-generation.mjs
```
Paket: `.build/staging-windows/Banana Studio/` → `BananaStudio.exe`.

## Çalışma kuralları
1. Bir oturum = bir görev. Bitince /clear, bağlam ~%60'ta /compact.
2. Her görevin "bitti" ölçütü yazılı olsun. Büyük değişiklik plan modunda başlar.
3. Model: varsayılan Sonnet. Opus sadece mimari karar veya çözülemeyen hata için.
4. Uygulama içinde merdiven: önce kural/script, sonra ucuz model, en son pahalı model.
   Hesap ve istatistik asla LLM'e bırakılmaz.
5. Her AI çağrısı model, token ve maliyetle loglanır; bütçe eşiği aşılırsa uyarı.
6. API anahtarı, .env, kullanıcı medyası, veritabanı asla commit edilmez.
   Testler geçmeden commit yok.
7. Paralı sağlayıcıya test isteği atma; mock sağlayıcı testlerini kullan.
8. Görev bitince `docs/DURUM.md` güncellenir.

## Upstream ile senkron
```sh
git remote add upstream https://github.com/orkunisitmak/banana-studio  # bir kez
git fetch upstream && git merge upstream/main
```
Kendi değişikliklerimizi ayrı dalda tut; upstream'e katkı gerekiyorsa ayrı PR.
