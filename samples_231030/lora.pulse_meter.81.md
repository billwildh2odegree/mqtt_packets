```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 12032, 
        "pulse_count_raw": 1, 
        "battery_vdc_millivolts": 3550
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
    "packet_creation_timestamp": 1698690834, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "446C90E8", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "070024F8", 
                    "GatewayRSSI": "-102.000000", 
                    "GatewaySNR": "9.000000", 
                    "GatewayESP": "-102.514969"
                }
            ], 
            "raw_packet": "0000003b000000019b2f00", 
            "gateway_snr": 9.0, 
            "bridge_decoder": 81, 
            "frame_count_downlink": 1327, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -102.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 140, 
            "channel": 3, 
            "frame_count_uplink": 12033
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:33:53.738Z", 
            "payload_type": "commodity", 
            "device_type": "pulse_meter", 
            "serial_number": "0004A30B00F9C9F8-2", 
            "firmware_version": "7.07", 
            "gateway_hostname": "02020000070024F8"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```