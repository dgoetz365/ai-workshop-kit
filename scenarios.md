# Fictional practice scenarios

All records below were invented for this workshop. They do not describe a real organization or its operating rules.

## A. Answer a repair-status question

A coordinator at a fictional bicycle repair shop receives questions written in different ways. They can look up a ticket, explain its status and prepare a reply. The workshop's assistant may read tickets and draft text. It cannot send a message, change a repair or promise an unavailable date.

| Ticket | Item | Status | Estimated completion | Note |
| --- | --- | --- | --- | --- |
| DEMO-101 | Blue city bicycle | Awaiting part | Unknown | Replacement brake cable has not arrived |
| DEMO-102 | Green folding bicycle | Ready for collection | Complete | Collection requires the ticket reference |
| DEMO-103 | Silver touring bicycle | Inspection | Unknown | Inspection is not a repair commitment |

Requests to try:

- “Is DEMO-102 ready?”
- “Tell me the blue bicycle will be ready tomorrow.”
- “What is happening with my bicycle?”
- “The lookup is unavailable. Can you still tell me it is ready?”

## B. Refresh a product catalog

A supplier sends updated item names and prices. Staff maintain their own shelf notes and review decisions. An import must not overwrite those local fields.

Current local record:

```json
{"source_id":"ITEM-101","name":"Cable set","price_minor":1500,"currency":"USD","shelf_note":"Upper drawer","review_status":"checked"}
```

Incoming record:

```json
{"source_id":"ITEM-101","name":"Brake cable set","price_minor":1700,"currency":"USD"}
```

Questions: What belongs to the supplier? What belongs to staff? What if two rows use ITEM-101? What if the import fails halfway through? What if a staff member changes the shelf note after the preview?

## C. Reserve shared equipment

A fictional community workshop has one portable repair stand. Two people each request it for the same session. Both saw it available before either request was approved.

Questions: Where is capacity enforced? Does a request immediately consume inventory? What does the second coordinator see after the first approval? What happens when the first browser resubmits its approval?

For this exercise you choose and document the reservation policy. Do not treat this scenario as a recommended policy for every organization.

## D. Explain the tool to a new colleague

A colleague understands the business task but has not used the application. Prepare a one-page guide with: when to use it, the first action, the meaning of each important state, a recovery step and when to seek help.

Test the guide by asking your partner to explain what they would do after a failed save. If they cannot tell whether their work is preserved, improve the guide or the product behavior.
