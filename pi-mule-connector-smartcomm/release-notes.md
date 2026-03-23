# SmartCOMM Connector Release Notes

## Version 1.0.0 — March 2026

### Overview

This is the first release of the consolidated **SmartCOMM Connector** for MuleSoft 4. It replaces all previous SmartCOMM connectors published on Anypoint Exchange, providing a single unified connector for all SmartCOMM API integrations.

### Compatibility

| Software             | Version |
|----------------------|---------|
| Mule Runtime         | 4.9 LTS |
| Java                 | 17      |
| SmartCOMM DocGen API | v14     |
| SmartCOMM CMS API    | v18     |
| SmartCOMM Bulk API   | v11     |

### What's New

#### Unified Connector

A single connector replaces the previously separate SmartCOMM connectors available on Anypoint Exchange. All supported SmartCOMM APIs are available from one connector artifact.

#### Supported Operations

- **DocGen** (16 operations) — Document generation including synchronous and asynchronous generation, draft management, interview support, template preview, shared content, and batch operations.
- **CMS** (51 operations) — Content Management System operations covering projects, folders, resources, versioning, publishing, categories, annotations, and package import/export.
- **Bulk** (25 operations) — Bulk document processing including job management, queue management, spool and bundle retrieval, and appliance operations.

#### Authentication

Authentication uses the OAuth2 Client Credentials flow with automatic token management and renewal.

#### Additional Features

- Configurable connection and read timeouts (default: 10 seconds each)
- HTTP proxy support
- Custom TLS/truststore configuration for on-premises deployments
- Structured error types via `SMARTCOMM` error namespace

### Migration from Previous Connectors

Remove any previously installed SmartCOMM connectors from your Mule project and replace them with this connector. Operation names and parameters have been aligned with the current SmartCOMM API versions (DocGen v14, CMS v18, Bulk v11). Review your existing flows for any operation signature changes introduced by the API version upgrades.
