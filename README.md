# GoGoDrama - Official Distribution & Release Tunnel

Kanal rilis resmi dan terowongan pembaruan otomatis (OTA In-App Auto-Update) untuk **GoGoDrama Universal Edition**.

### 📱 Unduh Rilis Terbaru
- **APK Rilis Universal (Mobile & Android TV)**: [GoGoDrama-release.apk](https://github.com/Celosz-fle7/GoGoDrama-Release/releases/latest/download/GoGoDrama-release.apk)
- **Manifest Pembaruan OTA**: [version.json](version.json)

---

### 🛡️ Arsitektur & Spesifikasi:
- **Dual-Engine Adaptive UI**:
  - **Mobile Mode**: Feed vertikal Reels/TikTok style ala GoDrama, swipe cepat tanpa lag buffering, episode bottom sheet.
  - **Android TV Mode**: 10-Foot Google TV Widescreen grid, D-Pad focus ring, Hero ambient backdrop, Right Side Drawer.
- **Keamanan Biner Berlapis**:
  - C++ NDK 25 (`libgogodrama.so`) dengan OLLVM Control Flow Flattening (CFF) & Bogus Control Flow.
  - Vektor inisialisasi kripto tersembunyi (Anti-FindCrypt).
  - Dynamic JNI Registration (`RegisterNatives` di `JNI_OnLoad`) tanpa simbol publik.
  - Kernel `TracerPid` memory poisoning trap.
  - OS-Level `FLAG_SECURE` dan anti-UI scraping (`noHideDescendants`).
- **Media Player Engine**:
  - AndroidX Media3 (ExoPlayer) Hardware Acceleration (Zero frame drop & zero leak).
