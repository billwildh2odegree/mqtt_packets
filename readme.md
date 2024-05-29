


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
        "location_information_found": 1,  
        "property_name": "Daves Apartments",  
        "building_name": "1",  
        "apartment_name": "101",  
        "property_id": 345,  
        "building_id": 342342,  
        "apartment_id": 2342342,  
        "device_unique_id": 97856,  
        "repair_flag": 0,  
        "repair_flag_reason": "",  
        "bedroom_count": 1,  
        "bathroom_count": 2,  
        "meter_type": "matster",  
        "attached_to": "boiler"  
    }  
```

Thermostats have a limited amount of data that is able to be sent in its commodity packet. Some changes
will not be reflected in the main commodity packet and will be included in a command_response packet so if 
a setting is changed or queried in a thermostat the device will respond in one of two ways. 

1. It will respond with its commodity packet format marked as commodity_packet which will include the updated value.
2. It will respond with the commodity packet format marked as command_response

If the [payload_type](definitions.md#payload-type) is command_response there will be no usable sensor_data ; it will be "none":"none" .
If the [payload_type](definitions.md#payload-type) it commodity_data there will be no usable command_reponse data ; ; it will be "none":"none" .

Below is an empty payload response. Packets that may contain relevant data here will have the elements defined in the 
packet examples 

```javascript         
    "command_response": [
        { "none": {
                "none": "none"
            }}
    ],
```
Below is a populated payload response.

```javascript

{
    "command_response": [
        {
            "get_zone_settings": {
                "window_closed_zone_1_hour_24hr": 10,
                "window_closed_zone_1_minute": 0,
                "window_closed_zone_1_set_point_c": 20,
                "window_closed_zone_1_set_limit_c": 22,
                "window_closed_zone_2_hour_24hr": 23,
                "window_closed_zone_2_minute": 0,
                "window_closed_zone_2_set_point_c": 20,
                "window_closed_zone_2_set_limit_c": 22,
                "window_open_zone_1_hour_24hr": 10,
                "window_open_zone_1_minute": 0,
                "window_open_zone_1_set_point_c": 20,
                "window_open_zone_1_set_limit_c": 22,
                "window_open_zone_2_hour_24hr": 23,
                "window_open_zone_2_minute": 0,
                "window_open_zone_2_set_point_c": 20,
                "window_open_zone_2_set_limit_c": 22,
                "summer_month": 6,
                "summer_day": 1,
                "winter_month": 10,
                "winter_day": 1,
                "config_byte_decimal": 188,
                "config_byte_binary": "10111100",
                "window": "closed",
                "time_zone": 1,
                "override": "heat",
                "season": "winter",
                "window_sensor_led": "enabled",
                "auto_season_changeover": "enabled",
                "auto_multicast_scaling": "disabled"
            }
        },
        {
            "set_zone_settings": {
                "window_closed_zone_1_hour_24hr": 10,
                "window_closed_zone_1_minute": 0,
                "window_closed_zone_1_set_point_c": 20,
                "window_closed_zone_1_set_limit_c": 22,
                "window_closed_zone_2_hour_24hr": 23,
                "window_closed_zone_2_minute": 0,
                "window_closed_zone_2_set_point_c": 20,
                "window_closed_zone_2_set_limit_c": 22,
                "window_open_zone_1_hour_24hr": 10,
                "window_open_zone_1_minute": 0,
                "window_open_zone_1_set_point_c": 20,
                "window_open_zone_1_set_limit_c": 22,
                "window_open_zone_2_hour_24hr": 23,
                "window_open_zone_2_minute": 0,
                "window_open_zone_2_set_point_c": 20,
                "window_open_zone_2_set_limit_c": 22,
                "summer_month": 6,
                "summer_day": 1,
                "winter_month": 10,
                "winter_day": 1,
                "config_byte_decimal": 188,
                "config_byte_binary": "10111100",
                "window": "closed",
                "time_zone": 1,
                "override": "heat",
                "season": "winter",
                "window_sensor_led": "enabled",
                "auto_season_changeover": "enabled",
                "auto_multicast_scaling": "disabled"
            }
        }
    ]


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
	"command_response": [
        	{
            	"none": {
                	"none": "none"
            	}
        	}
    	],
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
	"command_response": [
        	{
            	"none": {
                	"none": "none"
            	}
        	}
    	],
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

[axioma_ultrasonic](samples_240524/axioma_ultrasonic.md)  

Encoded Water Meters

[eleven_x_encoded](samples_240524/eleven_x_encoded.md)  

QMC Water Meters

[gwf_water_meter](samples_240524/gwf_water_meters.md)  

Single Jet Digital Face Water Meters

[h2o_eregister_water_meter](samples_240524/h2o_eregister_water_meter.md)  

Aqura Water Meters

[aqura_water](samples_240524/aqura_water.md)  

Pulse Counters / Meters

[pulse_meter](samples_240524/pulse_meter.md)  

Flood Detection and Prevention

[dual_channel_water_sensor](samples_240524/dual_channel_water_sensor.md)  
[rope_water_sensor](samples_240524/rope_water_sensor.md)  
[strega_shut_off_valve](samples_240524/strega_shut_off_valve.md)  


Environment Monitoring

[temperature_humidity_sensor](samples_240524/temperature_humidity_sensor.md)  

Electric Meters

[dragino_satec_kwh](samples_240524/dragino_satec_kwh.md)  
[vision_socket](samples_240524/vision_socket.md)  
[accuenergy_modbus](samples_240524/accuenergy_modbus.md)  
[ekm_rs485](samples_240524/ekm_rs485.md)  


BTU

[btu_commodity](samples_240524/btu_commodity.md)  
[btu_diagnostic](samples_240524/btu_diagnostic.md)  

Baseboard Heat Relay Controllers

[mini](samples_240524/mini.md)  
[mini_high_load](samples_240524/mini_high_load.md)  

Thermostats

[thermostat](samples_240524/thermostat.md)  

Zigbee Infrastructure

[coordinator](samples_240524/coordinator.md)  
[router](samples_240524/router.md)  

Gateways

[vision_datagate](samples_240524/vision_datagate.md)  
[zigbee_gateway](samples_240524/zigbee_gateway.md)   


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

                


