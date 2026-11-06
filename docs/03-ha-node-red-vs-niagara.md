# 03 · The Same Supervisory Jobs: HA + Node-RED vs Niagara

[← Back to README](../README.md)

To complete after the labs. The framework:

| Job | HA + Node-RED (this portfolio) | Niagara 4 | Notes to capture |
|---|---|---|---|
| Device integration | Integrations (RAMSES-II, ESPHome, MQTT, BACnet via HACS) | Drivers (BACnet, Trend, Modbus, S7) | Discovery, point creation, effort |
| Point metadata | Device classes, units, areas, labels | Facets, tags | How searchable and reusable |
| Histories | Recorder + long-term statistics | History extensions, history service | Retention, export |
| Alarms | Automations + notifications ([alarm strategy](https://github.com/the-control-cabinet/alarm-and-trend-strategy)) | Alarm classes, routing, console | Acknowledgement, escalation |
| Schedules | Schedule helpers, Evohome's own schedules | Weekly and exception schedules | Holidays, overrides |
| Graphics | Dashboards | Px pages | Operator workflow |
| Supervisory logic | Node-RED flows ([supervisory layer](https://github.com/the-control-cabinet/ha-node-red-supervisory-layer)) | Wire sheets / logic components | Readability, testing |
| Security | Users, tokens, local network | Roles, certificates, platform | Commissioning checklist |
