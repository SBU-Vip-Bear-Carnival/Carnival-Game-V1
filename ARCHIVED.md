# 🗄 This is an archive

**Version 1 of the VIP BEAR accessible carnival game — delivered to the
Children's Center at UCP of Long Island in March 2026.**

Nothing here is under development. It is kept as the historical record of what
was built, by whom, and what it taught us.

👉 **Active work lives in [Carnival-Game](https://github.com/SBU-Vip-Bear-Carnival/Carnival-Game).**

---

## Where this code came from

V1 was developed at `ssylviawolf-0/CARNIVALGAME-SOFTWARE`, on a team member's
personal GitHub account. It is **MIT licensed** and the copyright is held by its
original author — see [`LICENSE`](LICENSE), which travels with this copy
unchanged.

This organization's copy exists because the original sits on an account that
belongs to a student who has since left the team. Copying it here does not take
it over; it makes sure the team still has it when that account eventually goes
quiet.

**Everyone who wrote it, by commit count:**

| Contributor |
|---|
| ssylviawolf-0 |
| lionel509 |
| Blaze91827 |
| AldeyBrutus |
| KellyZhao06 |
| Paco N |

---

## ⚠ Three branches were rescued on the way in

When this archive was taken on **2026-09-02**, two branches that existed on the
original repo had already been deleted from it, and their work was seconds from
being lost for good — it survived only as unreferenced objects in one person's
local clone.

Recovered and preserved here under `recovered/`:

| Branch | Commit | What it is |
|---|---|---|
| `recovered/led-patterns` | `df412dc` | 116 lines of new LED patterns (2026-01-30) |
| `recovered/just-tracks-test` | `d374a16` | a track-only test sketch (2026-02-25) |
| `recovered/readme-and-gitignore` | `eafa33b` | the March repo reorganisation (2026-03-24) |

If you are wondering why V2 bothers with an organization account, protected
branches and CI — **this is why.** Work disappeared from a live repository and
nobody noticed.

The odd branch names are preserved deliberately too. `dummy_main` and
`dummy_cleanup` exist because someone wanted a safe place to experiment and did
not know that a branch already is one. That is a documentation failure, not a
personal one, and it is the reason V2 ships a
[git walkthrough](https://github.com/SBU-Vip-Bear-Carnival/Carnival-Game/blob/main/docs/GIT-WORKFLOW.md)
written for people who have never used git.

---

## Known state at the time of archiving

- **`main` has not compiled since 2026-05-07.** An enum in the audio code is
  missing a comma. Nothing checked, so nobody knew for four months. The fix is
  carried into V2's `audio.h`.
- **No pinned library or board versions** — six contributors, six toolchains.
- **All configuration in one `config.h`**, which people edited for their own
  bench and then committed, repeatedly overwriting the cabinet's real wiring.
  V2 splits this into a committed `pins.h` plus a gitignored `pins.local.h`.

## What V1 taught us, physically

These came from watching children actually play it on handover day:

- Printed pressure plates in **PLA were too stiff to step on**. V2 uses TPU.
- **Screws stripped out of printed parts.**
- **Some buttons were not reachable** from a wheelchair. Design reviews did not
  catch this; watching people play did.
- **Hot glue does not survive motor vibration**, and no adhesive fixes a track
  that is not flat to begin with.
