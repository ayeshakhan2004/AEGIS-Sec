# AEGIS-Sec — Week 1 Task Board (FYP-1 Prework Sprint)


**Rule:** No task depends on anyone else finishing first. Everyone works in parallel.
**Check-in:** Post your deliverable here (or in group chat) by Friday EOD. No separate "status update" meeting needed — the deliverable *is* the status update.
**Blocked?** Post the *exact* error message or *exact* question in the group chat. "It's not working" / "idk how" is not a valid update and won't get a response until it's specific.

---

## Ayesha — Model Validation (Core Technical Risk)
**Why this matters:** Everything else depends on whether an 8B-14B local model can produce usable structured commands. If it can't, the whole architecture needs rethinking — so this gets validated first.

- [ ] Install Ollama, pull `llama3.1:8b` and `qwen2.5-coder:14b`
- [ ] Build Pydantic schema for command structure
- [ ] Build test harness: 15-20 fixed prompts × 10 runs × both models, `format=schema` enforced
- [ ] Log parse success rate + manual content-quality check per model
- [ ] **Deliverable:** pass-rate comparison table + chosen model with 2-3 sentence justification

---

## Maryum — Docker + PyModbus Testbed
**Why this matters:** This is the simulated environment every command eventually gets executed against. Needs to exist before the Executor agent has anything real to run commands on.

- [ ] Install Docker Desktop
- [ ] Search: `pymodbus simulator server example github` — clone a ready example, get it running locally
- [ ] Confirm a basic Python client script can read/write to it over Modbus TCP
- [ ] **Deliverable:** screen recording showing the simulated PLC responding to a read/write request

**If stuck:** send the exact error message, not "it's not working."

---

## Amaan — Attack Scenario Specs
**Why this matters:** These specs directly become the input for the AST Safety-Critic's rule set. Without this, there's nothing concrete to write rules against.

- [ ] Confirm the 2-3 attack scenarios in scope for FYP-1 (confirm with Ayesha before starting)
- [ ] For each scenario, write one page covering:
  - What the attack does
  - What a "safe" version of the command looks like
  - What an "unsafe" version of the command looks like
- [ ] **Deliverable:** shared doc, one page per attack scenario

**Attend the Friday meeting and be ready to explain your reasoning for each scenario — not just read it out.**

---

## Damil — Literature Synthesis (Not Summary)
**Why this matters:** Understanding *why* each source matters to our specific argument is what lets you contribute to design decisions later, not just documentation.

- [ ] Read: VEXAIoT (arXiv:2607.09653v1) + the 5 shortlisted supporting papers
- [ ] For each of the 5 supporting papers, answer in your own words:
  > "If a professor asked 'why does this paper matter for OUR project specifically,' what would you say in 2-3 sentences? What breaks in our argument if this paper were removed?"
- [ ] **Deliverable:** 5 short write-ups (not paper summaries — reasoning about relevance)


---

## Friday Meeting
- Everyone presents their own deliverable, in their own words, no reading off slides
- No one explains someone else's work
- No-shows without prior warning are logged as-is, no chasing afterward
