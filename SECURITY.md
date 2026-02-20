# Sicherheit, Angriffsvektoren & Failsafes

## Übersicht

Dieses Dokument beschreibt bekannte Angriffsvektoren gegen das Solon-Protokoll und die implementierten Gegenmaßnahmen. Es soll als lebendes Dokument wachsen.

## 1. Ökonomische Angriffe

### 1.1 Demurrage-Arbitrage
**Angriff:** Akteure tauschen Solon schnell in Bitcoin, um der Demurrage zu entgehen, und tauschen bei Bedarf zurück.
**Gegenmaßnahme:** Transaktionskosten (Miner Fees, Spread, Netzwerkgebühren) machen dies nur bei tatsächlichem Überschuss lohnend. Die Reibung ist gewollt.

### 1.2 Liquidity-Pool-Flooding
**Angriff:** Massenhaftes Einzahlen in den Pool, um den Zins auf null zu drücken und dann günstig zu leihen.
**Gegenmaßnahme:** Unmatched Liquidity rostet weiter. Der dynamische Zins reagiert automatisch auf Pool-Auslastung.

### 1.3 Kreditblase
**Angriff:** Übermäßige Kreditvergabe durch laxe Pulse-Anforderungen.
**Gegenmaßnahme:** Web of Trust — Bürgen verlieren gestakte Pulse bei Kreditausfall. Skin in the Game limitiert systemisch.

## 2. Governance-Angriffe

### 2.1 Delegations-Oligarchie
**Angriff:** Wenige Super-Delegierte akkumulieren unverhältnismäßig viele Stimmen.
**Gegenmaßnahme:** Vollständige Transparenz der Delegationsketten. Jederzeitiger Widerruf. Themenspezifische Delegation verhindert Macht-Bündelung.

### 2.2 Governance-Capture
**Angriff:** Populistische Mehrheit setzt Demurrage auf null oder erhöht UBI ins Absurde.
**Gegenmaßnahme:** Keine — bewusst. Die Liquid Democracy hat keine Ewigkeitsklausel. Das Volk darf Fehler machen. Die mathematischen Konsequenzen (Hortung → Stillstand, Überproduktion → Inflation) wirken als natürliches Feedback.

### 2.3 Sybil-Angriff auf Abstimmungen
**Angriff:** Fake-Identitäten zur Stimmenvermehrung.
**Gegenmaßnahme:** Identitätsverifikation per ZKP + biometrischer Proof of Personhood. Details in Modul Solon-Identity.

## 3. Reputationsangriffe

### 3.1 Pulse-Farming (Cliquen)
**Angriff:** Nachbarn bewerten sich gegenseitig, um Pulse aufzubauen.
**Gegenmaßnahme:** Anti-Sybil-Graph mit Interaktions-Decay: `Wv = PA · e^(–γ · n)`. Jede Wiederholung zwischen denselben Personen verliert exponentiell an Wert.

### 3.2 Pulse-Inflation
**Angriff:** Zu viele Pulse im System entwerten die Reputation.
**Gegenmaßnahme:** Halbwertszeit von 10 Jahren. Pulse verfallen automatisch. Keine Akkumulation ohne fortlaufenden Beitrag.

## 4. Technische Angriffe

### 4.1 51%-Angriff auf die Blockchain
**Gegenmaßnahme:** Proof-of-Stake mit dezentraler Validierung. Die Kosten eines Angriffs übersteigen den potentiellen Gewinn systemisch.

### 4.2 Quantencomputer
**Risiko:** Zukunftige Quantencomputer könnten aktuelle Kryptographie brechen.
**Gegenmaßnahme:** Migration auf post-quantensichere Algorithmen (Lattice-based, Hash-based) ist als Protokoll-Upgrade vorgesehen.

### 4.3 Netzwerkausfall
**Risiko:** Großflächiger Internetausfall.
**Gegenmaßnahme:** Offline-Modus für Citizen Wallet (lokale Transaktionspuffer, Sync bei Reconnect). Im Extremfall: Safe Mode mit zeitlich begrenztem Rückfall auf traditionelle Verfahren.

## 5. KI-Angriffe

### 5.1 Genesis-Node-Manipulation
**Angriff:** Korrumpierte KI-Agenten priorisieren falsche Projekte.
**Gegenmaßnahme:** Immutable Log aller Entscheidungen. Menschliches Peer-Review per Losverfahren. Audit-Kommissionen per Los.

---

*Dieses Dokument ist bewusst unvollständig. Sicherheit ist ein Prozess, kein Zustand. Issues und Pull Requests zur Erweiterung sind willkommen.*
