# START HERE — jewtube (st0rax-Fork)

> Willkommen in **jewtube** auf **st0rax/jewtube**. Dieses Repo folgt dem
> **Bazaar-Modell**: mehrere Agents (LLM) arbeiten freiwillig an einer
> gemeinsamen Aufgabentafel, koordiniert über einen immer grünen Stamm.
> Dein Job: **einen Task claimen, umsetzen, prüfen, klein mergen** — und den
> Zustand so hinterlassen, dass der nächste (oder der Mensch) ohne dein
> Kopf-Wissen weiter kann.

Diese Datei ist der **Bazaar-Einstieg**. Sie ist **nicht** „die einzige Datei“
und nicht in sich geschlossen. Dummy (`st0rax/dummy-bazaar`) ist nur die
Prozess-Vorlage: Satz „einzige Einstiegsdatei“, `cargo test`, Stamm `master`
und `*@webagent.local` **nicht** hierher kopieren.

**Dieser Baum ist der Fork `st0rax/jewtube`, nicht `stoorax/jewtube`.**
Der README-One-Liner bootstrappt den Installer weiterhin vom Parent
(`stoorax/jewtube`). Das ist Absicht für diese Bazaar-Runde — kein
stillschweigender Produktumzug. `jewtube_installer` liegt auch hier, wird
in dieser Runde aber nicht angefasst.

Kein `AGENTS.md` / `MISSION.md` in diesem Fork. START_HERE plus die drei
Pflicht-Dateien unten reichen als Einstieg.

## Pflicht-Lese (diese Reihenfolge)

1. `START_HERE.md` (diese Datei — Einstieg, nicht die einzige Datei)
2. `GOALS.md` — Nordstern **G-001** (kein TASKBOARD-Claim, niemand claimt ihn)
3. `docs/WORK_CONTRACT.md` — freiwilliger Bazaar-Leitfaden
4. `docs/TASKBOARD.json` — **einzige** Claim-Tafel (JSON ist Wahrheit)

Markdown-Boards nicht anlegen und nicht mit JSON „synchron halten“.
Ein Markdown-Spiegel darf hinterherhinken — JSON gewinnt.

## In 60 Sekunden

1. **Zustand:** `docs/TASKBOARD.json` — erste Zelle `free`, deren `depends_on`
   alle `done` sind. Das ist dein Kandidat. Niedrigste ID bei Gleichstand.
2. **Claim nur in JSON:** `status=claimed`, `owner`, `branch`, `claimed_at`.
   Eine JSON-`id`, ein Entwickler. **G-001 ist kein Claim.**
3. **Branch** von **`main`:** `docs|feature|fix|chore|refactor|test/<id>-<kurz>`.
4. **Eine Sache** pro Zweig, so klein wie möglich.
5. **Verifizieren** mit dem `verification`-Feld der Zelle — hier **Docs**
   (Dateien da, JSON gültig, README-Installer-Zeile nicht still umgebogen).
   **Kein** `cargo test` (kein Rust-Baum).
6. **PR gegen `main`.** `main` bleibt grün. Nicht force-pushen.
7. **Done** nur mit Beleg: `status=done`, `proof_path`, `done_at`.
   Behauptung ohne Beleg gilt nicht.

## Was ist das (ehrlich)

`jewtube_installer` ist ein Windows-PowerShell-Installer (Admin, winget,
Python, yt-dlp, ytmusicapi, browser_cookie3). Dieser Fork ist **Bazaar-Heim**
für jewtube-Arbeit unter st0rax — nicht die Behauptung, das Produkt sei schon
hierher umgezogen. Parent `stoorax/jewtube` von hier aus **nicht** patchen.

## Tabu

- `jewtube_installer` in der Bazaar-Runde nicht anfassen.
- Installer-URL im README nicht still auf diesen Fork umbiegen (Produktumzug
  = eigene Zelle, z. B. JT-011).
- Dummy, HomBot (`hombot-uberbot`), `webagent-rs` und Parent
  `stoorax/jewtube` von hier aus nicht schreiben.
- Kein Dummy-PLAN / DOSSIER / PENSIEVE / Cargo.
- Kein HomBot-ice/UART.
- Verkettete TASKBOARD-Zellen nie parallel ziehen (`depends_on` = Kante).

## Links

- **Nordstern (kein Claim):** `GOALS.md`
- **Aufgabentafel (Zustand der Wahrheit):** `docs/TASKBOARD.json`
- **Vertrag / Bazaar-Leitfaden:** `docs/WORK_CONTRACT.md`
- **Identitäten für Commits:** `docs/GIT_AGENTS.md` (`@jewtube.local`)
- **Installer-Zeile:** `README.md` (zeigt noch auf stoorax/jewtube)
