# Self-Calibrating VLAs: Test-Time Embodiment Alignment for Vision-Language-Action Models

Keuntae Kim and Yong Suk Choi (Hanyang University)

**Paper:** [`paper/TEA_SelfCalibratingVLA.pdf`](paper/TEA_SelfCalibratingVLA.pdf) (preprint; to be submitted to CVPR 2027)

Vision-language-action (VLA) models that master standard manipulation benchmarks still collapse when the robot
starts from a slightly different pose or the camera is moved. We show that much of this failure does not lie in the
policy: the robot's embodiment departs from the one the VLA was trained on, and the VLA cannot tell that anything has
changed. **Test-Time Embodiment Alignment (TEA)** turns a VLA into a self-calibrating one. It predicts how the training
embodiment would realize each command and how the robot should appear to its camera, and corrects the VLA's commands
and view only when the evidence shows that the body has departed from training. TEA is never told what has changed,
leaves the policy untouched, works on top of whatever controller the robot uses, and needs no data from the deployment
condition.

Across five benchmarks, three robots and six VLAs, TEA lifts initial-state success by up to 59 points and
camera-perturbed success by up to 21 points on LIBERO-Plus, recovers persistent action perturbations (38–60% to 81–88%
under RobustVLA's action bias), and carries over to a dual-arm robot and to the Google Robot in SimplerEnv, while
leaving unperturbed performance intact.

Code will be released with the paper.

```bibtex
@misc{kim2026tea,
  title        = {Self-Calibrating VLAs: Test-Time Embodiment Alignment for Vision-Language-Action Models},
  author       = {Kim, Keuntae and Choi, Yong Suk},
  year         = {2026},
  howpublished = {\url{https://github.com/kkt94/self-calibrating-vla}},
  note         = {Preprint}
}
```
