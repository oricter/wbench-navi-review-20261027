# Class B self-review — case 64

Reviewed the current `official-first-frame.jpg`, `opening-gate.jpg`, and `motion-30fps.mp4`, together with `COMPOSITION.json`, `OPENING_LOCK.json`, and `TRAJECTORY.json`. The current video is 164 frames, 960×540, 30 fps, lasting 5.467 seconds. Inspected decoded samples every 10 frames plus the final frame and measured adjacent-frame differences across the entire video. This replaces the previous review of different, older artifacts. Visual conclusions are limited to the sampled frames; difference measurements provide additional continuity evidence.

1. **Still nearly-static? NO. World-space travel visible? YES.** After a short opening hold (approximately the first 0.7 seconds), the balloon recedes smoothly while the farmhouse moves down and exits the frame. The winding road, river, trees, and field boundaries shift substantially through the foreground, with successive terrain approaching beneath the camera. This is clear scene travel, not just balloon animation or a stationary view.

2. **Hard cuts / teleports / camera mode switches? NO observed.** The external aerial viewpoint continues through the clip; balloon recession and terrain movement develop progressively. Fresh full-resolution grayscale adjacent-frame MAE is maximum 10.87/255, mean 6.36, and p95 10.35, without a large global discontinuity. `TRAJECTORY.json` also reports zero spikes at its 28/50 thresholds, no near-black frames, and `nearly_static: false`. Its numeric MAEs differ from this independently measured method and are supporting evidence, not identical measurements.

3. **Clipping / through-wall / subject collapse? NO observed.** The balloon retains its rounded envelope, colored bands, and suspended basket as it becomes smaller. No major terrain penetration or collapsed subject is visible. Simplified trees, repetitive fields, and reduced distant detail affect fidelity but do not constitute major clipping.

4. **Opening matches official composition reasonably? YES.** Both images place the striped balloon centrally in the upper-middle view, above countryside with farm buildings below and a winding road to the right. Approximate envelope bounds are x=530–847, y=83–443 in the 1376×768 official image and x=373–584, y=61–301 in the 960×540 opening: normalized widths are about 23% and 22%, heights 47% and 44%, and vertical centers both about 34%. The visible skyline is near 42% versus 44% of image height. The stylized farmhouse is smaller and lower, and the scenery is less detailed, but the primary framing reasonably matches.

   `COMPOSITION.json` reports PASS within all configured tolerances. Its reported horizon values do not describe the visible skyline precisely, so the visual comparison above is the basis for acceptance. `OPENING_LOCK.json` reports PASS (MAE 1.311); fresh decoded-frame-zero versus gate RGB MAE is 1.93/255, with visually matching framing. Opening lock is OK.

5. **Arms/panel pop-in (if cockpit) or subject missing? NO observed.** This is an exterior view; cockpit checks are not applicable. The balloon remains visible in every inspected sample through the final frame, with its basket discernible beneath it.

6. **Verdict: PASS.** The current artifacts show clear world displacement, no observed jump-cuts or major clipping, a reasonable official opening composition, and a consistent gate-to-video opening lock.

7. **If FAIL: concrete next fix.** Not applicable; no playable fix is required by this review.

No recording was started. No playable files were modified.
