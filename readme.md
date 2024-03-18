


# Element Definitions 

[transmission_type](definitions.md#transmission-type)   
[payload_type](definitions.md#payload-type)   

# Elements common to all packets:

```javascript   

    "packet_creation_timestamp": 1674755744,  
    "sensor_radio_type": "lora",  
    "generating_process_id": "mqtt-lora-bridge-split_92d",  
    "transmission-type": "scheduled",
```

```javascript 
    "header": {  
        "common": {  
            "serial_number": "343531314F377510",  
            "device_type": "aqura_water",  
            "payload-type": "commodity",  
            "gateway_timestamp": "2023-01-26T17:55:48.904Z",  
            "gateway_hostname": "02020000070024F4",  
            "firmware_version": "0.02"  
        }  
    }
```

The location information data that is provided in the customer cached data feed is   
more extensive than the main data plane packets. See the [Customer Cache](#customer-cache) section.

```javascript         
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
```

Thermostats have a limited amount of data that is able to be sent in its commodity packet. Some changes
will not be reflected in the main commodity packet and will be included in a command_response packet so if 
a setting is changed or queried in a thermostat the device will respond in one of two ways. 
	1. It will respond with its commodity packet format marked as commodity_packet which will include the updated value.
 	2. It will respond with the commodity packet format marked as command_response

```javascript         
    "command_response": {  
        "none":"none"
    }  
```



Sensor data will vary by device. The [Sample Packets By Device Type](#sample-packets-by-device-type) shows detailed commodity information and complete packets for each device. 

```javascript
 "sensor_data": {  },
```
    
# Complete LoRa Packet  


```javascript 
    {  
        "packet_creation_timestamp": 1674755744,  
        "sensor_radio_type": "lora",  
        "generating_process_id": "mqtt-lora-bridge-split_92d",  
        "transmission_type": "scheduled",  
        "header": {  
            "common": {  
                "serial_number": "343531314F377510",  
                "device_type": "aqura_water",  
                "payload_type": "commodity",  
                "gateway_timestamp": "2023-01-26T17:55:48.904Z",  
                "gateway_hostname": "02020000070024F4",  
                "firmware_version": "0.02"  
            },  
            "lora": {  
                "port": 210,  
                "bridge_decoder": 75,  
                "channel": 1,  
                "device_address": "45180AC3",  
                "rssi": -95,  
                "lns_late_bit" : 0,    
                "gateway_snr": 8.5,  
                "spreading_factor": 7,  
                "decoder_type": "Unknown",  
                "message_type": 2,  
                "frame_count_uplink": 16499,  
                "frame_count_downlink": 3491,  
                "sub_band": "G0",  
                "gateway_count": 1,  
                "gateway_list": [  
                    {  
                        "GatewayID": "070024F4",  
                        "GatewayRSSI": "-95.000000",  
                        "GatewaySNR": "8.500000",  
                        "GatewayESP": "-95.573822"  
                    }  
                ],  
                "raw_packet": "000056c1ef318c1b4c4076"  
            }  
        },  
        "sensor_data": {  
            "battery_vdc_millivolts": 3672,  
            "gallons": 22209.93,  
            "flow_events": 12684,  
            "flow_time_minutes": 6988,  
            "transmit_attempt_count": 16502  
        },
	 "command_response": {  
	        "none":"none"
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

# Complete Zigbee Packet

```javascript 

    {  
        "packet_creation_timestamp": 1679669881,  
        "sensor_radio_type": "zigbee",  
        "generating_process_id": "mqtt-lora-bridge-split_92d",  
        "transmission-type": "scheduled",  
        "header": {  
            "common": {  
                "serial_number": "000D6F000351227D",  
                "device_type": "router",  
                "payload_type": "commodity",  
                "gateway_timestamp": "2023-03-24 10:57:52",  
                "gateway_hostname": "channelwood_dup",  
                "firmware_version": "02.08"  
            },  
            "zigbee": {  
                "major_version": "02",  
                "minor_version": "08",  
                "parent_eui": "000D6F0003512299",  
                "channel": "14",  
                "delivery_fail": 10,  
                "reset_count": 133,  
                "data_interval": 1823,  
                "app_loop_timer": 1,  
                "ember_reset_code": 4,   
                "app_reset_code": 0,  
                "device_transmit_count": 170805,  
                "diagnostic": 0,  
                "battery": 0,  
                "radio_power": 255,  
                "crc": "91CC",  
                "gateway_counter": 45975,  
                "short_id": "5C37",  
                "unit_code": 100,  
                "com_hub_index": 718799973,
                "root_packet": "yes", 
                "raw_packet":   "&0208000D6F00......29914FFFF*",  
                "decoded_packet_strings": {  
                        "payload_index_1": "02",  
                        "payload_index_2": "08",  
                        "payload_index_3": "000D6F000351227D",  
                        "payload_index_4": "000D6F0003512299",  
                        "payload_index_5": "14",  
                        "payload_index_6": "170805",  
                        "payload_index_7": "133",  
                        "payload_index_8": "10",  
                        "payload_index_9": "1",  
                        "payload_index_10": "1823",  
                        "payload_index_11": "4",  
                        "payload_index_12": "0",  
                        "payload_index_13": "0",  
                        "payload_index_14": "0",  
                        "payload_index_15": "255",  
                        "payload_index_16": "100",  
                        "payload_index_17": "91CC",  
                        "payload_index_18": "45975",  
                        "payload_index_19": "5C37",  
                        "payload_index_20": "2023-03-24 10:57:52",  
                        "payload_index_21": "5C37",  
                        "payload_index_22": "4",  
                        "payload_index_23": "A4BD",  
                        "payload_index_24": "0",  
                        "payload_index_25": "11",  
                        "payload_index_26": "0",  
                        "payload_index_27": "0",  
                        "payload_index_28": "0",  
                        "payload_index_29": "0",  
                        "payload_index_30": "0",  
                        "payload_index_31": "0",  
                        "payload_index_32": "0",  
                        "payload_index_33": "0",  
                        "payload_index_34": "0",  
                        "payload_index_35": "0",   
                        "payload_index_36": "0",  
                        "payload_index_37": "0",  
                        "payload_index_38": "0",  
                        "payload_index_39": "0",  
                        "payload_index_40": "0",  
                        "payload_index_41": "0",  
                        "payload_index_42": "0",  
                        "payload_index_43": "0",  
                        "payload_index_44": "0",  
                        "payload_index_45": "0"  
                    }  
            }  
        },  
        "sensor_data": {  
            "neighbors": 11,  
            "children": 0  
        },
	"command_response": {  
	        "none":"none"
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

# Sample Packets By Device Type


Ultrasonic Water Meters

[lora.axioma_ultrasonic.96](samples_231030/lora.axioma_ultrasonic.96.md)  

Encoded Water Meters

[lora.eleven_x_encoded.84](samples_231030/lora.eleven_x_encoded.84.md)  
[lora.gwf_encoded_integrated.106](samples_231030/lora.gwf_encoded_integrated.106.md)  
[lora.gwf_encoded_remote.107](samples_231030/lora.gwf_encoded_remote.107.md)  
[lora.gwf_encoded_remote.108](samples_231030/lora.gwf_encoded_remote.108.md)  


Aqura Water Meters

[lora.aqura_water.75](samples_231030/lora.aqura_water.75.md)  
[zigbee.aqura_water.36](samples_231030/zigbee.aqura_water.36.md)  
[zigbee.aqura_water.40](samples_231030/zigbee.aqura_water.40.md)  
[zigbee.aqura_water.42](samples_231030/zigbee.aqura_water.42.md)  
[zigbee.aqura_water_one_inch.190](samples_231030/zigbee.aqura_water_one_inch.190.md)  

Pulse Counters / Meters

[lora.pulse_meter.104](samples_231030/lora.pulse_meter.104.md)  
[lora.pulse_meter.46](samples_231030/lora.pulse_meter.46.md)  
[lora.pulse_meter.73](samples_231030/lora.pulse_meter.73.md)  
[lora.pulse_meter.78](samples_231030/lora.pulse_meter.78.md)  
[lora.pulse_meter.81](samples_231030/lora.pulse_meter.81.md)  
[zigbee.pulse_counter.126](samples_231030/zigbee.pulse_counter.126.md)  
[zigbee.pulse_counter.140](samples_231030/zigbee.pulse_counter.140.md)  


Flood Detection and Prevention

[lora.dual_channel_water_sensor.79](samples_231030/lora.dual_channel_water_sensor.79.md)  
[lora.rope_water_sensor.82](samples_231030/lora.rope_water_sensor.82.md)  
[lora.strega_shut_off_valve.80](samples_231030/lora.strega_shut_off_valve.80.md)  


Environment Monitoring

[lora.temperature_humidity_sensor.60](samples_231030/lora.temperature_humidity_sensor.60.md)  
[lora.temperature_humidity_sensor.64](samples_231030/lora.temperature_humidity_sensor.64.md)  
[zigbee.temperature_humidity_sensor.155](samples_231030/zigbee.temperature_humidity_sensor.155.md)  


Electric Meters

[lora.dragino_satec_kwh.102](samples_231030/lora.dragino_satec_kwh.102.md)  
[lora.vision_socket_12s.76](samples_231030/lora.vision_socket_12s.76.md)  
[zigbee.electric.187](samples_231030/zigbee.electric.187.md)  
[zigbee.accuenergy_modbus.192](samples_231030/zigbee.accuenergy_modbus.192.md)  
[zigbee.ekm_rs485.166](samples_231030/zigbee.ekm_rs485.166.md)  



BTU

[zigbee.btu_commodity.173](samples_231030/zigbee.btu_commodity.173.md)  
[zigbee.btu_diagnostic.174](samples_231030/zigbee.btu_diagnostic.174.md)  

Baseboard Heat Realay Controllers

[zigbee.mini.176](samples_231030/zigbee.mini.176.md)  
[zigbee.mini_high_load.188](samples_231030/zigbee.mini_high_load.188.md)  

Thermostats

[zigbee.thermostat.129](samples_231030/zigbee.thermostat.129.md)  
[zigbee.thermostat.171](samples_231030/zigbee.thermostat.171.md)  
[zigbee.thermostat.179](samples_231030/zigbee.thermostat.179.md)  
[zigbee.thermostat.182](samples_231030/zigbee.thermostat.182.md)  


Zigbee Infrastructure

[zigbee.coordinator.105](samples_231030/zigbee.coordinator.105.md)  
[zigbee.router.100](samples_231030/zigbee.router.100.md)  

Gateways

[zigbee.vision_datagate.253](samples_231030/zigbee.vision_datagate.253.md)  
[zigbee.zigbee_gateway.254](samples_231030/zigbee.zigbee_gateway.254.md)   

No Payload Defined - Legacy Devices

[zigbee.not_identified.119](samples_231030/zigbee.not_identified.119.md)  
[zigbee.not_identified.120](samples_231030/zigbee.not_identified.120.md)  
[zigbee.not_identified.123](samples_231030/zigbee.not_identified.123.md)  
[zigbee.not_identified.124](samples_231030/zigbee.not_identified.124.md)  
[zigbee.not_identified.125](samples_231030/zigbee.not_identified.125.md)  
[zigbee.not_identified.151](samples_231030/zigbee.not_identified.151.md)  
[zigbee.not_identified.181](samples_231030/zigbee.not_identified.181.md)  
[zigbee.not_identified.183](samples_231030/zigbee.not_identified.183.md)  
[zigbee.not_identified.189](samples_231030/zigbee.not_identified.189.md)  



# Customer Cache

## Location Information 

The location information data that is provided in the customer cached data feed is   
more extensive than the main data plane packets. 

```javascript

"location_information": {
		"unit_code": 42,
		"group_name": "",
		"meter_status": 1,
		"apartment_name": "5205",
		"property_name": "Dry Mesa Apartments",
		"building_name": "A07",
		"device_unique_id": 153845,
		"bathroom_count": 2.0,
		"gid_set_flag": "0",
		"audit_log_id": 0,
		"gid": "3F4A",
		"meter_type": "submeter",
		"location": "Toilet",
		"apartment_id": 147274,
		"factor": 1.0,
		"building_id": 12438,
		"location_information_found": 1,
		"device_part_number": "L54120+",
		"update_note": "update_note",
		"device_serial_number": "001DB9DE00000E65",
		"gid_set_date": "Jan  1 1900 12:00AM",
		"bedroom_count": 3.0,
		"property_id": 1642,
		"location_type": "apartment",
		"attached_to": "2nd Bath Toilet",
		"qr_index": 75,
		"building_or_floor": "building"
	},

```



## Misc Notes

In Zigbee packets the raw_packet and decoded_packet_strings will be empty.

## Unique Elements

packet_cache_id - primary key of the table where the cache is being pulled from. Sequential and time ordered  
packet_cache_limit - current maximum number of packets per cycle that will be pulled from the cache and delivered  
packet_cache_load - number of packets pulled this cycle   
packet_cache_interval - frequency that the process requsts new data from the cache. this will change based on load  

location_information->group_name - internal to H2O . Should be blank

                


