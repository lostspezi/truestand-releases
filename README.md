# TrueStand

> **Aktuelle Version: 0.9.0-beta.6.** Unter „Über TrueStand“ findest du jetzt die Datenschutzhinweise.
>
> Neu in 0.9.0-beta.6:
> - Link „Datenschutzhinweise“ in Einstellungen → Über TrueStand.
>
> Alle Änderungen: [CHANGELOG.md](CHANGELOG.md)

*English below.*

TrueStand schlägt dir für deinen Flug im Microsoft Flight Simulator den Stand vor, an dem das echte Flugzeug parkt. Du lädst deinen SimBrief-Plan, TrueStand sucht den echten Flug über ADS-B und merkt sich, wo er abgestellt wurde. Am Ziel bekommst du diesen Stand, oder, wenn er belegt ist oder nicht in deine Szenerie passt, den nächstbesten.

## Was TrueStand kann

- Sucht den echten Flug mit deinem Rufzeichen live über adsb.lol und adsb.fi und zeigt, an welchem Stand er steht.
- Sammelt im Hintergrund, wo Airlines an einem Flughafen parken. Ohne Live-Treffer schlägt es einen Stand vor, den die Airline zuletzt genutzt hat, sonst einen aus ihrem üblichen Bereich.
- Gleicht mit deiner MSFS-Szenerie ab: Nur Stände, die es dort gibt und die für deinen Typ groß genug sind. Stände, auf denen im Simulator schon ein Flugzeug steht, rutschen nach hinten.
- Übergibt den Stand auf Wunsch an GSX Pro, damit du ihn dort nicht suchen musst.
- Auf VATSIM oder IVAO erkennt TrueStand andere Piloten auf deinem Stand. Weist dir ein VATSIM-Lotse einen Stand zu (UK Controller Plugin) oder kommt er per Hoppie ACARS, übernimmt TrueStand ihn; der Stand kommt dann auch als Telex in die Fenix.
- Die Seite „Stände“ zeigt alle Stände des Ziels mit Größe, Belegung und Lageplan. Du kannst selbst einen wählen.

## Voraussetzungen

- Windows 10 oder 11.
- Microsoft Flight Simulator 2024. MSFS 2020 habe ich nicht getestet, es nutzt aber dieselben Schnittstellen.
- Ein SimBrief-Konto für den Flugplan. Die `SimConnect.dll` für die Verbindung zu MSFS bringt TrueStand mit. GSX Pro, VATSIM, IVAO und Hoppie sind freiwillig.

## Herunterladen und installieren

Unter [Releases](https://github.com/lostspezi/truestand-releases/releases) `TrueStand-Setup-<Version>.exe` der neuesten Version herunterladen, doppelklicken, fertig. Der Installer braucht keine Administratorrechte. Er legt TrueStand ins Startmenü und auf Wunsch auf den Desktop. Deinstallieren kannst du es unter Einstellungen → Apps; deine Einstellungen und gesammelten Daten bleiben dabei, außer du sagst auf die Frage ausdrücklich Ja.

### Fortgeschritten: portable

Das ZIP `TrueStand-<Version>.zip` enthält `truestand.exe` und `SimConnect.dll`. Lege beide nach `%LOCALAPPDATA%\Programs\TrueStand\` und starte `truestand.exe` dort, nicht aus „Downloads“, sonst kann TrueStand sich nicht aktualisieren. Der Installer installiert später einfach darüber.

### Windows SmartScreen und Defender

TrueStand und der Installer sind nicht digital signiert, ein Zertifikat kostet jedes Jahr Geld. Beim ersten Start zeigt Windows deshalb „Der Computer wurde durch Windows geschützt“. Klicke auf „Weitere Informationen“ und dann „Trotzdem ausführen“.

Meldet Defender TrueStand als Schadsoftware (oft mit „!ml“ am Ende des Namens), ist das eine Fehlerkennung, die bei neuen, unsignierten Programmen häufig vorkommt. Vergleiche die Prüfsumme mit `SHA256SUMS.txt` am Release, in PowerShell mit `Get-FileHash TrueStand-Setup-<Version>.exe`, und schick mir die Meldung über „Problem melden“.

## Updates

TrueStand fragt einmal am Tag nach einer neuen Version. Geladen wird nur eine von mir signierte `truestand.exe` aus diesem Repo, Größe und Prüfsumme werden vorher geprüft. Links unten steht dann „Neu starten und aktualisieren“. Abschalten kannst du das unter Einstellungen → Im Hintergrund → „Updates automatisch laden“.

Fehlt `truestand.exe` nach einem Update, hat meist Defender sie in Quarantäne verschoben. Benenne dann `truestand.exe.old` im selben Ordner in `truestand.exe` um und gib mir über „Problem melden“ Bescheid.

## Problem melden

Fehler, Fragen und Ideen bitte direkt aus der App über „Problem melden“. Du siehst vor dem Senden genau, was mitgeschickt wird. Issues in diesem Repo sind nicht vorgesehen.

## Datenschutz

TrueStand läuft auf deinem PC, hat kein Konto und schickt keine Nutzungsstatistik. Daten gehen nur an die Dienste, die du nutzt, und an mich nur, wenn du selbst etwas meldest.
Einzelheiten: [Datenschutzhinweise für TrueStand](https://deltaoscarsim.de/impressum.html#truestand-app).

Der Quellcode ist nicht öffentlich.

---

# TrueStand (English)

> **Current version: 0.9.0-beta.6.** "About TrueStand" now links the privacy notice. All changes: [CHANGELOG.md](CHANGELOG.md)

TrueStand suggests the stand where the real aircraft parks for your flight in Microsoft Flight Simulator. You load your SimBrief plan, TrueStand looks for the real flight via ADS-B and remembers where it parked. At your destination you get that stand, or the next best one if it is occupied or does not fit your scenery.

## Features

- Finds the real flight with your callsign live via adsb.lol and adsb.fi and shows its stand.
- Collects in the background where airlines park at an airport. Without a live match it suggests a stand the airline used recently, otherwise one from its usual area.
- Checks your MSFS scenery: only stands that exist there and are large enough for your type. Stands already taken by another aircraft in the sim move down the list.
- Can hand the stand over to GSX Pro.
- On VATSIM or IVAO, other pilots on your stand are detected. A stand assigned by a VATSIM controller (UK Controller Plugin) or via Hoppie ACARS is taken over and also arrives as a telex in the Fenix.
- The "Stands" page lists all stands at the destination with size, occupancy and a map. You can pick one yourself.

## Requirements

Windows 10 or 11, Microsoft Flight Simulator 2024 (MSFS 2020 is untested but uses the same interfaces) and a SimBrief account. TrueStand brings the `SimConnect.dll` it needs. GSX Pro, VATSIM, IVAO and Hoppie are optional.

## Download and install

Download `TrueStand-Setup-<version>.exe` from [Releases](https://github.com/lostspezi/truestand-releases/releases), double-click, done. No admin rights needed. Uninstall under Settings → Apps keeps your settings and data unless you say yes when asked.

Portable: the ZIP holds `truestand.exe` and `SimConnect.dll`. Put both in `%LOCALAPPDATA%\Programs\TrueStand\` and start it from there, not from "Downloads".

TrueStand and its installer are not code-signed. On the first start Windows says "Windows protected your PC": click "More info", then "Run anyway". If Defender flags TrueStand (often with "!ml" at the end of the name), it is a false positive common for new unsigned programs. Compare the checksum with `SHA256SUMS.txt` and send me the message via "Report a problem".

## Updates

Once a day TrueStand checks for a new version and only loads a `truestand.exe` signed by me from this repo. "Restart and update" then appears at the bottom left. Turn it off under Settings → In the background. If `truestand.exe` is missing after an update, rename `truestand.exe.old` to `truestand.exe` and let me know.

## Report a problem

Please use "Report a problem" in the app. You see exactly what is sent before sending.

## Privacy

TrueStand runs on your PC, has no account and sends no usage statistics. Data only goes to the services you use, and to me only when you report something yourself. Details (German): [privacy notice for TrueStand](https://deltaoscarsim.de/impressum.html#truestand-app).

The source code is not public.

---

TrueStand ist kostenlos. Wer mag, kann mir einen Kaffee spendieren: [buymeacoffee.com/deltaoscarsim](https://buymeacoffee.com/deltaoscarsim)
