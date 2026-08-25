# Auth0 Security Overview

Monitor Auth0 authentication activity, failures, user lifecycle changes, source IPs, and security events from Auth0 Custom Webhook logs ingested into Parseable.

## What the dashboard shows

- **Overview:** unique Auth0 events, successful logins, failure events, and signup/deletion activity.
- **Authentication Trends:** categorized event volume over time and Auth0 event-code distribution.
- **Security Details:** top source IPs for failed events and a recent security-event investigation table.

Queries count distinct `log_id` values so Auth0's at-least-once webhook delivery does not inflate dashboard totals.

## Data used

| Signal | Default dataset | Query language | Purpose |
| --- | --- | --- | --- |
| Auth0 logs | `auth0_logs` | SQL | Authentication, user lifecycle, administrative, and security events delivered by an Auth0 Custom Webhook |

Expected fields include `log_id`, `p_timestamp`, `data_type`, `data_description`, `data_client_name`, `data_user_id`, `data_user_name`, `data_ip`, `data_client_ip`, and `data_location_info_country_code`.

## Filters

The dashboard provides one dataset variable:

- **Dataset:** Parseable dataset receiving Auth0 webhook events; defaults to `auth0_logs`.

## Dashboard contents

- **8 tiles** across **3 collapsible sections**
- SQL panels over flattened Auth0 JSON logs
- Importable template: [`auth0-security-overview-sql.json`](https://github.com/parseablehq/dashboards/blob/main/auth0-security-overview/auth0-security-overview-sql.json)

## Ingestion

Configure an Auth0 Custom Webhook with:

- Payload URL: `https://<parseable-host>/api/v1/logstream/auth0_logs`
- Content type: `application/json`
- Content format: `JSON Array`
- Authorization: Parseable Basic authentication for direct Dashboard configuration

The Parseable endpoint must be publicly reachable over trusted HTTPS. For production, use dedicated ingestion credentials instead of an administrator account.

## Import

Download the JSON file and use Parseable's dashboard import flow. During import or after creation, map the dataset variable to the dataset receiving Auth0 events.
