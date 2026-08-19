# A/B Experiment Brief, RouteLogic (B2B)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Driver Alert Notifications |
| Persona | Fleet Coordinator |
| Expected outcome | Compliance and Reporting will go up if routes update faster and tool is being used as intended |
| Primary success metric | If reporting starts to go up then the routes are updating faster and the tool is being used more reliably |
| Baseline rate | Assign routes utilization is 71% |
| Guardrail metric | Core dispatch must not drop |
| Guardrail boundary | Core dispatch (assign routes) must not drop below  65% |
| Second guardrail | · |
| Minimum Detectable Effect | 5 |
| Sample size per arm | 589 |
| Traffic split | 50/50 |
| Test duration | 14 days |
| Significance threshold | .05 |

## Control vs. Variant
- **Control (A):** Routes are not updating in real time
- **Variant (B):** App will send a notification when a route changes
- **Held constant (isolation check):** Nothing else will change

## Hypothesis
> I believe that Driver Alert Notifications for Fleet Coordinator will result in Compliance and Reporting will go up if routes update faster and tool is being used as intended, as measured by a 5 change in If reporting starts to go up then the routes are updating faster and the tool is being used more reliably within 14 days. We will protect Core dispatch must not drop throughout the test.

## Shipping criteria
> We will **ship** if If reporting starts to go up then the routes are updating faster and the tool is being used more reliably improves by ≥ 5 at .05 and Core dispatch must not drop does not reach Core dispatch (assign routes) must not drop below  65% after 14 days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 days, no results reviewed before this date.
