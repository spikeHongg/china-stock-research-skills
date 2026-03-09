# Routing Matrix

Use this matrix to decide which core modules to run.

## Pattern to Module Routing

| Pattern | Mandatory Modules | Common Optional Modules | Notes |
| --- | --- | --- | --- |
| Business-model transition | `strategy-business-transition`, `financial-health` | `risk-warning-catalysts`, `valuation-investment-strategy`, `industry-competition-moat` | Use when legacy and new business overlap |
| Project or order-driven business | `business-decomposition-order-quality`, `financial-health` | `risk-warning-catalysts`, `valuation-investment-strategy`, `industry-competition-moat` | Revenue quality and cash conversion matter most |
| Asset-heavy ramp | `financial-health`, `risk-warning-catalysts` | `strategy-business-transition`, `valuation-investment-strategy`, `industry-competition-moat` | Focus on capex, ramp-up, financing, utilization |
| Cyclical or price-driven business | `industry-competition-moat`, `valuation-investment-strategy`, `risk-warning-catalysts` | `financial-health` | Separate cycle from moat |
| Consumer channel and brand | `industry-competition-moat`, `business-decomposition-order-quality`, `risk-warning-catalysts` | `financial-health`, `valuation-investment-strategy` | Channel and sell-through quality matter |
| Regulated healthcare or pharma | `industry-competition-moat`, `risk-warning-catalysts`, `valuation-investment-strategy` | `strategy-business-transition`, `financial-health` | Policy and approval cadence drive risk |
| Export manufacturing and supply chain | `business-decomposition-order-quality`, `industry-competition-moat`, `financial-health` | `risk-warning-catalysts`, `valuation-investment-strategy` | Customer concentration, FX, and inventory matter |

## Default Rule

- If the company clearly matches one or two patterns, route by the matrix above.
- If the company matches three or more patterns with similar weight, run all six modules.
- If the business model is unclear, start with `strategy-business-transition`, `financial-health`, and `industry-competition-moat`, then expand.

## Ordering Rule

Default order:

1. `strategy-business-transition`
2. `business-decomposition-order-quality`
3. `financial-health`
4. `industry-competition-moat`
5. `risk-warning-catalysts`
6. `valuation-investment-strategy`

Skip a module only when the pattern logic clearly makes it non-essential.
