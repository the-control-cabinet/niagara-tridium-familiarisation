# 02 · Lab Plan

[← Back to README](../README.md)

Each lab records: **steps**, **evidence** (screenshots, exported station fragments, point lists) and **pass criteria**.

| # | Lab | Steps | Pass criteria |
|---|---|---|---|
| 1 | Station and Workbench | Create a station; users and roles; backup and restore | Station runs; a restored backup matches |
| 2 | BACnet/IP | Add a BACnet network; discover YABE's room simulator, then the plant-points server; add points with units; subscribe COV | Values match YABE and HA; COV updates arrive; stale data shows as fault |
| 3 | Trend | Trend driver to the IQ411; discover its points | IQ411 I/O and strategy values readable; point-to-point record cross-checked |
| 4 | Modbus TCP | Modbus network to the ESP32 register map; scaling and status bits | Values and units match the register map document |
| 5 | Tags and histories | Tag the points (site/equip/point); add history extensions; trend charts | A 24 h trend of the plant points; tags searchable |
| 6 | Alarms | Alarm classes P1-P4 from the alarm strategy; limits, delays, deadbands; routing and acknowledgement | Test alarm raised, routed, acknowledged and cleared |
| 7 | Schedules | Weekly and exception schedules on simulator and rig points | Schedule drives the simulator setpoint at the switchpoint |
| 8 | Px graphics | Plant-room page with live values and alarm states | Page mirrors the HA plant-room graphic |
| 9 | S7 (optional) | S7 driver to an S7-1200 (PUT/GET enabled, non-optimised data blocks) | PLC tags readable |

**Safety:** reads only against the live house systems; writes only to the simulators and the training rig.
