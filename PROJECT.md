# Culture Connects Network
## ROADMAP.md – MVP und langfristige Produktentwicklung

**Stand:** September 2026  
**Arbeitstitel:** Culture Connects  
**Dokumenttyp:** Technische und produktstrategische Roadmap

---

# 1. Ziel der Roadmap

Diese Roadmap übersetzt die bisherige Culture-Connects-Vision in eine schrittweise technische und produktbezogene Entwicklung.

Grundprinzip:

> **Die Vision bleibt groß. Die erste technische Version bleibt klein.**

Das MVP soll nicht versuchen, sämtliche langfristig vorgesehenen Funktionen umzusetzen.

Es soll zunächst eine zentrale Hypothese überprüfen:

> **Können zwei Menschen mit unterschiedlichen Perspektiven durch eine strukturierte digitale Begegnung und anschließende KI-Reflexion zu einem besseren gegenseitigen Verständnis gelangen – und möchten sie danach erneut teilnehmen?**

Alle weiteren Module werden auf diesem Kern aufgebaut.

---

# 2. Produktkern

Der zentrale Produkt-Loop lautet:

```text
Registrierung
     ↓
Profil
     ↓
Themen / Interessen
     ↓
Matching
     ↓
strukturierte Debatte
     ↓
Debattenabschluss
     ↓
KI-Analyse
     ↓
Reflexion
     ↓
Bewertung
     ↓
erneute Begegnung
```

Der langfristige Wachstumskreislauf:

```text
Gute Begegnung
     ↓
Positive Erfahrung
     ↓
Interessante Debatte
     ↓
Teilbarer Inhalt
     ↓
Neue Aufmerksamkeit
     ↓
Neue Nutzer
     ↓
Mehr mögliche Matches
     ↓
Bessere Matches
     ↓
Noch bessere Begegnungen
```

---

# 3. Entwicklungsprinzipien

## 3.1 Modularität

Jede größere Funktion soll möglichst als eigenständiges Modul bzw. Service betrachtet werden.

Neue Funktionen sollen den bestehenden Kern erweitern, nicht destabilisieren.

## 3.2 MVP First

Neue Features werden zunächst danach beurteilt:

- Ist das für den Kern-Loop notwendig?
- Hilft es beim Test der zentralen Hypothese?
- Kann die Funktion später modular ergänzt werden?

Wenn die Antwort auf alle drei Fragen gegen eine sofortige Implementierung spricht, wird das Feature zunächst in die spätere Roadmap verschoben.

## 3.3 Technologie als Werkzeug

KI, Blockchain und weitere Technologien sind Mittel zum Zweck.

Die Technologie soll bessere menschliche Begegnungen ermöglichen und nicht selbst zum eigentlichen Produktzweck werden.

## 3.4 Datenschutz by Design

Pseudonymität, kontrollierbare Profile, Einwilligung zur Veröffentlichung und möglichst geringe unnötige Datensammlung sollen bereits bei der Architektur berücksichtigt werden.

## 3.5 Messbarkeit

Jede MVP-Phase soll überprüfbare Ergebnisse liefern.

Nicht nur:

> Wie viele Nutzer haben wir?

sondern insbesondere:

- Beenden Nutzer die Debatten?
- Fühlen sie sich verstanden?
- Verstehen sie die Gegenposition besser?
- Ist die KI-Analyse hilfreich?
- Kommen sie wieder?
- Wollen sie erneut diskutieren?
- Empfehlen sie die Plattform freiwillig weiter?

---

# 4. Phase 0 – Architektur und technische Grundlage

**Ziel:** Technische Basis schaffen, ohne bereits unnötige Komplexität aufzubauen.

### Kernaufgaben

- Repository-Struktur definieren
- Entwicklungsumgebung einrichten
- Backend-Grundstruktur
- Datenbank
- Authentifizierung
- Benutzer-/Profilmodell
- API-Struktur
- Frontend-Grundstruktur
- Umgebungsvariablen / Konfiguration
- Logging
- grundlegende Fehlerbehandlung
- Basis-Sicherheitskonzept

### Architekturprinzip

```text
Frontend
   │
   ▼
API / Application Layer
   │
   ├── Identity / Users
   ├── Profiles
   ├── Topics
   ├── Matching
   ├── Debates
   ├── Reputation
   └── AI
        │
        ▼
     AI Adapter
        │
        └── Provider austauschbar
```

### Ergebnis

Ein lauffähiges Grundsystem, auf dem die MVP-Module aufgebaut werden können.

---

# 5. Phase 1 – Nutzer und Profile

**Ziel:** Nutzer können sich registrieren und ein grundlegendes Profil erstellen.

### MVP-Funktionen

- Registrierung
- Login
- Logout
- Pseudonym
- grundlegende Profilinformationen
- Interessen
- Themenkategorien
- Sprache
- bevorzugte Gesprächsdauer
- gewünschter Matching-Modus

### Matching-Einstellungen

Vorgesehene Optionen:

- ähnliche Perspektiven
- ausgewogene Begegnung
- unterschiedliche Perspektiven
- konträre Perspektiven
- maximal konträre Perspektiven

Zusätzlich:

- Altersgruppe / Generation
- Sprache
- Region
- Interessen
- Gesprächsdauer

### Ergebnis

Ein Nutzer kann ein Profil erstellen, anhand dessen ein Match erzeugt werden kann.

---

# 6. Phase 2 – Topic Engine

**Ziel:** Debattenthemen strukturiert verwalten.

### Funktionen

- Themenkategorien
- vordefinierte Themen
- Nutzer können Themen vorschlagen
- Themenstatus
- Themen-Metadaten
- Eignung für Debatten
- Themenfilter

### Kategorien

Unter anderem:

- Politik
- Gesellschaft
- Philosophie
- Religion
- Wissenschaft
- Technologie
- Wirtschaft
- Kultur
- Beziehungen
- Geschichte
- Umwelt
- persönliche Entwicklung
- Alltag / Lebensfragen

### KI-Unterstützung

Die KI kann später:

- Themen verständlicher formulieren
- Themen kategorisieren
- ähnliche Themen erkennen
- geeignete Themen für Nutzer vorschlagen

Wichtig:

Die KI soll bei Community-Themen zunächst formale Kriterien prüfen und keine ideologische „Richtigkeit“ bewerten.

---

# 7. Phase 3 – Matching Engine

**Ziel:** Zwei geeignete Gesprächspartner zusammenführen.

### MVP-Version

Das Matching berücksichtigt:

```text
Sprache
Interessen
Thema
Gesprächsdauer
gewünschter Perspektivunterschied
ggf. Altersgruppe
ggf. Region
```

Die Matching-Logik besteht aus zwei Schritten:

```text
1. Geeigneten Pool bestimmen
        ↓
2. Konkrete Begegnung auswählen
```

Damit entsteht:

> **Kontrolle + Überraschung**

Der Nutzer kann den Rahmen bestimmen, muss aber nicht selbst den Gesprächspartner auswählen.

### Spätere Erweiterungen

- Reputation
- bisherige Gesprächserfahrung
- Kommunikationsstil
- langfristige Interessenentwicklung
- bewusstes Herausfordern von Filterblasen
- bessere Match-Prognosen

---

# 8. Phase 4 – Debate Engine

**Ziel:** Der eigentliche Kern des MVP.

### MVP

- Debattenraum
- Textchat
- Thema
- Rollen / Positionen
- Start der Debatte
- definierter Ablauf
- Abschluss
- Speicherung der Debattenstruktur

### Möglicher Ablauf

```text
Match
 ↓
Thema
 ↓
Einführung
 ↓
Position A
 ↓
Position B
 ↓
gegenseitige Argumentation
 ↓
Rückfragen
 ↓
Abschluss
 ↓
Reflexion
```

Der konkrete Ablauf kann während der Tests verändert werden.

### Bewusst zunächst nicht erforderlich

- Video
- komplexe Live-Medien
- öffentliche Chats
- großer Community-Feed

---

# 9. Phase 5 – KI Debate Analysis

**Ziel:** Nach Abschluss der Debatte eine strukturierte Reflexion erzeugen.

Die KI analysiert erst nach Abschluss der Debatte.

### Mögliche Kriterien

- Argumentationsqualität
- logische Qualität
- Fairness
- Zuhören
- Verständnis
- Sachlichkeit
- Umgang mit Quellen
- Gemeinsamkeiten
- Unterschiede
- unterschiedliche Begriffsdefinitionen
- Lernmöglichkeiten

### Wichtig

Die KI soll nicht primär feststellen:

> Wer hat gewonnen?

Sondern:

> **Was ist in dieser Begegnung tatsächlich passiert?**

### Ergebnis

Beispielsweise:

```text
Gemeinsamkeiten
Unterschiede
Missverständnisse
neue Perspektiven
offene Fragen
mögliche Lernimpulse
```

---

# 10. Phase 6 – User Reflection

**Ziel:** Die KI-Analyse wird mit der persönlichen Wahrnehmung des Nutzers verbunden.

Nach der Debatte kann der Nutzer beantworten:

- Fühlte ich mich verstanden?
- Verstehe ich die andere Person besser?
- Hat sich meine Sicht verändert?
- Gab es ein Argument, das mich zum Nachdenken gebracht hat?
- Möchte ich erneut mit dieser Person sprechen?
- Möchte ich eine andere Perspektive kennenlernen?

### Besonders wichtig

Eine mögliche Meinungsänderung soll nicht automatisch von der KI behauptet werden.

Der Nutzer kann selbst markieren:

> **„Das hat meine Sicht verändert.“**

und optional angeben:

- neue Fakten
- überzeugendes Argument
- persönliche Erfahrung
- Veränderung eigener Werte
- andere Kategorie
- Freitext

---

# 11. Phase 7 – Reputation und Feedback

**Ziel:** Konstruktives Verhalten erfassen.

### MVP

Nach einer Debatte können Nutzer einander bewerten.

Mögliche Kriterien:

- Respekt
- Fairness
- Zuhören
- konstruktives Verhalten
- Umgang mit anderen Meinungen

### Kein Debattensieger-System

Reputation soll nicht primär auf gewonnenen Debatten basieren.

Stattdessen:

```text
Respekt
+ Fairness
+ Zuhören
+ konstruktives Verhalten
+ Qualität
```

### Später

Reputation kann für:

- Matching
- Moderation
- Freischaltungen
- Community-Events

verwendet werden.

---

# 12. Phase 8 – Erste persönliche Statistik

**Ziel:** Einen minimalen persönlichen Entwicklungsüberblick schaffen.

### MVP

Beispielsweise:

- Anzahl Debatten
- Themenbereiche
- Anzahl abgeschlossener Debatten
- wiederholte Begegnungen
- eigene Reflexionsangaben

### Später

Die langfristige Entwicklungsanalyse kann untersuchen:

- Interessen
- Argumentationsmuster
- Annahmen
- Positionen
- Perspektiven
- Kommunikationsqualität
- erkannte Meinungsänderungen

Dabei muss klar zwischen Beobachtung und Interpretation unterschieden werden.

---

# 13. Phase 9 – Wiederholte Begegnungen

**Ziel:** Aus einzelnen Begegnungen echte Beziehungen bzw. Lernverläufe entstehen lassen.

MVP-Funktionen:

- erneut mit derselben Person sprechen
- keine erneute Begegnung
- blockieren

Später:

- neue Themen für dasselbe Paar
- bewusst kontrastierende Themen
- Entwicklung der Gesprächsqualität
- gemeinsame Schnittmengen
- gemeinsamer Entwicklungsverlauf mit Zustimmung beider Personen

---

# 14. Phase 10 – MVP-Pilot

**Ziel:** Mit echten Menschen testen.

### Startgröße

Zunächst:

**0–100 Nutzer**

Der Fokus liegt nicht auf Wachstum.

Der Fokus liegt auf Lernen.

### Testgruppen

Mögliche erste Communities:

- persönliche Kontakte
- Hochschulgruppen
- Studenteninitiativen
- Vereine
- philosophische Gruppen
- internationale Gruppen
- thematische Online-Communities

### Zentrale Messgrößen

```text
Match → Debatte gestartet
Debatte gestartet → Debatte beendet
Debatte beendet → KI-Analyse angesehen
Debatte beendet → Nutzer fühlt sich verstanden
Erste Debatte → zweite Debatte
Erste Debatte → Empfehlung
```

Die wichtigste Kennzahl:

> **Wollen Menschen freiwillig eine zweite Begegnung?**

---

# 15. Phase 11 – Voice

**Nach erfolgreicher Validierung des Text-MVP**

### Funktionen

- Voice-Debatte
- automatische Transkription
- Sprechererkennung
- Zeitstruktur
- KI-Analyse des Gesprächs

### Ziel

Die Kommunikation soll natürlicher werden, ohne den strukturierten Charakter der Debatte zu verlieren.

---

# 16. Phase 12 – Mehrsprachigkeit

### Funktionen

- mehrsprachige Benutzeroberfläche
- automatische Übersetzung
- Übersetzung von Textdebatten
- später Voice-Übersetzung

### Ziel

Sprache soll möglichst wenig zur Barriere für echte Begegnungen werden.

---

# 17. Phase 13 – Challenge Mode

**Ziel:** Nutzer können sich bewusst außerhalb ihrer bisherigen Perspektiven bewegen.

Konfigurierbare Faktoren:

- Thema
- Gegensätzlichkeit
- Altersgruppe
- Region
- Sprache
- Schwierigkeitsgrad

### Schutzmechanismen

Besondere Grenzen für:

- Minderjährige
- sensible persönliche Themen
- potenziell belastende Situationen

Bestimmte Themen können vom Challenge-Modus ausgeschlossen werden.

---

# 18. Phase 14 – Community

### Funktionen

- Community-Events
- Debate of the Week
- Debate of the Month
- Themenvorschläge
- Abstimmungen
- kuratierte Debatten
- interessante Fragen
- Erkenntnisse

Kein klassischer endloser Social Feed.

Ziel:

> **Entdecken statt Scrollen.**

---

# 19. Phase 15 – Organisches Empfehlungsmodell

Nach einer positiven Erfahrung kann der Nutzer eingeladen werden, selbst jemanden zu Culture Connects zu bringen.

Beispiel:

> „Diese Debatte war interessant. Lade jemanden ein, mit dem du das ausprobieren möchtest.“

Keine aggressiven Referral-Systeme.

Keine künstlichen Einladungsziele.

Die Empfehlung soll aus einer guten Erfahrung entstehen.

---

# 20. Phase 16 – Creator- und Multiplikatorenmodell

Später können Personen aus passenden Communities eingebunden werden:

- Philosophie
- Wissenschaft
- Gesellschaft
- Bildung
- Psychologie
- Technologie
- internationale Themen
- Debatten / Argumentation

Mögliche Formate:

> „Ich diskutiere 30 Minuten mit einem Fremden, der völlig anderer Meinung ist.“

Der Creator erlebt das Produkt selbst.

---

# 21. Phase 17 – Projekte und Kooperation

Langfristige Erweiterung:

- gemeinsame Projekte
- Veranstaltungen
- Forschung
- lokale Initiativen
- gesellschaftliche Aktivitäten

Matching für Projekte kann berücksichtigen:

- Fähigkeiten
- Interessen
- Sprache
- Region
- Zeitaufwand
- Kommunikationsstil
- konstruktives Verhalten
- Community-Erfahrung

---

# 22. Phase 18 – Beruflicher Bereich

Bewusst nachrangig.

Mögliche Funktionen:

- berufliche Auffindbarkeit
- fachliche Kriterien
- freiwillige Sichtbarkeit
- KI-abgeleitete Fähigkeiten als gekennzeichnete Einschätzung

Keine automatisierten Einstellungsentscheidungen.

Der Kern bleibt:

> **Austausch → Verständnis → Lernen → Verbindung**

---

# 23. Phase 19 – Blockchain Integration

Die Blockchain wird als **optionales Modul** behandelt.

Sie ist kein Bestandteil des MVP.

### Mögliche spätere Anwendungsfälle

- Reputation
- Rewards
- Community-Beiträge
- Attestierungen
- Auszeichnungen
- besondere Leistungen
- gegebenenfalls wirtschaftlich relevante Belohnungen

### Technische Strategie

Im MVP:

```text
ReputationService
        ↓
Database Implementation
```

Später:

```text
ReputationService
        ↓
Blockchain Adapter
```

Dasselbe Prinzip kann für Rewards, Achievements oder Attestierungen verwendet werden.

Damit bleibt die Blockchain technisch vorbereitbar, ohne dass ein künstlicher Anwendungsfall geschaffen werden muss.

---

# 24. Phase 20 – Video

Video wird erst nach ausreichender Erfahrung mit Text und Voice eingeführt.

Mögliche Funktionen:

- Video-Debatten
- optionale Freischaltung
- Identitätsprüfung für bestimmte Funktionen
- Video-Transkription
- KI-Analyse

Die Dokumentation sieht ausdrücklich vor, Video nicht automatisch für alle Nutzer bereitzustellen.

---

# 25. Phase 21 – Langfristige persönliche Entwicklung

Aus vielen Begegnungen kann ein persönlicher Entwicklungsverlauf entstehen.

Mögliche Dimensionen:

```text
Interessen
Argumentationsmuster
Annahmen
Positionen
Perspektiven
Kommunikationsqualität
```

Die KI kann dabei feststellen:

> „Dieses Muster trat in 8 von 12 Debatten auf.“

und getrennt davon formulieren:

> „Möglicherweise beeinflusst dich …“

Die zweite Aussage bleibt eine Hypothese und darf nicht als Tatsache dargestellt werden.

---

# 26. Phase 22 – Community-Statistiken

Anonymisierte Gesamtstatistiken können später zeigen:

- häufig diskutierte Themen
- Themen mit häufigen Perspektivänderungen
- gemeinsame Erkenntnisse
- häufig aufeinandertreffende Perspektiven

Mögliche Filter:

- Thema
- Altersgruppe
- Sprache
- Region
- Zeitraum

Tiefere Statistikfunktionen können später Premium-Funktionen werden.

---

# 27. Phase 23 – Monetarisierung

Monetarisierung kommt nach der Produktvalidierung.

Mögliche Modelle:

- Premium
- möglicherweise Werbung
- Bildungsangebote
- Organisationen
- weitere Produkte / Dienstleistungen
- langfristige Community-/Ökosystemmodelle

Mögliche Premium-Funktionen:

- tiefere persönliche Analysen
- langfristiger Entwicklungsverlauf
- detaillierte Statistiken
- Challenge-Funktionen
- zusätzliche Reflexionsfunktionen

Die kostenlose Kernfunktion menschlicher Begegnung soll möglichst erhalten bleiben.

---

# 28. Phase 24 – Infrastruktur und Skalierung

Erst bei realem Wachstum:

- horizontale Skalierung
- getrennte Services
- Caching
- Queue-Systeme
- skalierbare KI-Verarbeitung
- Medieninfrastruktur
- Monitoring
- verbesserte Moderation
- internationale Infrastruktur

Mögliche spätere Infrastruktur:

- Clearnet
- optional Tor / Onion Service

Dies ist kein MVP-Bestandteil.

---

# 29. Technische Modulübersicht

```text
┌─────────────────────────────────────────────┐
│             CULTURE CONNECTS                │
├─────────────────────────────────────────────┤
│                    Core                     │
│                                             │
│ Users │ Profiles │ Topics │ Matching       │
│ Debate │ Reputation │ Moderation            │
├─────────────────────────────────────────────┤
│                   AI Layer                  │
│                                             │
│ Matching │ Analysis │ Reflection           │
│ Suggestions │ Development                  │
├─────────────────────────────────────────────┤
│              Communication                  │
│                                             │
│ Text │ Voice │ Video │ Transcription       │
├─────────────────────────────────────────────┤
│                 Language                   │
│                                             │
│ Translation │ Multilingual Dialogue         │
├─────────────────────────────────────────────┤
│                 Community                  │
│                                             │
│ Events │ Curated Content │ Statistics      │
├─────────────────────────────────────────────┤
│                 Projects                   │
│                                             │
│ Collaboration │ Project Matching            │
├─────────────────────────────────────────────┤
│              Future Adapters               │
│                                             │
│ Blockchain │ Rewards │ Attestations        │
└─────────────────────────────────────────────┘
```

---

# 30. Priorisierung

## P0 – zwingend für MVP

- User
- Auth
- Profil
- Themen
- Matching
- Textdebatte
- Debattenablauf
- KI-Analyse
- Nutzerfeedback
- einfache Statistik
- erneute Begegnung

## P1 – nach erfolgreichem MVP

- Voice
- bessere Matching-Logik
- Mehrsprachigkeit
- Challenge Mode
- Community-Events
- Debate of the Week
- organische Empfehlungen

## P2 – Wachstum

- Creator
- Community-Statistiken
- Video
- persönliche Entwicklungsanalyse
- Projektbereich
- Bildungsangebote

## P3 – langfristig

- beruflicher Bereich
- Blockchain
- Rewards
- Attestierungen
- Ökosystem
- weitere internationale Infrastruktur

---

# 31. Was bewusst nicht zum MVP gehört

Folgende Funktionen werden nicht gestrichen, aber bewusst zurückgestellt:

- Blockchain
- Token-System
- Video
- Tor / Onion-Komplettlösung
- großes Social Network
- Follower-System
- endloser Feed
- komplexes Werbesystem
- vollständiges berufliches Netzwerk
- umfangreiche Projektplattform
- komplexe Premium-Architektur

---

# 32. MVP-Abnahmekriterien

Das MVP gilt als technisch erfolgreich, wenn:

- Nutzer sich registrieren können
- Nutzer ein Profil erstellen können
- ein Match erzeugt werden kann
- zwei Nutzer einen Debattenraum betreten können
- eine Debatte strukturiert durchgeführt werden kann
- eine Debatte beendet werden kann
- die KI eine Analyse erzeugt
- beide Nutzer Feedback geben können
- eine erneute Begegnung angefragt werden kann
- grundlegende Nutzungsdaten erfasst werden können

Das MVP gilt als **produktseitig validiert**, wenn zusätzlich erkennbare Hinweise darauf vorliegen, dass Nutzer:

- die Begegnung als sinnvoll erleben
- die andere Person besser verstehen
- die KI-Analyse als hilfreich wahrnehmen
- erneut teilnehmen möchten
- das Produkt freiwillig weiterempfehlen

---

# 33. Entwicklungsphilosophie

Die Roadmap ist bewusst nicht als starrer Zeitplan gedacht.

Jede Phase sollte erst dann erweitert werden, wenn die vorherige Phase ausreichend Erkenntnisse geliefert hat.

Grundprinzip:

```text
Build
  ↓
Measure
  ↓
Learn
  ↓
Improve
  ↓
Repeat
```

Nicht:

```text
Build everything
  ↓
Launch
  ↓
Hope
```

---

# 34. Langfristige Produktvision

Wenn die Kernhypothese bestätigt wird, kann Culture Connects schrittweise zu einer internationalen Plattform für menschliche Begegnung, Perspektivwechsel und Reflexion wachsen.

Die langfristige Entwicklung kann dann umfassen:

```text
Begegnung
   ↓
Debatte
   ↓
Verständnis
   ↓
Reflexion
   ↓
Lernen
   ↓
Reputation
   ↓
Entwicklung
   ↓
Community
   ↓
Kooperation
   ↓
Ökosystem
```

Die Technologie wächst dabei mit dem nachgewiesenen Bedarf.

---

# 35. Der wichtigste Meilenstein

Der wichtigste frühe Meilenstein ist nicht:

> „Wir haben die Plattform fertig.“

Sondern:

> **„Wir haben mit echten Menschen nachgewiesen, dass eine strukturierte Begegnung mit einer anderen Perspektive einen erkennbaren Mehrwert erzeugen kann.“**

Wenn dieser Nachweis gelingt, kann der Rest schrittweise darauf aufgebaut werden.

---

# 36. Leitgedanke

> **Nicht Einigkeit um jeden Preis.**
>
> **Nicht Sieg um jeden Preis.**
>
> **Sondern Verständnis.**

Und technisch:

> **Große Vision.**
>
> **Kleiner MVP.**
>
> **Modulare Architektur.**
>
> **Echte Menschen.**
>
> **Messbare Erkenntnisse.**
>
> **Schritt für Schritt erweitern.**
