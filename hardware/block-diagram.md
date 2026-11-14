# Functional Block Diagram

```mermaid
flowchart TB
    P[Regulated 5 V USB charger] --> R[Relay contact switches USB +5 V]
    R --> M[Mobile phone]
    T[Digital timer relay module] -->|Relay output| R
    S[Trigger switch] -->|Trigger input| T
    U[Preset time interval] --> T
    T --> L[LED status circuit]
    T --> B[Active buzzer]
```

This diagram shows functional relationships only. It does not specify terminal numbers, grounds, resistor values, or the exact relay contact selection. Those require the actual module model and verified wiring.
