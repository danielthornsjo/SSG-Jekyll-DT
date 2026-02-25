# SSG-Jekyll-ASJ

En enkel webbplats med Jekyll - en statisk sidgenerator

## Kom igång med Jekyll (statisk webbplats) – steg för steg

### 1) Förutsättningar
Du behöver:
- **Ruby** (inkl. RubyGems)
- **Bundler** (för att hantera Ruby-beroenden)
- En **terminal** (PowerShell/Terminal) och gärna **Git**

Kontrollera att Ruby finns:
```bash
ruby -v
gem -v
```

Installera Bundler:
```bash
gem install bundler
bundle -v
```

### 2) Skapa en ny Jekyll-sajt
Skapa en ny webbplats i en ny mapp:
```bash
jekyll new my-site
cd my-site
```

Om kommandot `jekyll` saknas, installera Jekyll:
```bash
gem install jekyll
```

### 3) Starta utvecklingsservern lokalt
Kör sajten lokalt:
```bash
bundle exec jekyll serve
```

Öppna sedan i webbläsaren:
- `http://localhost:4000`

Tips: om du vill att den ska uppdatera automatiskt vid ändringar:
```bash
bundle exec jekyll serve --livereload
```

### 4) Förstå projektstrukturen (kort)
Vanliga mappar/filer:
- **_posts/** – blogginlägg (filnamn enligt `YYYY-MM-DD-titel.md`)
- **_layouts/** – mallar (t.ex. `default.html`)
- **_includes/** – återanvändbara delar (header/footer)
- **_config.yml** – grundinställningar (titel, tema, m.m.)
- **index.md / index.html** – startsidan

### 5) Skapa en sida
Skapa t.ex. `about.md` i projektroten:
```markdown
---
layout: page
title: Om
permalink: /om/
---

Här är en enkel sida skapad med Jekyll.
```

### 6) Skapa ett inlägg (post)
Skapa en fil i `_posts/`, t.ex.:
`_posts/2026-02-25-forsta-inlagget.md`
```markdown
---
layout: post
title: "Första inlägget"
---

Det här är mitt första inlägg i Jekyll.
```

### 7) Bygg sajten för publicering
Skapa en statisk version (HTML/CSS/JS) i mappen `_site/`:
```bash
bundle exec jekyll build
```

Publicera innehållet i `_site/` (eller låt din plattform bygga den automatiskt).

### 8) Vanliga problem
- **Fel gem-versioner**: kör `bundle install` och använd `bundle exec ...`
- **Porten upptagen**: byt port:
    ```bash
    bundle exec jekyll serve --port 4001
    ```
- **Ändringar syns inte**: prova `--livereload` eller starta om servern

--- 

### Snabb checklista
1. Installera Ruby + Bundler  
2. `jekyll new <namn>`  
3. `bundle exec jekyll serve`  
4. Lägg till sidor/inlägg  
5. `bundle exec jekyll build` för publicering