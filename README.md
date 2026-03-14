+-----------------------------------------------------------+
|                 SISTEMA DE ALIMENTACIÓN                   |
|                                                           |
|   [ 4x Li-Ion 18650 ] -----> [ Reg. MP1584 ]              |
+------------------------------------+----------------------+
                                     | 5V VCC
                                     v
+-------------------+    +-----------------------+    +-------------------+
|     SENSORES      |    |       INTERFAZ        |    |      CONTROL      |
|                   |    |                       |    |                   |
| * Color TCS3200   |--->|     LEVEL SHIFTER     |<---| * Módulo HC-05    |
| * Línea Pololu    |--->|      (3.3V a 5V)      |    |   (Bluetooth)     |
| * Obstáculo FC-51 |--->|                       |    +-------------------+
+-------------------+    +-----------+-----------+
                                     | 3.3V (Señales Seguras)
                                     v
                         +-----------------------+
                         |        CEREBRO        |
                         |                       |
                         |     TARJETA FPGA      |
                         | (Procesam. Central)   |
                         +-----------+-----------+
                                     | Control (PWM/Dir)
                                     v
                         +-----------------------+
                         |      ESTRUCTURA       |
                         |                       |
                         |    KIT CHASIS 2WD     |
                         |  (Tracción / Ruedas)  |
                         +-----------------------+
