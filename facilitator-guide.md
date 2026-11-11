# Facilitator guide

## Prepare

Read the workbook and select two scenarios suitable for the audience. Keep all examples fictional. Ask participants to avoid pasting actual workplace data into a model or shared document. Prepare a local or printed copy so the session is usable without network access.

If using a companion application, start it and rehearse the exact path before the session. Check both a successful result and a failure result. A running server or a successful model download is not evidence that the demonstration works.

## Facilitate the 60-minute session

**First 10 minutes:** Ask participants what the user needs to finish. When someone starts with a tool name, return to the task and source of truth. Accept different approaches when the reasoning is sound.

**Minutes 10–25:** Compare automation, assistants and applications. For the repair question, language interpretation can help, while ticket facts still come from a structured source. For duplicate reservation approval, the important safeguard belongs in a transaction rather than in a model instruction.

**Minutes 25–40:** Ask pairs to draw inputs, outputs and state changes. Challenge one missing assumption: an ambiguous record, a stale browser, an unavailable dependency or an action submitted twice. Do not ask them to solve every enterprise deployment concern in one workshop.

**Minutes 40–50:** Swap acceptance scenarios. A partner should be able to predict what appears on screen and what changes in storage. Replace “handles errors gracefully” with a concrete outcome, such as “shows lookup unavailable and preserves the unsent draft.”

**Final 10 minutes:** Run teach-backs. Use the rubric for a short discussion. Each pair revises one weak point. Collect feedback about unclear instructions; do not present workshop scores as measured business impact.

## Discussion guidance

- Scenario A can use a bounded assistant with a deterministic lookup. Evidence must remain distinct from a draft. Unknown dates stay unknown.
- Scenario B is usually a deterministic synchronization task. Good answers define field ownership, validation, preview and atomic changes. A model may help explain a diff, but should not decide silently which source record to overwrite.
- Scenario C needs persistent shared state and a concurrency rule. An approval must check current capacity, not trust the earlier screen.
- Scenario D tests whether the product's states and recovery path are understandable. A guide cannot compensate for contradictory behavior.

These are reference considerations, not a single mandatory architecture. Reward a clearly stated alternative and its tradeoffs.

## Recover when the live demonstration fails

Say what failed without inventing a cause. Switch to [demo-script.md](demo-script.md) and the static fictional records. Ask participants what the product should display in this exact situation. Continue the learning task rather than spending the session reinstalling software or repeatedly signing in.

## Adapt the format

- 30 minutes: use one scenario; frame, choose, test one failure, then teach back.
- 90 minutes: add a paired implementation exercise with the companion software and a second review cycle.
- Mixed experience: pair a domain expert with a builder, and rotate who explains the design.
- Independent study: write responses in the workbook and use the discussion guidance after your first attempt.

After delivery, record what participants found confusing and revise the kit. Attendance is not proof of understanding; use the teach-back and ability to execute a recovery step as observable learning evidence.
