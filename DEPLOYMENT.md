# 🚀 Deployment Anleitung - Support Tool Vergleich

## Schnellstart für GitHub Pages

### Schritt 1: GitHub Repository erstellen

1. Gehen Sie zu [GitHub](https://github.com) und melden Sie sich an
2. Klicken Sie auf das **+** Symbol oben rechts → **New repository**
3. Repository Name: `support-tool-comparison` (oder beliebiger Name)
4. Beschreibung: "Interaktive Vergleichsmatrix für Support-Ticketing-Systeme"
5. Wählen Sie **Public** (für GitHub Pages erforderlich)
6. ✅ Aktivieren Sie **"Add a README file"**
7. Klicken Sie **Create repository**

### Schritt 2: Dateien hochladen

**Option A: Via GitHub Web Interface (Einfachste Methode)**

1. Öffnen Sie Ihr neues Repository
2. Klicken Sie auf **Add file** → **Upload files**
3. Laden Sie hoch:
   - `index.html` (die Hauptdatei)
   - `README.md` (die Dokumentation)
4. Commit message: "Initial commit: Support Tool Comparison"
5. Klicken Sie **Commit changes**

**Option B: Via Git Command Line**

```bash
# Repository klonen
git clone https://github.com/IHR-USERNAME/support-tool-comparison.git
cd support-tool-comparison

# Dateien hinzufügen
# (Kopieren Sie index.html und README.md in diesen Ordner)

# Committen und pushen
git add .
git commit -m "Initial commit: Support Tool Comparison"
git push origin main
```

### Schritt 3: GitHub Pages aktivieren

1. Gehen Sie in Ihrem Repository zu **Settings** (⚙️ oben rechts)
2. Scrollen Sie in der linken Sidebar zu **Pages**
3. Unter **Source**:
   - Branch: **main**
   - Folder: **/ (root)**
4. Klicken Sie **Save**
5. ⏱️ Warten Sie 1-2 Minuten

### Schritt 4: Website besuchen

Ihre Website ist nun live unter:
```
https://IHR-USERNAME.github.io/support-tool-comparison/
```

Die URL wird Ihnen auch in den GitHub Pages Settings angezeigt! 🎉

## 🎨 Anpassungen

### Farben ändern

Im `<style>` Bereich der `index.html`, suchen Sie nach:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Ersetzen Sie die Hex-Codes:
- `#667eea` - Primärfarbe (Lila)
- `#764ba2` - Sekundärfarbe (Dunkleres Lila)

### Bewertungen aktualisieren

Im `<script>` Bereich, finden Sie das `requirements` Array:

```javascript
const requirements = [
    { 
        category: "AI & Automation", 
        name: "AI Agents / Bots", 
        description: "...", 
        weight: 5, 
        zendesk: 9,      // ← Hier Scores ändern
        salesforce: 9, 
        freshdesk: 8,
        jira: 5,
        hubspot: 7,
        umbraco: 0
    },
    // ...
];
```

### Tool-Summaries anpassen

```javascript
const toolSummaries = {
    zendesk: { 
        name: "Zendesk", 
        avgScore: 8.4,                                    // ← Score ändern
        rating: "⭐⭐⭐⭐⭐", 
        price: "$55-115/Agent",                          // ← Preis ändern
        recommendation: "Beste Wahl für mittlere Teams"  // ← Text ändern
    },
    // ...
};
```

## 📱 Custom Domain (Optional)

### Mit GitHub Pages Custom Domain

1. Kaufen Sie eine Domain (z.B. bei Namecheap, GoDaddy)
2. In GitHub Pages Settings:
   - Geben Sie Ihre Domain ein: `www.ihredomain.com`
   - Klicken Sie **Save**
3. Bei Ihrem Domain-Provider:
   - Erstellen Sie einen CNAME Record:
     - Name: `www`
     - Value: `IHR-USERNAME.github.io`
   - Oder für Apex-Domain (ohne www):
     - 4x A Records zu GitHub IPs:
       - `185.199.108.153`
       - `185.199.109.153`
       - `185.199.110.153`
       - `185.199.111.153`
4. ⏱️ Warten Sie auf DNS-Propagierung (kann bis zu 24h dauern)

## 🔧 Troubleshooting

### Website zeigt 404 Error
- ✅ Stellen Sie sicher, dass die Datei `index.html` heißt (nicht `support-tool-comparison.html`)
- ✅ Prüfen Sie, dass GitHub Pages aktiviert ist (Settings → Pages)
- ✅ Warten Sie 2-3 Minuten nach Aktivierung

### Änderungen werden nicht angezeigt
- 🔄 Hard-Refresh im Browser: `Ctrl+Shift+R` (Windows) oder `Cmd+Shift+R` (Mac)
- 🗑️ Cache löschen
- ⏱️ GitHub Pages braucht manchmal 1-2 Minuten für Updates

### Design sieht kaputt aus
- ✅ Öffnen Sie Browser DevTools (F12) und prüfen Sie auf JavaScript-Fehler
- ✅ Stellen Sie sicher, dass die komplette HTML-Datei hochgeladen wurde
- ✅ Testen Sie lokal, indem Sie die HTML-Datei im Browser öffnen

## 📊 Analytics hinzufügen (Optional)

### Google Analytics

Fügen Sie vor `</head>` ein:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔐 SEO Optimierung

Fügen Sie im `<head>` Bereich hinzu:

```html
<!-- SEO Meta Tags -->
<meta name="description" content="Umfassender Vergleich von Support-Ticketing-Systemen: Zendesk, Salesforce, Freshdesk, Jira Service Management, HubSpot">
<meta name="keywords" content="Support Software, Ticketing System, Zendesk, Salesforce, Freshdesk, Tool Vergleich">
<meta name="author" content="Ihr Name">

<!-- Open Graph / Social Media -->
<meta property="og:type" content="website">
<meta property="og:title" content="Support Tool Vergleich 2025">
<meta property="og:description" content="Interaktive Bewertungsmatrix für 6 Support-Tools mit 56 Anforderungen">
<meta property="og:url" content="https://IHR-USERNAME.github.io/support-tool-comparison/">
```

## 📈 Performance

Die Website ist bereits optimiert:
- ✅ Keine externen Dependencies
- ✅ < 50 KB Dateigröße
- ✅ Lädt in < 1 Sekunde
- ✅ Mobile-responsive

## 🆘 Support

Bei Problemen:
1. Prüfen Sie die [GitHub Pages Documentation](https://docs.github.com/en/pages)
2. Öffnen Sie ein Issue im Repository
3. Kontaktieren Sie GitHub Support

---

**Viel Erfolg mit Ihrer Website! 🚀**
