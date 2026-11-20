# 📸 FotoLov

Android aplikace pro Daníka a Lukáška: zatoč kolem, vylosuj 4 úkoly, vyfoť je a aplikace z nich udělá koláž.

## Jak z projektu udělat APK

### Varianta A – Android Studio (nejjednodušší)
1. Nainstaluj [Android Studio](https://developer.android.com/studio).
2. Rozbal zip a ve Studiu dej **File → Open** → vyber složku `FotoLov`.
3. Počkej, až se projekt sám nastaví (stáhne Gradle a knihovny, chvíli to trvá).
4. Menu **Build → Build App Bundle(s) / APK(s) → Build APK(s)**.
5. APK najdeš v `app/build/outputs/apk/debug/app-debug.apk`.

### Varianta B – GitHub (bez instalace čehokoli)
1. Nahraj obsah složky do nového repozitáře na GitHubu.
2. Záložka **Actions** → workflow **Build APK** se spustí sám.
3. Po pár minutách si v detailu běhu stáhneš artefakt **FotoLov-apk**.

### Instalace na telefon
Pošli si APK do telefonu (e-mail, Drive, kabel), otevři ho a povol
„Instalovat z neznámých zdrojů“. Vyžaduje Android 10 nebo novější.

## Co kde je
- `app/src/main/assets/index.html` – celá hra (vzhled, kolo, úkoly, koláž).
  Úkoly pro jednotlivé obtížnosti jsou v ní nahoře v `TASKS`, vtipné hlášky v `FUN`.
- `app/src/main/java/cz/marb/fotolov/MainActivity.java` – Android obal:
  fotoaparát, výběr z galerie, uložení koláže do Galerie (složka *Pictures/FotoLov*), sdílení, vibrace.
