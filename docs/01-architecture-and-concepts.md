# 01 · Niagara 4: Architecture and Concepts

[← Back to README](../README.md)

| Concept | What it is | Home Assistant equivalent (roughly) |
|---|---|---|
| **Station** | The running Niagara application: drivers, points, services, graphics, all as components in one tree | An HA instance |
| **Platform** | The host layer underneath a station (installation, licences, certificates, station start/stop) | The HA OS / Supervisor |
| **Workbench** | The engineering tool used to build and maintain stations | Settings, YAML and the developer tools |
| **Component model** | Everything is a typed component with slots (properties, actions, topics), wired graphically or by links | Entities, attributes and services |
| **Drivers** | Protocol networks (BACnet, Modbus, Trend, S7, …) with devices and their points under them | Integrations |
| **Points** | Proxy points to device values, with facets (units, precision) and status (fault, stale, overridden) | Entities with units and availability |
| **Tags** | Haystack-style metadata on components, for searching and templating | Labels, areas, device classes |
| **Services** | Station-wide functions: histories, alarms, schedules, users | Recorder, alerts/automations, schedules, users |
| **Px graphics** | Operator pages bound to points | Dashboards |

**Hardware:** a **JACE** is an embedded controller running a station at the edge (field buses, local histories); a **supervisor** runs a station on a server, aggregating many JACEs. The JACE-8000 is the long-standing model (now succeeded by newer hardware); for learning, a station on a PC is enough. **Branding** (Tridium, Honeywell or an OEM) matters less than the Niagara **version** and the **licence** (which drivers and point counts are enabled).

**Typical place in a building:** field controllers (DDCs such as the IQ411) → JACE → supervisor/head end. PLCs appear more on the plant/industrial side, and Niagara can sit above them through drivers.

**Licensing:** Workbench and station licences come through Tridium's channel (OEMs, integrators, distributors); for an individual, the **Niagara 4 TCP** course is the usual route to software access.
