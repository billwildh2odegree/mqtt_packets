```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 2683, 
        "pulse_count_raw": 2, 
        "battery_vdc_millivolts": 3590
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
    "packet_creation_timestamp": 1698690817, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "44FEB09B", 
            "gateway_count": 2, 
            "gateway_list": [
                {
                    "GatewayID": "07009FAE", 
                    "GatewayRSSI": "-96.000000", 
                    "GatewaySNR": "8.000000", 
                    "GatewayESP": "-96.638924"
                }, 
                {
                    "GatewayID": "0700A0E6", 
                    "GatewayRSSI": "-79.000000", 
                    "GatewaySNR": "7.500000", 
                    "GatewayESP": "-79.710815"
                }
            ], 
            "raw_packet": "00006ed8000000029f0a7b", 
            "gateway_snr": 8.0, 
            "bridge_decoder": 78, 
            "frame_count_downlink": 281, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -96.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 140, 
            "channel": 5, 
            "frame_count_uplink": 2686
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:33:37.428Z", 
            "payload_type": "commodity", 
            "device_type": "pulse_meter", 
            "serial_number": "0004A30B00F718A3-2", 
            "firmware_version": "7.07", 
            "gateway_hostname": "0202000007009FAE"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```