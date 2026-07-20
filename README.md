## Hi, I'm RootSwitch

I'm a Network Engineer with a passion for diagrams. I build small, self-hosted
tools with an ethos of simplicity and usability - each does one thing well, runs
on hardware you already have, and makes no calls home. Together they turn a
network diagram into a live view of the network behind it: draw it, watch it,
measure it, and catch what it says.

It's all public domain and yours to fork or reuse without asking - only the
open-source packages each tool builds on keep their own licenses.

### [CrossCanvas](https://github.com/RootSwitch/CrossCanvas) - network diagram editor

A lightweight, locally hostable editor that runs in any browser with no build
step and no network calls. Imports Visio, Gliffy, and draw.io diagrams plus
common device-inventory formats, so you can diagram an existing environment fast
instead of starting from a blank page.

### [PingCanvas](https://github.com/RootSwitch/PingCanvas) - live monitoring wall

Point it at a CrossCanvas board whose devices carry IP addresses and it becomes
a status wall that recolors each device by reachability. A small PowerShell
poller pings; a read-only kiosk shows the result on any screen.

### [SNMPCanvas](https://github.com/RootSwitch/SNMPCanvas) - metrics and history for the wall

Polls devices over SNMP and keeps the history - interfaces, CPU, memory,
temperature, UPS and PDU sensors. It discovers what each device exposes, graphs
it over time, and feeds live readings back onto a PingCanvas wall, so a link on
the diagram can show its real throughput and a device its real load. One small
self-hosted container.

### [SyslogCanvas](https://github.com/RootSwitch/SyslogCanvas) - syslog and SNMP trap receiver

A quiet place for your devices' logs to land. Receives syslog and SNMP traps,
stores them with sensible retention, and gives you a fast searchable view - the
thing you want already running the moment something misbehaves after a reboot.
Self-hosted, no external services.
