# robotics-startup

Robot cells that do one factory job, with a remote human who fixes mistakes in VR.
Every fix becomes training data, so one operator can supervise more robots every month.

> **Status:** setup. No robot code yet. Code lands once the IP position is confirmed in writing (see [ROADMAP.md](ROADMAP.md), M0).

`[60-second demo GIF goes here]`   `[This week's chart: interventions per robot-hour]`

## The two numbers we track

| Metric | Definition | Goal |
|---|---|---|
| Interventions per robot-hour | Human takeovers or corrections ÷ hours the cell ran | Falls every month |
| Robots per operator | Cells one person supervises at once without losing success rate | 1 → 2 → 5 → 20+ |

Full definitions are in [metrics/README.md](metrics/README.md).

## Results so far

| | |
|---|---|
| Task | _not chosen yet: part sorting / CNC machine tending / tray assembly_ |
| Interventions per robot-hour | _a → b over n weeks_ |
| Success rate | _x %_ |
| Cycle time vs human | _y×_ |
| Robots per operator | _z_ |

## How it works

1. **Teleop:** a human shows the task (leader-follower arm or VR).
2. **Policy:** an open robot model (ACT, SmolVLA, π0 via LeRobot/openpi) is fine-tuned on those demos.
3. **Supervised autonomy:** the robot works. When it's unsure or fails, a remote operator takes over by clicking on a screen, or in VR for hard cases.
4. **Logger:** every takeover is recorded with a reason code and becomes new training data.
5. **Metrics:** a chart of interventions per robot-hour is published every Friday.

## Repo layout

| Folder | What's in it |
|---|---|
| [hardware/](hardware/) | Bill of materials, CAD/STL for the gripper, tactile fingertip and camera mounts |
| [teleop/](teleop/) | Leader-follower control and VR takeover |
| [logger/](logger/) | Episode and intervention recording |
| [datasets/](datasets/) | Export to LeRobot dataset format, plus viewers |
| [policy/](policy/) | Training and evaluation |
| [cell/](cell/) | Task setups, arm drivers, safety notes |
| [metrics/](metrics/) | Metric definitions and the weekly chart |
| [remote/](remote/) | Remote supervision over an outbound-only connection |
| [docs/](docs/) | Weekly log, data policy, halal policy |

## Weekly log

One short post every Friday in [docs/weekly-log/](docs/weekly-log/).

## Policies

- [Data policy](docs/data-policy.md): consent, hands-only capture, retention, no worker scoring.
- [Halal policy](docs/halal-policy.md): customer screening and money rules.

## License

Apache-2.0, to be added when the GitHub repo is created. Customer configurations and customer data are never in this repo.
