[Portapilas 4x Li-Ion 18650] ---> (Módulo Regulador MP1584) ---> [Alimentación del Sistema]

                                      [Módulo Bluetooth HC-05]
                                                 |
                                                 v
                                    (Level Shifter 3.3V a 5V)
                                                 |
                                                 v
   [Sensor de Color (TCS3200)]   ----> +-----------------------+
   [Sensor de Línea (Pololu)]    ----> |                       |
   [Sensor de Obstáculos (FC-51)]----> |     Tarjeta FPGA      |
                                       |       (Cerebro)       |
                                       |                       |
                                       +-----------------------+
                                                 |
                                                 v
                                        [Kit de Chasis 2WD]
                                      (Tracción y Rueda Loca)
