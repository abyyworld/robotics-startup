# Roadmap

Each milestone below is a GitHub milestone (Issues → Milestones), with its items as issues.

## Before any code (by 16 Dec 2026)

- [ ] IP position confirmed in writing
- [ ] Arm plan decided: borrowed, rented or refurbished cobot (get quotes)
- [ ] Long-lead parts ordered

## M0: Teleop + logger (target 4 Jan 2027)

- [ ] SO-101 leader-follower teleop working
- [ ] Logger records every episode: cameras, joint states, actions
- [ ] Logger records every human takeover: timestamp, reason code, state before and after
- [ ] Export to LeRobot dataset format
- [ ] **Demo:** a 15-second clip of a human teleoperating a pick

## M1: VR takeover + dashboard (target 31 Jan)

- [ ] Operator in a Quest can take over mid-task
- [ ] Reason-code picker for every takeover
- [ ] Screen click-to-correct mode (the default for supervision)
- [ ] Dashboard: interventions per robot-hour, success rate, cycle time
- [ ] Reproduce the 3 candidate tasks on sample parts
- [ ] **Demo:** the robot runs, fails, and a human fixes it in VR

## M2: First policy (target 28 Feb)

- [ ] Task chosen (G1, 14 Feb)
- [ ] Policy trained on our own data runs the chosen task
- [ ] Real cobot integrated through a ROS 2 driver, with local safety interlocks
- [ ] Weekly chart published every Friday
- [ ] **Demo:** an autonomous run with an on-screen intervention counter

## M3: Customer parts (target 15 Apr)

- [ ] Bench demo on real parts mailed by prospects
- [ ] 100+ logged hours
- [ ] Interventions per robot-hour trending down
- [ ] **Demo:** a 60-second video plus the before/after chart

## M4: Open-source release v0.1 (target 31 May)

- [ ] Quickstart (record, train and evaluate in 3 commands)
- [ ] Docs and data policy finished
- [ ] **Demo:** a launch post with a GIF

## M5: Pilot kit (target: graduation month + 2)

- [ ] Remote supervision over an outbound-only connection
- [ ] One operator running 2 cells
- [ ] Safety file and risk-assessment template (integrator signs off)
- [ ] **Demo:** live pilot footage (only with the customer's OK)
