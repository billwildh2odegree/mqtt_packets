```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "temperature_valid": "yes", 
        "temperature_c": 24.1, 
        "temperature_f": 75.38, 
        "humidity_valid": "yes", 
        "humidity": 58
    }, 
    "location_information": {
        "property_name": "", 
        "attached_to": "", 
        "device_unique_id": 0, 
        "apartment_id": 0, 
        "bathroom_count": 0, 
        "repair_flag_reason": "", 
        "repair_flag": 0, 
        "meter_type": "", 
        "location_information_found": 0, 
        "apartment_name": "", 
        "bedroom_count": 0, 
        "building_id": 0, 
        "property_id": 0, 
        "building_name": ""
    }, 
    "transmission_type": "scheduled", 
    "packet_creation_timestamp": 1698690998, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "44C1335A", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07001C39", 
                    "GatewayRSSI": "-64.000000", 
                    "GatewaySNR": "10.500000", 
                    "GatewayESP": "-64.370781"
                }
            ], 
            "raw_packet": "036700f104687400ff012e", 
            "gateway_snr": 10.5, 
            "bridge_decoder": 64, 
            "frame_count_downlink": 34, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -64.0, 
            "decoder_type": "", 
            "message_type": 2, 
            "port": 10, 
            "channel": 5, 
            "frame_count_uplink": 348
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:36:38.156Z", 
            "payload_type": "commodity", 
            "device_type": "temperature_humidity_sensor", 
            "serial_number": "647FDA0000003AD8", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007001C39"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```