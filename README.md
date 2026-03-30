# CLOUDCRAFT — Cloud Architecture Planner

Visual cloud architecture design tool focused on Azure. Drag and drop 21 resource types onto a blueprint canvas, configure SKUs and regions, draw connections, and get live monthly cost estimates. Export to Terraform HCL, ARM templates, Mermaid diagrams, or formatted cost reports. Single HTML file, zero dependencies.

## Live Demo

**[nexusfang-tech.github.io/cloudcraft](https://nexusfang-tech.github.io/cloudcraft/)**

## Resource Types (21)

| Category | Resources |
|----------|-----------|
| Compute | Virtual Machine (6 SKUs), App Service (5 tiers), Functions, Container Instance, AKS |
| Networking | Virtual Network, Load Balancer, App Gateway/WAF, DNS Zone, VPN Gateway, NSG |
| Storage & DB | Storage Account, Azure SQL (5 tiers), Cosmos DB, Redis Cache (4 tiers) |
| Identity & Security | Entra ID, Key Vault, Sentinel (SIEM) |
| Integration & Monitoring | Logic App, Azure Monitor, API Management (4 tiers) |

## Features

- **Drag-and-drop canvas** — Place resources from the sidebar palette onto a blueprint grid
- **Live cost estimation** — Every resource has a monthly cost that updates when you change SKUs. Running total with category breakdown and annual projection
- **SKU/tier selection** — Change VM sizes, App Service plans, SQL tiers, etc. directly in the properties panel
- **Resource configuration** — Region, CIDR blocks, replication, OS, runtime, NSG rules, and more
- **Connection drawing** — Click and drag between resource ports to create bezier curve connections
- **Auto layout** — Arranges resources by category in columns
- **Demo architecture** — Pre-built NCACC-style Azure stack (DNS → App Gateway/WAF → NSG → VM → SQL + Key Vault + Entra ID + Storage + Monitor → Sentinel)
- **Save/Load** — Persist architectures to browser localStorage

## Export Formats

| Format | Output |
|--------|--------|
| Terraform HCL | `azurerm` provider resource blocks with proper syntax and cost comments |
| ARM Template | Azure Resource Manager JSON deployment template |
| Mermaid | Diagram markup with category-colored node styling |
| Cost Report | Formatted text with per-resource breakdown, category totals, and percentages |

## Tech Stack

Vanilla JavaScript · HTML Canvas · CSS · GitHub Pages

## Author

**Matt Keith** · [nexusfang-tech.github.io](https://nexusfang-tech.github.io)
