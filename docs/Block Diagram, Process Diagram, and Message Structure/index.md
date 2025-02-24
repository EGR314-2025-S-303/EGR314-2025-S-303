
## **Block Diagram**
The team’s block diagram outlines the flow of communication and functionality across different components in the system. Cade, utilizing an ESP32 microchip, serves as the central hub for bidirectional communication with the other team members, who use PIC microcontrollers. Data flows sequentially from Cade to Tyler, who manages sensor integration, then to Dan, who controls the actuator, and finally to Jahmel, responsible for the Human-Machine Interface (HMI), before looping back to Cade. The boards communicate via UART, ensuring reliable data transmission between each module. Additionally, the sensor and actuator exchange data through either SPI or I2C protocols, enabling efficient and precise control of the system’s operation.

<img src="Team-Block-Diagram.png">

## **Sequence Diagram**

The sequence diagram illustrates the communication flow between users and system components, ensuring synchronized operation. When a Web User requests to turn on LED1, the command is passed sequentially from Cade to Tyler, then to Dan, and finally to Jahmel, who activates the LED and discards the processed message. Similarly, when an In-Person User sets the motor speed, the request travels from Jahmel to Cade, through Tyler, and then to Dan, who executes the command before discarding the message. Additionally, sensor data is transmitted in a continuous 1-second loop, where Tyler sends data to Dan, who forwards it to Jahmel. Jahmel provides real-time feedback to the In-Person User while also relaying the data to Cade, who then updates the Web User before discarding the received data. This structured communication ensures efficient data flow and command execution throughout the system.

``` mermaid
sequenceDiagram
    actor Web User
    Web User-->>+Cade: Turn on LED1
    Cade->>+Tyler: Turn on LED1
    Tyler->>+Dan: Turn on LED1
    Dan->>+Jahmel: Turn on LED1
    Jahmel->>-Jahmel: LED1 ON, Trash Message
    actor In Person User
    In Person User-->>+Jahmel: Set Motor Speed
    Jahmel->>+Cade: Set Motor Speed
    Cade->>+Tyler: Set Motor Speed
    Tyler->>+Dan: Set Motor Speed
    Dan->>-Dan: Set Motor Speed Trash
    loop Every 1 second
    Tyler->>+Dan: Sensor Data
    Dan->>+Jahmel: Sensor Data
    Jahmel-->>+In Person User: Sensor Data
    Jahmel->>+Cade: Sensor Data
    Cade-->>+Web User: Sensor Data
    Cade->>-Cade: Sensor Data Trash
    end
```

