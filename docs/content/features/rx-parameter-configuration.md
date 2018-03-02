---
title: RX parameter (re)configuration
menu:
    main:
        parent: features
        weight: 1
---

## RX parameter (re)configuration

LoRa Server supports the (re)configuration of the following RX parameters:

* **RX1 data-rate offset** the offset used to calculate the RX1 data-rate,
  based on the uplink data-rate.
* **RX2 data-rate** the data-rate used for the RX2 receive-window.
* **RX2 frequency** the frequency used for the RX2 receive-window.

The first parameters are sent to the device as part of the OTAA join-accept
frame. The third parameter is pushed to the device using the `RXParamSetupReq`
mac-command.

**Note:** on a LoRa Server configuration change, the new parameters will be
pushed to the device using the `RXParamSetupReq` mac-command at the first
opportunity.