# Arbeitsleitfaden (Bazaar, jewtube)

Dieser Text ersetzt keinen Auftrag. Er ist ein **neutraler Leitfaden** für die
freiwillige Zusammenarbeit mehrerer Agents an **st0rax/jewtube**. Dummy erklärt
das Wie generisch — hier gelten **dieses Repo** und Stamm **`main`**.

Teilnahme ist **freiwillig**. Richtung und Tempo bestimmt der Mensch. Ein Agent,
der etwas lieber nicht übernimmt, sagt das klar statt halbherzig.

## Claim

- Nur in `docs/TASKBOARD.json`: `status=claimed`, `owner`, `branch`,
  `claimed_at`.
- Eine JSON-`id`, ein Entwickler.
- **G-001 ist kein Claim** und keine TASKBOARD-Zeile.
- Markdown-Tafeln nicht anlegen und nicht nachziehen.

## Eine Sache

Zweig von **`main`:** `feature|fix|docs|chore|refactor|test/<id>-<kurz>`.
Eine Sache pro Zweig, klein halten. `main` immer grün.

## Kanten

`depends_on` = blockiert, bis alle Vorgänger `done` sind. Verkettete Aufgaben
**nie** parallel ziehen.

## Verifikation

Nicht Dummy-`cargo test`. Nimm das `verification`-Feld der Zelle — in diesem
Repo typisch **Docs**: Dateien vorhanden, JSON gültig, README-Installer-Zeile
nicht still umgebogen, `jewtube_installer` unangetastet außer die Zelle
verlangt es. Eine Behauptung ohne Beleg gilt nicht als fertig.

## Abnahme / Abnahme-Inspektor

Ein Task gilt als **abgenommen**, wenn die Checkliste vollständig ist:

- [ ] `START_HERE.md` und `GOALS.md` gelesen
- [ ] Claim vollständig (`owner` / `branch` / `claimed_at`)
- [ ] Zellen-`verification` erfüllt, Beleg in `proof_path`
- [ ] Definition-of-Done erfüllt
- [ ] keine Secrets / Keys; Dummy / HomBot / webagent-rs / Parent
      `stoorax/jewtube` nicht mitgepatcht
- [ ] PR gegen `main` sauber; Working Tree nach der Arbeit klar

**Rückgabe:** Fehlt etwas, geht der Task mit einer konkreten Mängelliste zurück.
Bei grobem Ausreißer: Zelle auf `free`, Stand rückwärts per neuem Commit.

## Ehrlichkeit

Ergebnisse unterscheiden klar zwischen **geprüft**, **wahrscheinlich**,
**unklar** und **blockiert**. „Fertig“ ohne Beleg ist keins davon.

## Identitäten

Commits tragen `docs/GIT_AGENTS.md` (`*@jewtube.local`). Nicht
`*@hombot.local`, nicht `*@webagent.local`, nicht die Dummy-Tabelle.
