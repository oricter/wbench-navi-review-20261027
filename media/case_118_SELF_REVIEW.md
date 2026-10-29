# Class B self-review — case_118

Reviewed `official-first-frame.jpg`, `opening-gate.jpg`, and the current `motion-30fps.mp4` (960×540, 474 frames, 30 fps, 15.8 seconds), together with `COMPOSITION.json`, `OPENING_LOCK.json`, and `TRAJECTORY.json`. Visually inspected half-second samples across the complete clip and the final frame; decoded all frames for adjacent-frame continuity measurements. This replaces the stale review of a different, 27.467-second clip.

1. **Still nearly-static? NO. World-space travel visible? YES.** Successive stall posts, pots, awnings, and floor tiles move past the following camera with strong foreground/background parallax. The distant ochre buildings grow as the merchant and cart advance down the aisle. The initial camera pullback settles into a follow view, but environmental displacement continues afterward. `TRAJECTORY.json` reports `nearly_static=false`, sparse MAE mean 23.22, and 474 frames, consistent with the current clip.

2. **Hard cuts / teleports / camera mode switches? NO observed.** The opening framing widens smoothly into the follow view; the stall sequence and subject position progress continuously. No abrupt view change is apparent. The supplied trajectory report has adjacent MAE max 4.17 and zero spikes at 28 or 50. An independent full-resolution grayscale check across all 473 frame pairs gives max MAE 5.628 and mean 4.406; these differently computed values likewise show no large discontinuity.

3. **Clipping / through-wall / subject collapse? NO major issue observed in this clip.** The cart and merchant remain intact in the open central aisle, and the camera passes the flanking stalls without a visible wall crossing. The final frame at 15.77 seconds still shows the merchant, cart, and surrounding market clearly, before the distant building. The simplified thin legs are a fidelity weakness, but no temporal collapse is evident. This assessment covers only the supplied 15.8 seconds; it does not establish collision safety beyond the recorded endpoint.

4. **Opening matches official composition reasonably? YES.** Both openings place a rear-facing, turbaned merchant above a broad fruit cart, with yellow/red/purple produce, striped awnings overhead, market stalls on both sides, and geometric paving below. The remake has a narrower torso, more rigid perspective, and simplified geometry, but preserves the main arrangement. `COMPOSITION.json` passes with subject-center deltas 0.0008/0.0014, relative area difference 0.1614, and horizon delta 0.0083. `OPENING_LOCK.json` passes with MAE 1.365, and the video opening visually matches the gate.

5. **Arms/panel pop-in (if cockpit) or subject missing? NO observed.** This is not a cockpit. The merchant's turban, red torso, and cart remain visible throughout the sampled sequence, including the last frame. The cart naturally occludes much of the lower body; no separate subject disappearance or pop-in is evident.

6. **Verdict: PASS.** The supplied clip shows clear world displacement, continuous camera movement, no observed major clipping, and a passing opening lock with reasonable official composition matching.

7. **If FAIL: concrete next fix — not applicable.** No playable changes made. No recording started. PASS applies to the current supplied clip, not to any longer previously reviewed recording or unrecorded continuation.
