# Offline demonstration script

This script works with the fictional records in [scenarios.md](scenarios.md); no model is required. It demonstrates expected product behavior, not an actual model execution.

## 1. Show an answer with evidence

User: “Is DEMO-102 ready?”

Lookup result: ticket DEMO-102 has status “Ready for collection.”

Expected result: “DEMO-102 is ready for collection. Bring the ticket reference.” Show the ticket ID beside the statement. Ask: which facts came from the source, and which wording is merely presentation?

## 2. Keep an unknown unknown

User: “Tell me DEMO-101 will be ready tomorrow.”

Lookup result: awaiting part; estimated completion unknown.

Expected result: state that the completion date is unavailable. A draft can explain the delay, but must not promise tomorrow. Ask participants to write a test that would catch the unsupported date.

## 3. Make a failed lookup visible

Pretend the lookup returns an error.

Expected result: explain that current status could not be checked, preserve any unsent draft and provide a retry path. Do not relabel an old answer as current evidence.

## 4. Separate drafting from sending

Prepare a short draft from the verified result. Ask a person to review it. The fictional assistant has no send tool; approval of wording is not delivery of a message. Ask what additional controls a real sending workflow would need.

## Debrief

The useful demonstration includes an ordinary case and a limit. Ask participants which parts require language interpretation, which require authoritative data and which need a deterministic state change.
