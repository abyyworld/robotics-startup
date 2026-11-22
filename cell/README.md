# Cell

- `tasks/`: one folder per candidate task: `part_sorting/`, `cnc_tending/`, `tray_assembly/`.
- `arm_drivers/`: the SO-101 driver and the cobot driver (ROS 2).
- `safety/`: interlock notes and a risk-assessment template. The local safety controller always has the final say; remote operators send goals, not raw motion.

No customer installation without a risk assessment, insurance and an integrator's sign-off.
