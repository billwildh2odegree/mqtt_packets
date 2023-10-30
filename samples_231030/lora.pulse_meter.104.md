```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 0, 
        "pulse_count_raw": 16638, 
        "battery_vdc_millivolts": 0
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
    "packet_creation_timestamp": 1698690588, 
    "header": {
        "lora": {
            "sub_band": "G0", 
            "device_address": "45FDC10E", 
            "gateway_count": 1, 
            "gateway_list": [
                {
                    "GatewayID": "07001C39", 
                    "GatewayRSSI": "-35.000000", 
                    "GatewaySNR": "9.500000", 
                    "GatewayESP": "-35.461838"
                }
            ], 
            "raw_packet": "010081210040fe653ff61b", 
            "gateway_snr": 9.5, 
            "bridge_decoder": 104, 
            "frame_count_downlink": 39, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -35.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 7, 
            "channel": 1, 
            "frame_count_uplink": 118
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:29:47.901Z", 
            "payload_type": "commodity", 
            "device_type": "pulse_meter", 
            "serial_number": "A84041818188C8AE-2", 
            "firmware_version": "0.0", 
            "gateway_hostname": "0202000007001C39"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```