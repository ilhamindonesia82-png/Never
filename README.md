# Kalkulator (Android)

Kalkulator sederhana: tema gelap, bahasa Indonesia, tanpa dependensi tambahan.
Fitur: + − × ÷, persen (200+10% = 220), ± , hapus satu karakter, pratinjau hasil langsung,
perhitungan desimal akurat (0,1 + 0,2 = 0,3), pesan error bila dibagi 0.
Minimal Android 8.0 (API 26).

## Cara dapat APK

### Opsi A: lewat GitHub (tanpa PC, bisa dari HP)
1. Buat repository baru di GitHub, unggah seluruh isi folder ini (termasuk folder `.github`).
2. Buka tab **Actions** -> workflow **Build APK** (jalan otomatis setelah upload; atau klik **Run workflow**).
3. Setelah hijau, buka run-nya, unduh artifact **Kalkulator-APK** (zip berisi `app-debug.apk`).
4. Ekstrak, lalu instal di HP (izinkan "Instal dari sumber tidak dikenal").

### Opsi B: Android Studio
1. Buka folder ini di Android Studio (Ladybug atau lebih baru), tunggu sync.
2. Menu **Build -> Build APK(s)**. Hasil: `app/build/outputs/apk/debug/app-debug.apk`.

### Opsi C: terminal (butuh JDK 17 dan Android SDK)
```
./gradlew assembleDebug
```
APK ada di `app/build/outputs/apk/debug/app-debug.apk`.

## Struktur
- `app/src/main/java/id/kalkulator/app/Calc.java` : penghitung ekspresi (BigDecimal)
- `app/src/main/java/id/kalkulator/app/MainActivity.java` : tampilan dan logika tombol
- `app/src/main/res/` : ikon, tema, warna
