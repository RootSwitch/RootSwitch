## Hi, I'm RootSwitch

I'm a Network Engineer with a passion for diagrams. I build small, self-hosted
tools with an ethos of simplicity and usability - each does one thing well, runs
on hardware you already have, and makes no calls home.

It's all public domain and yours to fork or reuse without asking - only the
open-source packages each tool builds on keep their own licenses.

### [Canvas Suite](https://github.com/RootSwitch/canvas-suite) - draw your network, watch it live

[![Canvas Suite: your network diagram becomes the live dashboard](https://raw.githubusercontent.com/RootSwitch/canvas-suite/main/docs/social-preview.png)](https://github.com/RootSwitch/canvas-suite)

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

<table>
<tr align="center">
<td><a href="https://github.com/RootSwitch/CrossCanvas"><img src="https://raw.githubusercontent.com/RootSwitch/CrossCanvas/main/favicon.svg" width="52" alt="CrossCanvas"><br><b>CrossCanvas</b></a><br><sub>draw the board</sub></td>
<td><a href="https://github.com/RootSwitch/PingCanvas"><img src="https://raw.githubusercontent.com/RootSwitch/PingCanvas/main/kiosk/favicon.svg" width="52" alt="PingCanvas"><br><b>PingCanvas</b></a><br><sub>watch it live</sub></td>
<td><a href="https://github.com/RootSwitch/SNMPCanvas"><img src="https://raw.githubusercontent.com/RootSwitch/SNMPCanvas/main/public/favicon.svg" width="52" alt="SNMPCanvas"><br><b>SNMPCanvas</b></a><br><sub>measure it</sub></td>
</tr>
<tr align="center">
<td><a href="https://github.com/RootSwitch/SyslogCanvas"><img src="https://raw.githubusercontent.com/RootSwitch/SyslogCanvas/main/public/favicon.svg" width="52" alt="SyslogCanvas"><br><b>SyslogCanvas</b></a><br><sub>catch what it says</sub></td>
<td><a href="https://github.com/RootSwitch/AlertCanvas"><img src="https://raw.githubusercontent.com/RootSwitch/AlertCanvas/main/public/favicon.svg" width="52" alt="AlertCanvas"><br><b>AlertCanvas</b></a><br><sub>get paged</sub></td>
<td><a href="https://github.com/RootSwitch/LaunchCanvas"><img src="https://raw.githubusercontent.com/RootSwitch/LaunchCanvas/main/public/favicon.svg" width="52" alt="LaunchCanvas"><br><b>LaunchCanvas</b></a><br><sub>one front door</sub></td>
</tr>
</table>

### [CrossCanvas](https://github.com/RootSwitch/CrossCanvas) - network diagram editor

[![CrossCanvas: draw the network you actually run - no install, no account, no cloud](https://raw.githubusercontent.com/RootSwitch/CrossCanvas/main/docs/social-preview.png)](https://github.com/RootSwitch/CrossCanvas)

A lightweight, locally hostable editor that runs in any browser with no build
step and no network calls. Imports Visio, Gliffy, and draw.io diagrams plus
common device-inventory formats, so you can diagram an existing environment fast
instead of starting from a blank page.

### [PingCanvas](https://github.com/RootSwitch/PingCanvas) - live monitoring wall

[![PingCanvas: your network diagram, with a pulse](https://raw.githubusercontent.com/RootSwitch/PingCanvas/main/docs/social-preview.png)](https://github.com/RootSwitch/PingCanvas)

Point it at a CrossCanvas board whose devices carry IP addresses and it becomes
a status wall that recolors each device by reachability. A small PowerShell
poller pings; a read-only kiosk shows the result on any screen.

### [SNMPCanvas](https://github.com/RootSwitch/SNMPCanvas) - metrics and history for the wall

[![SNMPCanvas: poll your gear over SNMP and keep the history](https://raw.githubusercontent.com/RootSwitch/SNMPCanvas/main/docs/social-preview.png)](https://github.com/RootSwitch/SNMPCanvas)

Polls devices over SNMP and keeps the history - interfaces, CPU, memory,
temperature, UPS and PDU sensors. It discovers what each device exposes, graphs
it over time, and feeds live readings back onto a PingCanvas wall, so a link on
the diagram can show its real throughput and a device its real load. One small
self-hosted container.

### [SyslogCanvas](https://github.com/RootSwitch/SyslogCanvas) - syslog and SNMP trap receiver

[![SyslogCanvas: every syslog message, searchable the moment it lands](https://raw.githubusercontent.com/RootSwitch/SyslogCanvas/main/docs/social-preview.png)](https://github.com/RootSwitch/SyslogCanvas)

A quiet place for your devices' logs to land. Receives syslog and SNMP traps,
stores them with sensible retention, and gives you a fast searchable view - the
thing you want already running the moment something misbehaves after a reboot.
Self-hosted, no external services.

### [AlertCanvas](https://github.com/RootSwitch/AlertCanvas) - the one that taps you on the shoulder

[![AlertCanvas: when a threshold trips, you hear about it](https://raw.githubusercontent.com/RootSwitch/AlertCanvas/main/docs/social-preview.png)](https://github.com/RootSwitch/AlertCanvas)

Watches the values SNMPCanvas exports and the devices PingCanvas pings, walks
them through honest raise/clear alarm state (no flapping, no stale alerts), and
notifies by email, ntfy, or syslog - so the wall works even when nobody is
looking at it.

### [LaunchCanvas](https://github.com/RootSwitch/LaunchCanvas) - the suite's front door

[![LaunchCanvas: one login, every canvas](https://raw.githubusercontent.com/RootSwitch/LaunchCanvas/main/docs/social-preview.png)](https://github.com/RootSwitch/LaunchCanvas)

One login, a tile for every app, opt-in single sign-on across the suite, and
board upload/download from the browser - the address you give someone that
makes six ports feel like one product.

Outside the suite:

### [RSConclave](https://github.com/RootSwitch/RSConclave) - several models, one conversation

[![RSConclave: send one prompt to several models and have another consolidate the answers](https://raw.githubusercontent.com/RootSwitch/RSConclave/main/docs/img/social-preview.png)](https://github.com/RootSwitch/RSConclave)

A web UI for the local LLMs on your own box, and the one thing here that is not
about networks. Send one prompt to several models and have another consolidate
the answers, or seat two of them at a roundtable and let them argue a question
out turn by turn. Personas and presets are reusable, each person's history stays
private, and it runs next to your inference box rather than on one machine, so
the same sessions are there from a desktop or a phone. Zero dependencies, no
build step, nothing leaves the network.
