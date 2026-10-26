# tekdefter-videolar

<!-- KUNYE:BASLA -->
> **Ne:** TekDefter tanıtım videolarının izlendiği herkese açık yayın sayfası — nasıl kullanılır (9 × 4 biçim), revize 2 sunum alternatifleri (5 × yatay/dikey), UGC + tanıtım (4).
> **Üstü:** `mtbr-codex-workspace/inventory/projects.yaml` (katalog id: `tekdefter-videolar`) · `OBSD-KASA/10-projects/tekdefter/tekdefter.md` (durum) · `WORKSPACE.md` (dizin sözleşmesi)
> **Altı:** `index.html`, `v/` (mp4 + kapak), `yeni-videolar.json` (kart verisi)
> **Güncelleme:** 2026-10-26
<!-- KUNYE:BITIR -->

## Amaç
TekDefter tanıtım videolarının tarayıcıdan izlenebilir herkese açık yayın sayfası.
Üç bölüm: "Nasıl kullanılır" (9 video × 4 biçim), "Revize 2 · sunum alternatifleri"
(5 sunum × yatay/dikey = 10), "UGC + tanıtım" (4 video). Üretim burada yapılmaz;
dosyalar asıl üretim hattından kopyalanır.

## Sahiplik / grup
TekDefter — marka içeriği. Üretim hattı: `/Users/mtbr/TEKDEFTER-ROO/tdf-marketing/videos/nasil`.

## Durum
Aktif, yayında. GitHub Pages (`main` kökü), herkese açık depo.
Adres: https://digitalord.github.io/tekdefter-videolar/

## Esas çalışma dizini
`/Users/mtbr/tekdefter-videolar` — `index.html` (izleme sayfası), `v/` (mp4 + kapak jpg).

## Remote
`https://github.com/DigitaLord/tekdefter-videolar` (`origin`, `main`)

## Yayın akışı
1. Yeni video eklenecekse: `~/.hermes/scripts/video-galeri-yeni-bolum.py` — kaynak yayın
   dizininden `v/<id>.mp4` kopyalar, 3. saniyeden `-kapak.jpg` üretir, `yeni-videolar.json` yazar.
2. `~/.hermes/scripts/video-galeri-sayfa-yaz.py` — `index.html`'i JSON'dan üretir
   (bölüm + biçim sekmeleri, süre, indir, YouTube bağlantısı).
3. Boş kare kontrolü: `python3 ~/.hermes/skills/productivity/video-gallery-publish/scripts/bos-kare-tara.py v`
4. `git add -A && git commit && git push` → Pages birkaç dakikada yenilenir.

## Kaynak dizinler
- Nasıl kullanılır: `TEKDEFTER-ROO/tdf-marketing/videos/nasil` (yayın: `v/01..09-*`)
- Revize 2: `tdf-marketing/videos/(YENİ) alternatif-sunumlar-revize-2-2026-10-25/yayin`
- UGC + tanıtım: `tdf-marketing/videos/(YENİ) video-brief-alternatifleri-2026-10-25/yayin`

## Sınırlar
- Video kaynağı burada düzenlenmez; değişiklik üretim hattında yapılır, sonra kopyalanır.
- Depo herkese açık: müşteri verisi, secret veya yayınlanmamış müşteri görüntüsü eklenmez.
- YouTube kanalı ayrı iş: Google oturumu gerektirir, kullanıcı açar.
