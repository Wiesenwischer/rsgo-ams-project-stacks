# ams.project Stacks for ReadyStackGo

Stack definitions for [ams.project](https://www.ams-erp.com/) by [ams.Solution AG](https://www.ams-erp.com/) — an enterprise project management system built on microservices.

## Usage

This repository is available as a stack source in [ReadyStackGo](https://github.com/Wiesenwischer/ReadyStackGo). You can add it during the setup wizard or in **Settings > Stack Sources**.

## Products

| Product | Description | Version | Stacks |
|---------|-------------|---------|--------|
| [ams.project](ams-project/) | Enterprise Project Management System | 3.1.0-pre | 16 |
| [ams.identityaccess](ams-identityaccess/) | Standalone Identity Provider | 3.1.0-pre | 1 |

### ams.project

Multi-stack product with Infrastructure, Platform, IdentityAccess and Business Services organized by bounded context:

- **Infrastructure** — EventStore, EventStoreDB, Redis
- **Platform** — Web BFF, Desktop Gateways, ClientHub
- **IdentityAccess** — IdentityServer, AdminPortal, EmailSender
- **Business Services** — ProjectManagement, Discussions, Memo, SalesOrders, Export, ERP Integration, Capacity Planning, Production Planning, Reporting, Project Exporting, Project Import, Public API, Analytics, Monitoring

### ams.identityaccess

Standalone identity provider product that can be deployed independently of ams.project.

## Stack Format

Each product is a directory containing a `stack.yaml` file in the [RSGO Manifest Format](https://github.com/Wiesenwischer/ReadyStackGo). Multi-stack products use `include` references to organize sub-stacks.
