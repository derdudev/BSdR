# Dokumentation

## Blöcke

| Block                 | Paremeter                                                    | Erklärung                                                    |
| --------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `lineNotice`          | `speed`: Geschwindigkeit [0-100]<br />`direction`: Richtung [-1: rückwärts oder 1: vorwärts]<br />`kp`: Konstante für Proportional [default: 3.5]<br />`ki`: Konstante für Proportional [default: 0]<br />`kd`: Konstante für Differential [default: 0]<br /> | Folgt über den mittleren Farbsensor einer Linie, bis der äußere Farbsensor eine schwarze Linie erkennt |
| `gyroStraightToLine`  | `kd`: Konstante für Proportional [default: 1.6 oder -2]<br />`target`: Zielwert für den Gyrosensor [default: 0]<br />`v`: Geschwindigkeit [0-100]<br />`dir`: Richtung [-1 oder 1] | Mithilfe des Gyrosensors gerade nach vorne/hinten fahren, bis der mittlere (!) Farbsensor (auf Port 4) eine Linie erkennt |
| `gyroStraightTimeV`   |                                                              |                                                              |
| `pidGyroStraight`     | `kp`: Proportionalskonstante <br />`kd`: Differenzialkonstante<br />`target`: Zielwert | Fährt solange nach vorne, bis Lichtsensor an Port 4 einen Wert kleiner als 8 misst.<br />Funktioniert auf Basis eines PID-Reglers, daher auch der Name.<br />Allerdings sind in Verwendung `kd` und `ki` oft einfach gleich null gesetzt, da das Finden eines passenden Wertes oft astronomisch schwer ist. |
| `pidGyroStraightTime` | `kp`: Proportionalitätskonstante<br /> `target`: "Gradlinie", auf welcher gefahren wird, default = 0<br />`t`: Zeit, die gefahren werden soll<br />`dir`: Richtung [1; -1] |                                                              |
| `alignToAngle`        | `a`: Winkel [0 - 360]<br />`v`: Geschwindigkeit [0 - 100]    | Ausrichtungsprogramm: Richtet sich nach dem übergebenen Winkel `a` aus |
| `alignToZeronew`      | -                                                            | Ausrichtungsprogramm: Zuvor muss ein Nullwinkel (`angleZero`) festgelegt worden sein, zu dem dann auf die optimalste Weise zurück gekehrt wird. |
| `fahre bis linie`     | -                                                            | Fährt solange nach vorne                                     |
| `turnGyro`            | `degrees`: Zu drehende Grad, ausgehend vom Nullpunkt<br />`v`: Drehgeschwindigkeit |                                                              |
| `proportional`        | `speed`:<br />`direction`:<br />`duration`:                  |                                                              |

