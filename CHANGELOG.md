# Changelog

<!-- KUNYE:BASLA -->
> **Ne:** TekDefter kullanım videosu yayın sayfasının tarihli değişiklik kronolojisi.
> **Üstü:** `tekdefter-videolar/PROJECT.md`
> **Altı:** — (uç dosya)
> **Güncelleme:** 2026-10-22
<!-- KUNYE:BITIR -->

Bu dosya herkese açık yayın sayfasının (`index.html` + `v/`) teknik değişikliklerini izler.
Video üretimi burada yapılmaz; render'lar `TEKDEFTER-ROO/tdf-marketing/videos/nasil` altından kopyalanır.

## 2026-10-21 - Yayın sayfası ve galeri ilk yayını

### Değişenler

- `index.html`: TekDefter "Nasıl kullanılır" videolarının 4 biçimde (16x9, 9x16,
  9x16 sessiz, reels) izlendiği tek sayfalık galeri.
- `v/`: 9 video × 4 biçim mp4 ve her video için kapak jpg (toplam 45 dosya, ~212 MB).
- `.nojekyll`: GitHub Pages'in Jekyll işlemesini kapatır.
- `.gitignore`: yerel `KUNYE.txt` yayın dışında tutulur.

### Neden

- Videoların tarayıcıdan, uygulama kurmadan ve biçim seçerek izlenebilmesi için
  herkese açık, statik bir yayın yüzeyi gerekiyordu.

### Build/deploy

- GitHub Pages (`main` kökü) — https://digitalord.github.io/tekdefter-videolar/
- Yayın doğrulaması: `~/.hermes/scripts/video-galeri-dogrula.sh` 36 mp4 için
  HTTP 206 ve `video/mp4` yanıtını kontrol eder.
- Üretim hattı: `~/.hermes/scripts/video-galeri-kopyala.sh` (kopyalama + kapak).

## 2026-10-21 - Proje künyesi ve dokümantasyon

### Değişenler

- `PROJECT.md`: amaç, sahiplik, durum, esas çalışma dizini, remote, yayın akışı ve
  sınırlar; künye bloğu katalog id'si `tekdefter-videolar` ile bağlandı.
- `KUNYE.txt`: dizin künyesi (ne, neden, nereye bağlı, tarih, silme şartı).

### Neden

- `/Users/mtbr/WORKSPACE.md` dizin sözleşmesi: kökte duran (`sabit_kok`) her proje
  kökü `PROJECT.md` ve künye taşır; katalog (`projects.yaml`) tek kaynaktır.

### Build/deploy

- Dokümantasyon değişikliği; yayın içeriği değişmedi.
