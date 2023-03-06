---
description: n8n's privacy policies
tags:
  - gdpr
  - data collection
  - pid
  - payment processor
hide:
  - tags
---


# Privacy

This page describes n8n's data privacy practices.

## GDPR

### Data protection addendum

For Cloud versions of n8n, n8n is considered both a Controller and a Processor as defined by the GDPR. As a Processor, n8n implements policies and practices that secure the personal data you send to the platform, and includes a [Data Processing Addendum](https://n8n.io/legal/#data){:target=_blank .external-link} as part of the company's standard [Terms of Service](https://n8n.io/legal/#terms){:target=_blank .external-link}.

The n8n Data Protection Addendum includes the [Standard Contractual Clauses (SCCs)](https://ec.europa.eu/info/law/law-topic/data-protection/international-dimension-data-protection/standard-contractual-clauses-scc_en){:target=_blank .external-link}. These clarify how n8n handles your data, and they update n8n's GDPR policies to cover the latest standards set by the European Commission.

You can find a list of n8n sub-processors [here](https://n8n.io/legal/#subprocessors){:target=_blank .external-link}.

!!! note "Self-hosted n8n"
		For self-hosted versions, n8n is neither a Controller nor a Processor, as we don't manage your data

### Submitting a GDPR deletion request

Email privacy@n8n.io to request data deletion.

### GDPR for self-hosted users

--8<-- "_snippets/privacy-security/gdpr-self-hosted.md"



## Data collection

n8n collects selected usage and performance data to help diagnose problems and improve the platform. n8n takes care to keep this data anonymous and to avoid collecting sensitive data. Read about how n8n stores and processes this information in the [privacy policy](https://n8n.io/legal/#privacy){:target=_blank .external-link}.

### What n8n collects

- Error codes and messages of failed executions (excluding any payload data, and not for custom nodes)
- Error reports for app crashes and API issues
- The graph of a workflow (types of nodes used and how they're connected)
- From node parameters:
    - The 'resource' and 'operation' that a node is set to (if applicable)
    - For HTTP request nodes, the domain, path, and method (with personal data anonymized)
- Data around workflow executions:
  - Status
  - The user ID of the user who ran the execution
  - The first time a workflow loads data from an external source
  - The first successful production (non-manual) workflow execution
- The domain of webhook calls, if specified (excluding subdomain).
- Details on how the UI is used (for example, navigation, nodes panel searches)
- Diagnostic information
    - n8n version
    - Selected settings:
        - DB_TYPE
        - N8N_VERSION_NOTIFICATIONS_ENABLED
        - N8N_DISABLE_PRODUCTION_MAIN_PROCESS
        - [Execution variables](/hosting/environment-variables/environment-variables/#executions)
        - N8N_BASIC_AUTH_ACTIVE
    - OS, RAM, and CPUs
    - Anonymous instance ID
 - IP address

### What n8n doesn't collect

n8n doesn't collect private or sensitive information, such as:

- Personally identifiable information (except IP address)
- Credential information
- Node parameters (except 'resource' and 'operation')
- Execution data
- Sensitive settings (for example, endpoints, ports, DB connections, username/password)
- Error payloads

### How collection works

Most data is sent to n8n as events that generate it occur. Workflow execution counts and an instance pulse are sent periodically (every 6 hours).

### Opting out of telemetry

Telemetry collection is enabled by default. To disable it you can configure the following environment variables.

To opt out of telemetry events:

```bash
export N8N_DIAGNOSTICS_ENABLED=false
```

To opt out of checking for new versions of n8n:

```bash
export N8N_VERSION_NOTIFICATIONS_ENABLED=false
```

See [configuration](/hosting/configuration/) for more info on how to set environment variables.

### Documentation telemetry

n8n's documentation (this website) uses cookies to recognize your repeated visits and preferences, as well as to measure the effectiveness of our documentation and whether users find what they're searching for. With your consent, you're helping us to make our documentation better.

[Change cookie settings](#__consent){ .md-button }

## Retention and deletion of personal identifiable data

PID (personal identifiable data) is data that's personal to you and would identify you as an individual.

### n8n Cloud

#### PID retention

n8n only retains data for as long as necessary to provide the core service. 

For n8n Cloud, n8n stores your workflow code, credentials, and other data indefinitely, until you choose to delete it or close your account. The platform stores execution data according to the retention rules on your account.

n8n deletes most internal application logs and logs tied to subprocessors within 30 days. The company retains a subset of logs for longer periods where required for security investigations.

#### PID deletion

If you choose to delete your n8n account, n8n deletes all customer data and event data associated with your account. n8n deletes customer data in backups within 30 days.

### Self-hosted

Self-hosted users should have their own PID policy and data deletion processes. Refer to [What you can do](/privacy-security/what-you-can-do/) for more information.

## Payment processor

n8n uses Paddle.com to process payments. When you sign up for a paid plan, Paddle transmits and stores the details of your payment method according to their security policy. n8n stores no information about your payment method.