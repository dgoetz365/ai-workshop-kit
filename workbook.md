# Learner workbook

Use the fictional bicycle repair shop in [scenarios.md](scenarios.md). Work with a partner if possible. Your task is to design something that helps a person finish useful work and makes its limits visible.

## Exercise 1: Name the task

Choose one scenario. Fill in these sentences before choosing a tool:

1. The person using this is ______.
2. They need to ______.
3. Today, the difficult or repetitive part is ______.
4. The authoritative information is ______.
5. A successful result would be observable as ______.
6. An incorrect action could cause ______.

Replace goals such as “use AI” or “make it faster” with an observable task. For example: “A coordinator can answer a repair-status question using the current ticket and identify when the completion date is unknown.” Do not invent a percentage improvement.

## Exercise 2: Choose an approach

Compare three approaches for the same task:

| Approach | What it is good at | What you must account for |
| --- | --- | --- |
| Deterministic automation | Applying explicit rules consistently | Rules, exceptions and failure recovery |
| AI assistant | Interpreting varied requests and drafting explanations | Evidence, incorrect answers and review |
| Application | Maintaining shared state and coordinating users | Permissions, concurrent edits and usability |

Choose one approach or a combination. Explain what each component does. A model does not have to make every decision. An application can use an assistant for a bounded task.

Record one alternative you rejected and the condition under which you would reconsider it. There can be more than one reasonable answer.

## Exercise 3: Design the workflow

Draw or write the path:

```text
User request -> obtain evidence -> perform a bounded operation -> review -> result
                         |                    |
                  evidence missing     dependency fails
                         |                    |
                    explain limit       preserve work and retry safely
```

For each step, write its input, output and owner. Identify which actions read information and which change shared state. For a write, decide what happens if the same request is repeated or the record changed after it was read.

Answer:

- Where does the displayed fact come from?
- What happens if two records match the request?
- What is the system forbidden to claim without evidence?
- What does a person review before a consequential action?
- What work remains intact after an error?

## Exercise 4: Test the unhappy path

Write four acceptance scenarios. Use this structure:

```text
Given: the record, permissions and dependency state
When: the person performs one concrete action
Then: the visible result and any allowed state change
And: the change or claim that must not happen
```

Required cases:

1. A straightforward request with current, unambiguous evidence.
2. A missing or conflicting record.
3. An external dependency fails after the person has entered useful work.
4. The same action is submitted twice, or another person edits the record first.

For scenario A, a ticket without an estimated completion date must not produce a promised pickup date. For scenario C, the second reservation must not exceed available inventory even if both people saw availability earlier.

## Exercise 5: Teach back

In two minutes, explain the problem, your approach, one tradeoff, one failure case and how a colleague would verify it. Your partner should be able to repeat the main limitation in their own words.

Use [rubric.md](rubric.md) to identify one strength and one revision. Revise the design before adding features.
