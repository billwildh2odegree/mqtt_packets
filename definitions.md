
# Transmission Type

Transmission type provides a verbal queue as to the reason that the device generated and sent a packet.

| transmission_type | Radio Type | Description |
|--|--|--|
| scheduled | All | Packet generated at its normal transmit interval |
| triggered | All | Generated by external stimulus - magnet, button , etc 
| alarm | LoRa | Packet is an alarm packet - flood, leak, etc|
| tamper | LoRa | Packet is a result of the device sensing possible unauthorized access to the device |
| announce | Zigbee | Device is announcing it presence to the the Zigbee network |
| power_up | Zigbee | Device has been powered up or rebooted  |
| command_response | Zigbee | Packet is a response to a commmnd - change transmit interval, change setpoint, etc |


# Payload Type

| payload_type | Radio Type | Description | Notes |
|--|--|--|--|
| commodity | All | Commodity data - gallons, kwh , pulses ||
| health_packet | Zigbee | Contains network information information about device performance | Not implemented |