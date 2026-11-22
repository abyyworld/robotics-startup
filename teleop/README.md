# Teleop

- `leader_follower/`: an SO-101 leader arm drives the follower.
- `vr/`: an operator in a Quest takes over mid-task (WebXR or Unity). The default supervision mode is screen click-to-correct; VR is for full takeovers.

Every takeover goes through the logger (`../logger/`) with a reason code.
