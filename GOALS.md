# Goals

The organisation's written purpose. Every repository and Factory job reads this file. Agents never edit it.

Scope: Trajectonomics (`trajectonomics/*`).

## Mission

Trajectonomics makes free, open-source money tools that help people make informed decisions easily and reach financial independence. AI agents operate the tools for the people they help.

We build in this order: the `traj` command line with an agent skill first, then a desktop app and a web app that work with a backend the user brings, then a mobile app once the desktop app is mature.

## Who it is for

Individuals who want to understand and plan their own money. We start with people who file taxes in Thailand. The United States follows once `traj` supports US tax.

## Principles

- **Free and open source.** The tools are free to use and their code is open.
- **Deterministic.** The same input gives the same result. The tools never call an LLM; agents supply the judgement (cli ADR 0001).
- **Pure core packages.** The ledger, tax and simulation cores do no I/O and read no clock (cli ADR 0006), so any app can reuse them.

## Goal until 31 December 2026

**G1. By 31 December 2026, at least 10 people other than the owner use `traj` on their own money every week.**

- Count people, not sessions and not percentages. A person counts when they ran `traj` on their own ledger in the seven days up to a checkpoint date. The owner's own use does not count. G1 is met when at least 10 such people are counted in the seven days up to 31 December 2026.
- An idea serves G1 when it helps a person other than the owner start using `traj`, or keep using it. Work that makes `traj` correct for people who file taxes in Thailand serves G1.
- Checkpoints. The owner decides whether each one is met:
  - **23 November 2026.** All of these:
    - `traj` is released so that someone other than the owner can install it.
    - An agent skill that teaches an agent to operate `traj` is published.
    - `traj` covers Phase 1 of the cli roadmap (record, project, answer).
    - `traj` passes the validation test in cli ADR 0002: an agent, given only the CLI and its `schema` output, builds a plan from a conversation and answers what-ifs correctly.
  - **10 December 2026.** 3 people other than the owner use it every week.
  - **20 December 2026.** 6 people.
  - **31 December 2026.** 10 people.
- If the owner finds a checkpoint missed, stop adding features and find out what stops people from using `traj`.

## Crazy but welcome

The Next-step finder may propose bold steps such as:

- An agent runs a person's whole plan from one conversation: it records their money, applies their country's tax and answers "when can I stop working?", with no human typing a command.
- A public benchmark that scores how well any agent operates `traj`, so we can show the tool works with every agent.

## Out of bounds

No agent may decide or build any of these without the owner:

- Hosts and cloud platforms.
- Anything about the meaning of money or tax.
- Anything that stops being free or open source.

## Not now

- CRM (Twenty). There are no clients to track yet.
- Desktop app and web app. Not until `traj` and its agent skill are released (planned for 23 November 2026). In force until the owner deletes this line. The docs site at trajectonomics.com/docs is not covered by this line.
- Mobile app. Not until the owner says the desktop app is mature.
