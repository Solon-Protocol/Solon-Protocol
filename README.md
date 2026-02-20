# SOLON Protocol

**Ein dezentrales Betriebssystem für menschliche Koordination.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## Was ist das?

SOLON ist ein Open-Source-Protokoll für dezentrale Governance, transparente Ressourcenallokation und reputationsbasierte Kooperation. Es kombiniert:

- **Duales Geldsystem** — Bitcoin (Wertspeicher) + Solon (Umlaufwährung mit programmierbarer Demurrage)
- **Liquid Democracy** — direkt abstimmen oder an Experten delegieren, jederzeit widerrufbar
- **Heartbeat** — multidimensionale Reputation via nicht-übertragbare Pulse (Soulbound Tokens)
- **Genesis-Nodes** — KI-Agenten für autonome Ressourcenallokation bei öffentlichen Projekten
- **Liquidity Pool** — dezentrale Kreditvergabe mit dynamischem Zins und Solon-Bonds

Das vollständige **[Whitepaper](WHITEPAPER.md)** lesen.

## Warum?

Jedes politische System löst Koordination und erzeugt Korruption. Jedes Wirtschaftssystem bewertet, was bepreist werden kann, und ignoriert, was zählt. Jedes Arbeitssystem koppelt Überleben an Erwerbstätigkeit — auch wenn Maschinen die Erwerbstätigkeit ersetzen.

SOLON ist kein Fix. Es ist ein Experiment. Open Source, opt-in, forkable.

## Status

🟡 **Pre-Alpha.** Das Whitepaper ist veröffentlicht. Der Code wird gebaut. Wir brauchen Hilfe.

## Mitarbeiten

| Du bist... | Du kannst... |
|---|---|
| **Solidity-Entwickler** | Smart Contracts bauen und auditieren (Solon-Core, Liquid Democracy, Pulse) |
| **Mobile-Entwickler** | Die Citizen Wallet bauen (React Native / Flutter) |
| **KI/ML-Ingenieur** | Genesis-Node-Agenten entwickeln und trainieren |
| **Kryptograph** | ZKP-Voting, Proof of Care/Compute und Identitätsmodule implementieren |
| **Ökonom** | Demurrage-System und Liquidity Pool modellieren und stresstesten |
| **Jurist** | Rechtsrahmen für Community-Währungen und DAOs erkunden |
| **Autor / Übersetzer** | Whitepaper übersetzen, Dokumentation schreiben |
| **Jeder** | Mitmachen, lokale Gruppe starten, kochen |

Siehe **[CONTRIBUTING.md](CONTRIBUTING.md)** für Details.

## Projektstruktur

```
solon-protocol/
├── WHITEPAPER.md              # Die vollständige Protokollspezifikation
├── CONTRIBUTING.md             # Wie man mitmacht
├── LICENSE                     # MIT-Lizenz
├── contracts/                  # Smart Contracts (Solidity)
│   ├── SolonCore.sol          # Demurrage-Währung + Geldschöpfung
│   ├── LiquidityPool.sol      # Dezentrale Kreditvergabe + Solon-Bonds
│   ├── LiquidDemocracy.sol    # Abstimmung und Delegation
│   └── Pulse.sol              # Soulbound Reputation Tokens
├── agents/                     # Genesis-Node KI-Agenten
│   ├── genesis_node.py        # Projektmanagement-Agent
│   └── allocation.py          # Ressourcen-Allokationsalgorithmus
├── wallet/                     # Citizen Wallet App
├── docs/                       # Weiterführende Dokumentation
│   ├── ECONOMICS.md           # Makroökonomisches Modell
│   ├── SECURITY.md            # Angriffsvektoren & Failsafes
│   └── GOVERNANCE.md          # Protokoll-Updates & Soft Forks
└── simulations/                # Ökonomische Modelle und Stresstests
```

## Kernkonzepte

### Der Solon
Eine souveräne Umlaufwährung. Jeder Bürger erhält ein bedingungsloses Grundeinkommen. Der Solon unterliegt einer programmierten Demurrage — er rostet. Die Demurrage-Rate passt sich algorithmisch an die zirkulierende Geldmenge an: `D(t+1) = D(t) + α · (M_aktuell – M_ziel)`. Geld, das nicht fließt, verliert an Wert. Geld, das zirkuliert, treibt die Wirtschaft an.

### Der Liquidity Pool
Wer Solon vor dem Rost schützen will, verleiht sie über den dezentralen Pool. Aber: Unmatched Liquidity rostet weiter — erst wenn ein Kreditnehmer das Geld tatsächlich abruft, erhält der Geldgeber einen Solon-Bond und entgeht der Demurrage. Kredite fließen per Fractional Streaming nach Baufortschritt. Der algorithmische Zins reguliert Angebot und Nachfrage ohne Zentralbank.

### Bitcoin
Der private Wertspeicher. Nicht manipulierbar, nicht konfiszierbar, deflationär. Was langfristig gehalten werden soll, wird in Bitcoin gespeichert. Der Solon ist zum Fließen da, Bitcoin ist zum Bewahren da.

### Liquid Democracy
Deine Stimme, deine Wahl. Direkt abstimmen bei Themen, die du verstehst. An Experten delegieren bei Themen, die du nicht verstehst. Delegation jederzeit widerrufen. Zwei Budgetkreisläufe: Mikro-Budget (Kiez) und Makro-Budget (Infrastruktur).

### Der Heartbeat (Pulse)
Kein Score. Kein Ranking. Ein Mosaik deiner Beiträge — Pflege, Handwerk, Forschung, Mentoring, Kunst, Code — bestätigt von denen, die sie bezeugt haben. Nicht übertragbar. Nicht handelbar. Soulbound. Dein. Halbwertszeit: 10 Jahre.

### Genesis-Nodes
Für jedes genehmigte öffentliche Projekt wird ein dedizierter KI-Agent instanziiert. Er prüft Machbarkeit, verhandelt autonom mit anderen Agents um knappe Ressourcen (Yield & Lease), dokumentiert alles auf einem Immutable Log. Dringlichkeit berechnet sich als: `Up = (Dw · Sp) / Rk`. Bei Deadlocks greift der Kleisthenes-Mechanismus: drei per Los gewählte Fachexperten entscheiden.

### Anti-Sybil-Graph
Der Wert gegenseitiger Bewertungen sinkt exponentiell mit jeder Wiederholung: `Wv = PA · e^(–γ · n)`. Cliquen werden entwertet, echte Vielfalt belohnt. Stille Arbeit (Code, Pflege) wird per Proof of Compute/Care via Zero-Knowledge Proofs validiert.

## Prinzipien

1. **Regeln im Code, nicht in Verträgen.** Smart Contracts führen aus — sie verhandeln nicht.
2. **Transparenz der Macht, Privatsphäre der Bürger.** Der Staat ist Glas; der Bürger ist souverän.
3. **Keine Delegation ohne Widerruf.** Vertrauen ist ein laufender Vertrag, kein Blankoscheck.
4. **Ressourcenverbrauch ist mathematisch gebunden.** Niemand druckt Solon ohne demokratischen Beschluss.
5. **Anreize, nicht Strafen.** Der Heartbeat öffnet Türen. Er schließt sie nie.

## Der Name

Solon von Athen (638–558 v. Chr.) reformierte die athenische Verfassung, erließ Schulden und legte den Grundstein für die Demokratie. Dann verließ er Athen freiwillig für zehn Jahre, damit das Volk lernte, sich selbst zu regieren, anstatt von ihm abhängig zu sein.

Das SOLON-Protokoll folgt derselben Logik: Das Werkzeug bauen, dann zurücktreten.

## Die Bücher

Die theoretische Grundlage des Protokolls wird in drei Bänden erarbeitet:

- **Band I: GELD — Der Speicher der Zeit** (Von Muscheln über Gold und Fiat zu Bitcoin und Solon)
- **Band II: STAAT — Das Betriebssystem der Menschheit** (Von Lagerfeuern über Athen und Lobbykratie zu Liquid Democracy)
- **Band III: ARBEIT — Die Entfaltung des Tuns** (Von Jägern und Sammlern über Bullshit Jobs zu Homo Ludens)

---

*„Ich habe dieses Protokoll nicht geschrieben, um Recht zu haben. Ich habe es geschrieben, um ein Gespräch zu beginnen."*
— SOLON

## Lizenz

MIT License. Frei verwendbar, modifizierbar, verteilbar. Siehe [LICENSE](LICENSE).
