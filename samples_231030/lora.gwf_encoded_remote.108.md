```javascript 

{
    "packet_creation_timestamp": 1701443929,
    "sensor_radio_type": "lora",
    "generating_process_id": "bridge_truety_1701443929",
    "transmission_type": "scheduled",
    "header": {
        "common": {
            "serial_number": "70B3D53878000342",
            "device_type": "gwf_encoded_remote",
            "payload_type": "commodity",
            "gateway_timestamp": "2023-11-17T00:00:00Z",
            "gateway_hostname": "0203000000000059",
            "firmware_version": "0.0"
        },
        "lora": {
            "port": 1,
            "bridge_decoder": 108,
            "channel": 1,
            "lns_late_bit": 0,
            "device_address": "42424242",
            "rssi": -42,
            "gateway_snr": 0,
            "spreading_factor": 7,
            "decoder_type": "Unknown",
            "message_type": 42,
            "frame_count_uplink": 11,
            "frame_count_downlink": 42,
            "sub_band": "G0",
            "gateway_count": 1,
            "gateway_list": [
                {
                    "GatewayID": "42424242",
                    "GatewayRSSI": "-42",
                    "GatewaySNR": "0",
                    "GatewayESP": "-42.42"
                }
            ],
            "raw_packet": ""
        }
    },
    "sensor_data": {
        "gallons": 46.8,
        "utility": "hot water",
        "meter_sn": 231842,
        "interval_length": 60
    },
    "location_information": {
        "location_information_found": 0,
        "property_name": "",
        "building_name": "",
        "apartment_name": "",
        "property_id": 0,
        "building_id": 0,
        "apartment_id": 0,
        "device_unique_id": 0,
        "repair_flag": 0,
        "repair_flag_reason": "",
        "bedroom_count": 0,
        "bathroom_count": 0,
        "meter_type": "",
        "attached_to": ""
    }
}
```