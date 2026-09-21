# ONES Migration Tool

The ONES Migration Tool provides a guided path for migrating Jira and Confluence data to ONES Self-Hosted. This repository is the official place to download the tool, review release history, and find self-service migration guidance.

[Download the latest release](https://github.com/ONES-com/atlassian-migration-tool/releases/latest) · [Migration guide](https://docs.ones.com/import-data-into-ones/) · [Migration Wiki](https://github.com/ONES-com/atlassian-migration-tool/wiki) · [Contact ONES](https://ones.com/contact_us/migration)

## Download

The current public package is **v7.25.0 for Linux AMD64**.

- [Download `migration-tool-linux-amd64-v7.25.0.zip`](https://github.com/ONES-com/atlassian-migration-tool/releases/download/v7.25.0/migration-tool-linux-amd64-v7.25.0.zip)
- [Download `SHA256SUMS`](https://github.com/ONES-com/atlassian-migration-tool/releases/download/v7.25.0/SHA256SUMS)
- [Read the v7.25.0 release notes](https://github.com/ONES-com/atlassian-migration-tool/releases/tag/v7.25.0)

To run the migration tool, download the ZIP package listed under **Assets** in the GitHub Release. GitHub also displays automatically generated source archives; those archives are repository snapshots and are not the migration tool package.

## Choose Your Migration Path

| Source | Target | Start here |
| --- | --- | --- |
| Jira Server or Data Center | ONES Self-Hosted | [Migration Tool Guide](https://docs.ones.com/import-data-into-ones/migration-tool-guide/) |
| Confluence Server or Data Center | ONES Wiki Self-Hosted | [Migration Tool Guide](https://docs.ones.com/import-data-into-ones/migration-tool-guide/) |
| Confluence Cloud | ONES Wiki Self-Hosted | [Atlassian Cloud Migration Guide](https://docs.ones.com/import-data-into-ones/atlassian-cloud-migration-guide/) |
| Jira Cloud | ONES Self-Hosted | [Contact ONES before starting](https://ones.com/contact_us/migration) |
| Jira or Confluence | ONES Cloud | [Contact ONES for assistance](https://ones.com/contact_us/migration) |

## Before You Start

- The target ONES deployment must be **Self-Hosted**. ONES **6.100.6 or later** is recommended.
- Install the tool on a server that can communicate with both the source system and the target ONES environment.
- Keep at least **20 GB of free space** available for the migration tool cache.
- The default migration tool port is `5001` for Jira. Confluence connectivity checks use `5002`.
- During migration, keep at least **15–20% CPU and memory headroom** available.
- Use stable intranet bandwidth of at least **1 Gbps**. For terabyte-scale attachments, **10 Gbps** is recommended.
- Test the migration in a non-production environment before the final migration.

See [Infrastructure and Network Requirements](https://github.com/ONES-com/atlassian-migration-tool/wiki/Infrastructure-and-Network-Requirements) for the readiness checklist.

## Migration Workflow

1. Download and extract the migration tool package.
2. Start the tool and choose the product type, HTTP port, and cache path.
3. Verify connectivity between Jira or Confluence, the migration tool, and ONES.
4. Prepare the source data and create a migration task.
5. Select the target team, projects or spaces, and complete data mapping.
6. Run the migration and review its progress.
7. Copy attachments, rebuild indexes, and verify the migrated data.

The detailed operating steps are maintained in the [official migration documentation](https://docs.ones.com/import-data-into-ones/) and summarized in this repository's [Wiki](https://github.com/ONES-com/atlassian-migration-tool/wiki).

## Migration Methods

Jira migrations can use different source-data methods depending on the source environment, migration scale, and completeness requirements.

| Method | Typical use |
| --- | --- |
| REST API | Jira Cloud, smaller migrations, or supplementary synchronization |
| Jira backup package | Repeatable, point-in-time migration from Jira Server or Data Center |
| Read-only database connection | Large Jira Server or Data Center migrations or project-scoped migration |

Review [Migration Methods: API vs. Backup vs. Database](https://docs.ones.com/import-data-into-ones/migration-methods/) before choosing a method.

## Documentation

- [Jira & Confluence Migration](https://docs.ones.com/import-data-into-ones/)
- [Migration Tool Guide](https://docs.ones.com/import-data-into-ones/migration-tool-guide/)
- [Atlassian Cloud Migration Guide](https://docs.ones.com/import-data-into-ones/atlassian-cloud-migration-guide/)
- [Server & Network Requirements](https://docs.ones.com/import-data-into-ones/server-network-requirements/)
- [Migration Data Scope](https://docs.ones.com/import-data-into-ones/migration-data-scope/)
- [Troubleshooting & Maintenance](https://docs.ones.com/import-data-into-ones/troubleshooting-maintenance/)
- [Repository changelog](./changelog/)

## Feedback and Support

Use [GitHub Discussions](https://github.com/ONES-com/atlassian-migration-tool/discussions) for migration questions, planning guidance, and general feedback.

Use [GitHub Issues](https://github.com/ONES-com/atlassian-migration-tool/issues) for reproducible migration problems, installation problems, download problems, and documentation corrections. Do not post passwords, tokens, cookies, private URLs, customer data, or unredacted logs in public issues.

For migration assistance involving a customer environment or sensitive information, [contact ONES privately](https://ones.com/contact_us/migration).
