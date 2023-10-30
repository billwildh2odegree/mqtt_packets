```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 19368, 
        "pulse_count_raw": 1, 
        "battery_vdc_millivolts": 3630
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
            "device_address": "45A8626C", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "070023BE", 
                    "GatewayRSSI": "-81.000000", 
                    "GatewaySNR": "7.750000", 
                    "GatewayESP": "-81.673981"
                }
            ], 
            "raw_packet": "00002d5100000001a34ba8", 
            "gateway_snr": 7.75, 
            "bridge_decoder": 73, 
            "frame_count_downlink": 2088, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -81.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 140, 
            "channel": 6, 
            "frame_count_uplink": 19368
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:36:38.127Z", 
            "payload_type": "commodity", 
            "device_type": "pulse_meter", 
            "serial_number": "0004A30B00F7D43A-2", 
            "firmware_version": "7.05", 
            "gateway_hostname": "02020000070023BE"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```