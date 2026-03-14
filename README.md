graph LR
    subgraph Alimentacion [Alimentación y Potencia]
        BAT[4x Li-Ion 18650] --> REG[Regulador MP1584]
    end

    subgraph Perifericos [Sensores y Comunicación]
        BT[Bluetooth HC-05]
        S1[Color TCS3200]
        S2[Línea Pololu QTR-8RC]
        S3[Obstáculos FC-51]
    end

    subgraph Procesamiento [Lógica Central]
        LS[Level Shifter 3.3V a 5V]
        CEREBRO{Tarjeta FPGA}
    end

    subgraph Actuadores [Estructura]
        MOTORES[Kit Chasis 2WD]
    end

    %% Conexiones de energía
    REG --> |VCC 5V| LS
    REG -.-> |VCC| Perifericos

    %% Conexiones de datos (Lado 5V)
    BT <--> |Datos 5V| LS
    S1 --> |Señal 5V| LS
    S2 --> |Señal 5V| LS
    S3 --> |Señal 5V| LS

    %% Conexión protegida (Lado 3.3V)
    LS <--> |Datos 3.3V| CEREBRO

    %% Control de motores
    CEREBRO --> |PWM / Dirección| MOTORES
