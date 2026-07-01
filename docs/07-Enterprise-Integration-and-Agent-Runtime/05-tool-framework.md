# Tool Framework

A tool is the business-facing action available to an agent. A connector is the technical implementation behind that action.

## Tool examples

- Query customer record
- Create support case
- Retrieve policy document
- Generate approval summary
- Write audit annotation

## Connector examples

- REST API connector
- JDBC connector
- SOAP connector
- File connector
- Kafka connector
- MCP connector
- SAP connector
- Fusion connector

## Tool contract

Every tool should define:

- name and version
- purpose
- required inputs
- output shape
- security scope
- allowed resources
- telemetry requirements
- failure behavior

## Separation rule

The platform should never expose a connector directly to orchestration. Orchestration selects a tool. The tool is then mapped to one or more connectors by the integration layer.
