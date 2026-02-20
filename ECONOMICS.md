# Makroökonomisches Modell

## Wirkzusammenhänge

Das Solon-Protokoll definiert fünf ökonomische Kernvariablen und deren Wechselwirkungen:

### Variablen

| Variable | Symbol | Beschreibung |
|---|---|---|
| **Geldmenge** | `M` | Gesamtmenge zirkulierender Solon |
| **Demurrage-Rate** | `D` | Jährlicher Wertverlust durch Rost (%) |
| **UBI-Höhe** | `U` | Monatliche Auszahlung pro Bürger (Solon) |
| **Kreditzins** | `r` | Dynamischer Zins des Liquidity Pool (%) |
| **Umlaufgeschwindigkeit** | `V` | Wie oft ein Solon pro Jahr den Besitzer wechselt |

### Formeln

**Demurrage-Adjustment:**
```
D(t+1) = D(t) + α · (M_aktuell – M_ziel)
```

**Projektdringlichkeit (Genesis-Nodes):**
```
Up = (Dw · Sp) / Rk
```

**Anti-Sybil-Decay:**
```
Wv = PA · e^(–γ · n)
```

### Qualitative Wirkungsketten

```
UBI-Erhöhung → M steigt → D steigt automatisch → Hortung teurer → V steigt → Wirtschaft beschleunigt
                                                                                          ↓
                                                            Wenn V zu hoch → Inflation → Liquid Democracy senkt UBI
```

```
Demurrage → Anreiz, Solon auszugeben ODER in Pool einzuzahlen → Kreditzins sinkt → Investitionen steigen
```

```
Fractional Streaming → Kreditnehmer zahlt Demurrage nur auf aktuelle Tranche → Baukosten kalkulierbar
```

## Extremszenarien (To-Do: Simulieren)

| Szenario | Erwartete Dynamik | Failsafe |
|---|---|---|
| **Deflation** | Nachfrageeinbruch → weniger Solon in Umlauf → D sinkt automatisch | Liquid Democracy kann UBI temporär erhöhen |
| **Energiekrise** | Reale Knappheit → Genesis-Nodes priorisieren Energieprojekte | Kleisthenes-Mechanismus bei Deadlock |
| **Demographie-Schock** | Weniger Arbeitskräfte → KI-Automation übernimmt mehr Routine | Heartbeat erkennt auch KI-gestützte Beiträge |
| **Populistische Demurrage-Senkung** | D → 0 → Hortung → Wirtschaft stoppt | Kein Failsafe — bewusst. Konsequenzen als Feedback |

## Simulation (geplant)

- Agent-Based Model in Python (Mesa-Framework)
- Parameter: 100.000 Agenten, 20 Jahre Simulation
- Metriken: Gini-Koeffizient, Umlaufgeschwindigkeit, Kreditvolumen, Pool-Auslastung

---

*Pull Requests für Simulationsmodelle sind besonders willkommen.*
