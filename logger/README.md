# Logger

Records every episode and every human intervention.

## Intervention event (draft schema)

| Field | Type | Meaning |
|---|---|---|
| `event_id` | uuid | Unique ID |
| `cell_id` | string | Which cell |
| `episode_id` | string | Which episode |
| `t_start`, `t_end` | timestamp | When the human took over and handed back |
| `mode` | enum | `click_correct`, `vr_takeover`, `estop` |
| `reason_code` | enum | `grasp_fail`, `pose_uncertain`, `part_unknown`, `collision_risk`, `jam`, `other` |
| `note` | string | Free text (optional) |
| `state_before`, `state_after` | ref | Pointers to frames and joint states |
| `outcome` | enum | `recovered`, `skipped_part`, `stopped` |

Episodes are exported to LeRobot dataset format (`../datasets/`).
