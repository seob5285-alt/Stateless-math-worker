# Stateless Math & Array Aggregation Worker (MoltPe x402 Powered)

An ultra-efficient, zero-maintenance utility service built on **Hono** and **Cloudflare Workers**. It solves the non-deterministic calculation liabilities common to LLM agents by performing 100% precise data cleaning, mathematical aggregation, and matrix grouping on the edge in microseconds.

## Specifications & Machine Pricing
- **Payment Layer:** x402 Open Protocol Standard (MoltPe Native Engine)
- **Execution Cost:** 1,000 micro-USDC ($0.001 USD) per request
- **Settlement Chain:** Base Network Mainnet (`eip155:8453`)
- **Compliance Structure:** Handled via MoltPe aggregation routing (Simple Service Revenue).

## Operational Workflow

When an autonomous agent makes an unpaid request, the engine returns an `HTTP 402 Payment Required` response containing transaction requirements. Native x402 agents automatically detect these headers, execute a gasless stablecoin settlement signature through MoltPe, and instantly resubmit the request to finish the task.

### Core Routes
`POST /aggregate`

#### Input Structure Example
```json
{
  "data": [
    { "revenue": "$1,450.00px", "category": "Utilities" },
    { "revenue": "300.50 USD", "category": "Utilities" },
    { "revenue": "$12.00", "category": "Consulting" }
  ],
  "targetKey": "revenue",
  "groupBy": ["category"]
}