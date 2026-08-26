# North-West Asset Finance — Network Design Project

**Module:** CMPG 325 — Computer Networks (Individual Semester Project)
**Project ID:** CMPG325-2026-011 &nbsp;|&nbsp; **Client ID:** CLI-011
**Student:** Choto, HMB (45285209)
**Assigned Organisation:** North-West Asset Finance (Rustenburg) — Banking & Finance
**Assigned Technical Challenge:** ACLs (traffic filtering policy) — Intermediate

## Project Overview

This repository is the portfolio of evidence for the design, simulation, and
configuration of a Cisco Packet Tracer network for North-West Asset Finance.
The solution segments the client into departmental VLANs, applies an IP
addressing plan derived from the assigned block `192.168.14.0/24`, and
implements an ACL policy that satisfies the client's sharing constraint and
guest Wi-Fi change request.

- **Design constraint:** Printer sharing must cross departments; file sharing must not.
- **Change request (CR3):** Guest Wi-Fi must be added for visitors, isolated from internal resources.

## Repository Structure

```
├── 01-requirements/     # Client requirements, brief, assumptions
├── 02-design/           # Physical & logical topology diagrams, IP addressing plan
├── 03-packet-tracer/    # Working .pkt file(s)
├── 04-configuration/    # Router/switch configs, ACL scripts
├── 05-testing/          # Connectivity & ACL verification evidence (screenshots, logs)
├── 06-video/            # Link to the 15–20 minute demonstration video
└── README.md            # This file
```

## Milestone Progress

| Milestone | Due | Status |
|---|---|---|
| Project commencement | 14 Aug 2026 | ✅ Done |
| Milestone 1 — Client Design Review | 28 Aug 2026 | ✅ Requirements, topology, IP plan committed |
| Milestone 2 — Client Implementation Review | 02 Oct 2026 | ⬜ Not started |
| Final Submission | 16 Oct 2026 | ⬜ Not started |

## Design Summary

| VLAN | Purpose | Subnet | Gateway |
|---|---|---|---|
| 10 | Admin / Management | 192.168.14.0/27 | 192.168.14.1 |
| 20 | Loans Department | 192.168.14.32/27 | 192.168.14.33 |
| 30 | Client Services | 192.168.14.64/27 | 192.168.14.65 |
| 40 | Servers (File + Print) | 192.168.14.96/28 | 192.168.14.97 |
| 99 | Guest Wi-Fi (CR3) | 192.168.14.112/28 | 192.168.14.113 |

Full detail: see `02-design/Milestone1_Report.docx`.

## Academic Integrity

This work is my own. Any AI assistance used during this project complies with
the NWU AI Policy; I remain responsible for the correctness, understanding,
and verification of everything submitted.
