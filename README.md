# App-Hub – alle deine Web-Apps an einem Ort

Der App-Hub ist eine Startseite für deine Web-Apps im Piraten-Look (One-Piece-Stil): Steckbrief-Kacheln nach Kategorien, mit Notizen und Online-Check. Er besteht aus **einer einzigen Datei** (`index.html`), braucht weder Server noch Konto und speichert alles **nur in deinem Browser**.

**Adresse:** https://hezudemnrik-eng.github.io/Uebersicht/

Beim ersten Start ist **Blueprint** schon eingetragen (Kategorie „Minecraft“).

## Einmalig einrichten (GitHub Pages)

1. Repo **öffentlich** machen: Settings → General → ganz unten „Change visibility“ → Public.
   Bei einem kostenlosen GitHub-Konto veröffentlicht Pages nur öffentliche Repos. Deine eingetragenen Apps und Notizen landen dabei **nicht** im Repo, die bleiben in deinem Browser.
2. Settings → Pages → **Source: „GitHub Actions“**.
3. Danach veröffentlicht jede Änderung auf `main` die Seite automatisch (Workflow „App-Hub veröffentlichen“).

## Bedienen

- **Öffnen:** Klick auf eine Kachel. Unter Einstellungen → „Apps öffnen“ wählst du neuer Tab oder gleicher Tab. „Automatisch“ öffnet im Browser einen neuen Tab und als installierte App am iPhone im selben Fenster.
- **Suchen:** oben ins Suchfeld tippen. Gesucht wird in Name, Adresse, Beschreibung, Notizen und Kategorie. Taste **/** springt ins Feld, **Enter** öffnet den ersten Treffer.
- **Hinzufügen:** „+ App“. Name, Adresse (ohne `https://` geht auch), Kategorie (oder direkt eine neue), Icon, Farbe, Kurzbeschreibung und Notizen (Markdown mit Vorschau).
  - **Icon:** Piraten-Icon (Strohhut, Flagge, Schiff, Teufelsfrucht …), das Icon der Website (`favicon.ico`, optional eigene Bild-Adresse) oder ein Buchstabe bzw. Emoji.
  - Erlaubt sind nur Web-Adressen (`https://`, `http://`).
- **Bearbeiten & löschen:** der Stift auf der Kachel. Gelöschtes lässt sich über „Rückgängig“ zurückholen.
- **Details:** das Info-Symbol zeigt Adresse, Status mit Uhrzeit und die Notizen.

## Ordnen

- **Am PC:** Kacheln ziehen, innerhalb einer Kategorie oder in eine andere (auch auf die Überschrift einer zugeklappten Kategorie).
- **Am Handy:** „Anordnen“ antippen und mit den Pfeilen verschieben, oder im Bearbeiten-Dialog die Kategorie wechseln.
- **Kategorien:** im Anordnen-Modus (am PC auch beim Darüberfahren) umbenennen, nach oben/unten schieben oder löschen. Die Apps einer gelöschten Kategorie landen unter „Ohne Kategorie“.
- Ein Klick auf den Kategorienamen klappt sie zu oder auf. Das bleibt gespeichert. Zugeklappte Kategorien zeigen ihre App-Icons in der Kopfzeile.
- **Flaggenfarbe:** beim Bearbeiten einer Kategorie wählbar, sonst automatisch.
- **Kategorien-Leiste:** ab zwei Kategorien oben eingeblendet. Ein Klick springt zur Kategorie, „Alle zu“ / „Alle auf“ klappt alle gleichzeitig. Kleine Kategorien stehen am PC nebeneinander.

## Online-Check

Beim Öffnen, beim Zurückkehren nach mehr als 5 Minuten und mit **„Alle prüfen“** fragt der App-Hub jede Adresse an (Zeitlimit 6 Sekunden).

- **Grün:** antwortet. **Rot:** keine Antwort, Zeitüberschreitung oder Fehlerseite. **Grau umrandet:** kann nicht geprüft werden.
- Bei Apps unter `hezudemnrik-eng.github.io` (z. B. Blueprint) erkennt er auch Fehlerseiten wie **404**.
- Bei fremden Seiten sieht der Browser nur, *ob* der Server antwortet. Eine Fehlerseite zählt dort als online.
- Adressen mit `http://` kann der Browser von der `https`-Seite aus nicht prüfen („Unbekannt“).

## Daten übertragen & sichern

- **Daten übertragen** (unten links): Code kopieren oder teilen und auf dem anderen Gerät einfügen, oder die Backup-Datei (`apphub-backup-JJJJ-MM-TT.json`) laden. Hat das Ziel schon eigene Apps, wählst du **Zusammenführen** (bei gleichen Einträgen gewinnt die zuletzt geänderte Version, gleichnamige Kategorien und gleiche Adressen werden zusammengelegt) oder **Alles ersetzen**.
- Blueprint hat einen eigenen Code (`BLUEPRINT1:`) und wird in Blueprint selbst übertragen. Der App-Hub erkennt Blueprint-Daten und sagt dir das.
- **Browserdaten löschen = Daten weg.** Ab und zu unter Einstellungen „Als Datei herunterladen“.
- **Keine Passwörter in die Notizen.** Sie liegen unverschlüsselt im Browser und stehen auch im Übertragungs-Code.

## Am iPhone installieren

In Safari die Adresse öffnen → Teilen-Symbol → **„Zum Home-Bildschirm“**. Blueprint hat in der Seitenleiste den Link **„← Alle Apps“** zurück zum App-Hub.

## Technik

- Gleiche Adresse wie Blueprint (`hezudemnrik-eng.github.io`), deshalb getrennte Speicher-Schlüssel: App-Hub `apphub:*`, Blueprint `blueprint:*`. Die beiden beeinflussen sich nicht.
- Lädt nichts aus dem Internet außer den Anfragen für den Online-Check und die Website-Icons.

## Lizenzen

- Überschriften-Schrift: **Bangers** von Vernon Adams, SIL Open Font License 1.1
- Piraten-Icons: selbst gezeichnet (frühere Pixel-Icons werden automatisch auf passende neue Icons umgestellt)
