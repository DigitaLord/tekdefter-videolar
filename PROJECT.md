# tekdefter-videolar

## Amaç
TekDefter "Nasıl kullanılır" videolarının (9 video × 4 biçim) tarayıcıdan izlenebilir
herkese açık yayın sayfası. Üretim burada yapılmaz; dosyalar asıl üretim hattından
kopyalanır.

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
1. `~/.hermes/scripts/video-galeri-kopyala.sh` — render'ları `v/` altına kopyalar, kapak üretir.
2. `~/.hermes/scripts/video-galeri-dogrula.sh` — 36 dosyanın yayın kontrolü (206 + video/mp4).
3. `git add -A && git commit && git push` → Pages birkaç dakikada yenilenir.

## Sınırlar
- Video kaynağı burada düzenlenmez; değişiklik üretim hattında yapılır, sonra kopyalanır.
- Depo herkese açık: müşteri verisi, secret veya yayınlanmamış müşteri görüntüsü eklenmez.
- YouTube kanalı ayrı iş: Google oturumu gerektirir, kullanıcı açar.
