```javascript 

 {
    "sensor_radio_type": "lora", 
    "sensor_data": {
        "transmit_attempt_count": 0, 
        "gallons": 17343.77, 
        "flow_time_minutes": 8360, 
        "battery_vdc_millivolts": 3586, 
        "flow_events": 7024
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
            "device_address": "45FB3041", 
            "gateway_count": 2, 
            "gateway_list": [
                {
                    "GatewayID": "0700B970", 
                    "GatewayRSSI": "-112.000000", 
                    "GatewaySNR": "2.500000", 
                    "GatewayESP": "-113.937759"
                }, 
                {
                    "GatewayID": "0700AB00", 
                    "GatewayRSSI": "-118.000000", 
                    "GatewaySNR": "-3.250000", 
                    "GatewayESP": "-122.932472"
                }
            ], 
            "raw_packet": "000043bfc61b7020a80e02", 
            "gateway_snr": 2.5, 
            "bridge_decoder": 75, 
            "frame_count_downlink": 912, 
            "spreading_factor": 7, 
            "lns_late_bit": 0, 
            "rssi": -112.0, 
            "decoder_type": "Unknown", 
            "message_type": 2, 
            "port": 212, 
            "channel": 2, 
            "frame_count_uplink": 3990
        }, 
        "common": {
            "gateway_timestamp": "2023-10-30T18:36:38.411Z", 
            "payload_type": "commodity", 
            "device_type": "aqura_water", 
            "serial_number": "001DB9DE00003D6B", 
            "firmware_version": "0.07", 
            "gateway_hostname": "020200000700B970"
        }
    }, 
    "generating_process_id": "mqtt-lora-bridge-split_3d5"
} 

```