## Hi, I'm RootSwitch

I'm a Network Engineer with a passion for diagrams. I build small, self-hosted
tools with an ethos of simplicity and usability - each does one thing well, runs
on hardware you already have, and makes no calls home.

It's all public domain and yours to fork or reuse without asking - only the
open-source packages each tool builds on keep their own licenses.

### [Canvas Suite](https://github.com/RootSwitch/canvas-suite) - draw your network, watch it live

The main event: six apps that turn a network diagram into a live view of the
network behind it - draw it, watch it, measure it, catch what it says, get
paged when it breaks, and walk in through one front door. Each is useful
alone; together they cover the ground of a monitoring platform without the
platform. The suite repo is the landing page, with one-shot install scripts
that stand the whole thing up on a fresh Linux box (or a Raspberry Pi) in
minutes - and there's a
[live demo](https://rootswitch.github.io/canvas-suite-demo/) to click around
first, no install required.

The pieces:

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

### [AlertCanvas](https://github.com/RootSwitch/AlertCanvas) - the one that taps you on the shoulder

Watches the values SNMPCanvas exports and the devices PingCanvas pings, walks
them through honest raise/clear alarm state (no flapping, no stale alerts), and
notifies by email, ntfy, or syslog - so the wall works even when nobody is
looking at it.

### [LaunchCanvas](https://github.com/RootSwitch/LaunchCanvas) - the suite's front door

One login, a tile for every app, opt-in single sign-on across the suite, and
board upload/download from the browser - the address you give someone that
makes six ports feel like one product.
