# 🛜 Enterprise-Grade-Home-Lab-DNS-Security-Remote-Access-Gateway
This project demonstrates the design, deployment, and configuration of an enterprise-aligned DNS security filter and cryptographic VPN remote access gateway hosted on a dedicated Linux-based single-board computer (Raspberry Pi).

The infrastructure enforces network-wide telemetry control, DNS-layer threat mitigation, and encrypted remote access for internal endpoints, mirroring core modern network administration and Zero Trust edge access principles.

# 🛜 Key Technical Features
<ul>
  <li>Network-Wide DNS Filtering: Centralized DNS sinkhole (Pi-hole) blocking ad domains, trackers, telemetry, and known malware endpoints for all local network clients.</li>
  <li>Upstream Secure DNS Forwarding: Encrypted DNS forwarding through secure upstream providers (Cloudflare/Quad9) to prevent ISP inspection and spoofing.</li>
  <li>Custom Adlists & Regex Blocking: Integration of dynamic blocklists to proactively block emerging threat vectors and ad networks.</li>
  <li>Query Logging & Forensics: Real-time visibility into internal client DNS queries, query latency, and domain resolution patterns.</li>
</ul>

# 🛜 Network Typology 
```mermaid
flowchart TD
    A[Client Devices<br/>PC, Mobile, IoT] -->|DNS Queries Port 53| B[Raspberry Pi<br/>Pi-hole DNS Sinkhole]
    B -->|Filtered Forwarding| C[Upstream DNS<br/>Cloudflare 1.1.1.1]

    style A fill:#eef2f7,stroke:#3b82f6,stroke-width:2px
    style B fill:#eef2f7,stroke:#3b82f6,stroke-width:2px
    style C fill:#eef2f7,stroke:#3b82f6,stroke-width:2px
