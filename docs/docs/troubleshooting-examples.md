# Automation and Infrastructure Troubleshooting Examples

These are sanitized examples from independent technical projects.

No credentials, private infrastructure details, client data or personal information are included.

## 1. Missing or Inconsistent Workflow Data

### Problem

Automation workflows may receive missing, empty or differently structured values from forms, APIs or previous workflow steps.

This can cause later nodes to fail or produce incorrect results.

### Approach

- Inspect the input and output of each workflow step.
- Identify where the expected value changes or disappears.
- Check field names, nested JSON paths and data types.
- Normalize incoming values before processing.
- Validate required fields.
- Route invalid records to a separate error path.
- Preserve the original input for later review.

### Result

The workflow becomes more predictable, and invalid records can be reviewed without stopping valid processing.

## 2. Duplicate Record Prevention

### Problem

Webhook retries, repeated submissions or interrupted executions can create duplicate records or repeated actions.

### Approach

- Identify a stable external record ID.
- Check whether the record has already been processed.
- Store or compare an idempotency value.
- Use update operations where appropriate.
- Track processing status and timestamps.
- Test repeated delivery of the same payload.

### Result

Repeated inputs can be processed safely without creating unnecessary duplicate records.

## 3. API Authentication Failures

### Problem

API requests may fail because of expired credentials, incorrect headers, invalid tokens or changed authentication requirements.

### Approach

- Inspect the API response code and error body.
- Confirm the required authentication method.
- Check request headers and token formatting.
- Test the API request separately from the full workflow.
- Add a dedicated route for authentication errors.
- Avoid exposing credentials in logs and screenshots.
- Document how credentials are renewed.

### Result

Authentication problems can be separated from data-processing and workflow-logic problems.

## 4. API Rate Limits and Temporary Failures

### Problem

External APIs may reject requests when too many requests are sent or when the service is temporarily unavailable.

### Approach

- Inspect response codes and retry headers.
- Reduce unnecessary requests.
- Process records in controlled batches.
- Add delays where necessary.
- Use retries with increasing wait periods.
- Set a maximum number of retry attempts.
- Route unresolved records for later review.
- Avoid retrying permanent validation errors.

### Result

The workflow can recover from temporary failures without entering uncontrolled retry loops.

## 5. Linux or Docker Service Unavailable

### Problem

A self-hosted service may stop responding even when the host machine remains online.

### Approach

- Check service and container status.
- Review recent logs.
- Test the health-check endpoint.
- Confirm the expected port is available.
- Check configuration and environment variables.
- Verify dependent services.
- Restart only the affected service where possible.
- Confirm recovery after the restart.
- Document the cause and corrective action.

### Result

Service failures can be isolated without restarting unrelated infrastructure.

## 6. Workflow Error Handling

### Problem

A complete workflow may stop because one record or external request fails.

### Approach

- Separate successful and failed processing paths.
- Preserve the original failed input.
- Record the failed workflow stage and error message.
- Classify failures as temporary or permanent.
- Retry only temporary failures.
- Allow unrelated valid records to continue.
- Add a manual-review route for unresolved failures.
- Test the failure path deliberately.

### Result

Individual failures do not automatically prevent the rest of the workflow from completing.

## General Troubleshooting Process

1. Reproduce the problem.
2. Inspect inputs and outputs.
3. Identify the earliest incorrect result.
4. Separate data, authentication, configuration and availability issues.
5. Test the smallest affected component.
6. Apply one controlled change at a time.
7. Verify both the normal path and failure path.
8. Document the solution and remaining limitations.

## Tools and Areas Used

- n8n execution data
- REST API responses
- JSON payloads
- webhooks
- JavaScript transformations
- Linux service status
- Docker container logs
- systemd logs
- health-check endpoints
- WordPress REST API
- validation and error routing
