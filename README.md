---

## 📊 MangoHud: Performance-Overlay für Spiele einrichten

MangoHud ist ein konfigurierbares Overlay für Linux, das FPS, Temperaturen, CPU/GPU-Auslastung und mehr direkt im Spiel anzeigt.

### 1. Installation
Installiere MangoHud und das grafische Konfigurationstool GOverlay via DNF:
```bash
sudo dnf install mangohud -y
```

### 2. Startoptionen in Steam 
Um das Overlay und die Systemoptimierung (GameMode) für ein Spiel zu aktivieren, nutze folgenden Startbefehl:
```bash
mangohud gamemoderun %command%
```

### 3. Konfigurationsdatei erstellen
Erstelle das Verzeichnis und eine leere Konfigurationsdatei im Benutzerverzeichnis:
```bash
mkdir -p ~/.config/MangoHud
touch ~/.config/MangoHud/MangoHud.conf
```

### 4. Konfiguration anpassen
Öffne die Datei, um deine gewünschten Parameter oder Tastaturkürzel (Shortcuts) einzutragen:
```bash
nano ~/.config/MangoHud/MangoHud.conf
```

**Praktisches Beispiel für ein Tastaturkürzel (In die Datei einfügen):**
Mit dieser Zeile lässt sich das Overlay im Spiel jederzeit ein- und ausschalten (Linke Alt-Taste + R):
```ini
toggle_hud=Alt_L+R
```

*Tipp: Eine vollständige Vorlage mit allen verfügbaren Optionen findest du auf deinem System unter `/usr/share/doc/mangohud/MangoHud.conf.example`.*

### 5. Funktion testen
Überprüfe mit einem einfachen X11-Testprogramm, ob das Overlay korrekt geladen wird:
```bash
mangohud glxgears
```
