# Speedometer

This project consists of two GUI applications working together to create a user interactable speedometer. These applications form a client and server pair.

The server application's GUI consist of:
- Three sliders controlling
  - Speed
  - Temperature
  - Battery level

- Three checkboxes to toggle:
  - Indicator left and right
  - Warning lights

The client application's GUI consist of:
- A central speedometer gauge
- Indicator lights
- Temperature indicator
- Battery level indicator
- Connection indicator

The two applications can communicate using either a local TCP/IP connection or BLE via two microcontrollers connected to a PC via UART. The protocol is chosen by the user when generating the program through CMAKE. All communication protocols are derived off of a generic communication service class that letting the rest of the program go unchanged when switching between protocols.

The client GUI will inform the user of connection issues between the two applications by turning on the connection indicator symbol, and the server application will print an error message to the terminal. The applications are able to reconnect to one another automatically if this occurs.

This project was made as a school group assignment lasting for 4 weeks earlier this year. We were a total of 5 people working on this project during this period.
