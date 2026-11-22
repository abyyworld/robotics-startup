# Metrics

Use exactly the same definitions everywhere: the README, the weekly log and applications.

| Metric | Definition |
|---|---|
| Intervention | Any moment a human takes control or corrects the robot. Logged with a reason code. |
| Interventions per robot-hour | Interventions ÷ hours the cell was running. Reported weekly. |
| Success rate | Units completed correctly ÷ units attempted. |
| Cycle-time ratio | Robot seconds per unit ÷ human seconds per unit (from the stopwatch baseline). |
| Robots per operator | Cells one person supervises at once without the success rate dropping. |

Output every Friday: `chart.png` and `metrics.csv`.
