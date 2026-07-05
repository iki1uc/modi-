YZIU — RAW Bench System (v1.0)
YZIU ist ein vollständiges RAW‑Bench‑System bestehend aus UI‑Viewer, Bench‑Stations, Operator‑Mapping und Bench‑Plan.
Es dient zur Durchführung, Darstellung und Prüfung von RAW‑Bench‑Tests.

1. Struktur
UI
index.html  
RAW‑Bench‑Viewer
Input → Output (RAW‑Durchleitung)
RESPO‑ID: yziu.bench

Items
station-01.bench.item

station-02.bench.item

yziu-bench-plan.item

yziu-operator.item

2. Bench‑Stations
Station 01
RAW‑Input: ? A, ? B, ? C

RAW‑Output: ! A, ! B, ! C

Regeln:

& raw in → raw out

& no logic

& no correction

Station 02
RAW‑Input: ? X, ? Y, ? Z

RAW‑Output: ! X, ! Y, ! Z

Regeln:

& raw in → raw out

& no merge with station 01

& no interpretation

3. Operator
yziu-operator.item
Operator‑Mapping

RAW‑Flow

States:

&idle

&processing

&error

Flow:

? → &processing

&processing → !output

&error → !err

Testcases:

?A → !A

?B → !B

?0 → !0

?* → !*

4. Bench‑Plan
yziu-bench-plan.item
definiert Test‑Inputs

definiert erwartete Outputs

definiert RAW‑Regeln

keine Logik

keine Interpretation

RAW‑Version: raw-1

5. Zweck
YZIU dient zur:

Durchführung von RAW‑Bench‑Tests

Darstellung von RAW‑Input/Output

Prüfung von RAW‑Operator‑Verhalten

Ausführung unabhängiger Bench‑Stations

RAW‑Validierung ohne Logik

6. Status
YZIU ist ein:

RAW‑Bench‑System

UI‑Respo

Operator‑Respo

Stations‑Respo

Bench‑Plan‑Respo

Es ist nicht nur Material, sondern ein vollwertiges RAW‑Bench‑Framework.
