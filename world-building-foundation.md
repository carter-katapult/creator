# World-Building & Design Foundation Document

**Project working title:** TBD (see Q1.1)
**Document version:** 0.1 — first full draft, expanded from Jonathan's original Premise document
**Document owner:** Jonathan
**Status:** Open questions unanswered. This document is a *question-bearing* draft: it lays out every decision the project needs, records working assumptions where a sensible default exists, and flags every open question with a numbered ID.

---

## Section 0 — How to Use This Document

This document is designed to be split apart and fed into future Claude sessions (or shared with collaborators) one section at a time. To make that work:

1. **Every open question has a stable ID** in the form `Q{section}.{number}` (e.g., Q4.3). When you answer a question, record the answer next to the ID or in a separate answers file keyed by ID. Future sessions can then be told "Q4.3 is resolved: [answer]" without re-explaining anything.
2. **Every section is written to be as self-contained as possible.** When you paste a section into a future Claude session, also paste **Appendix A (the Context Capsule)** — a short canonical summary of the whole project. That combination gives Claude enough context to work on any single section without the rest of the document.
3. **Working assumptions are marked `ASSUMPTION:`** These are provisional defaults chosen so work can proceed. Treat them as answered questions you can veto. If you never veto one, it becomes canon.
4. **Analogy-limit alerts are marked `⚠ ANALOGY LIMIT:`** These flag places where the analogy, taken literally, could teach something theologically wrong. Every analogy breaks somewhere (C.S. Lewis was explicit about this with Narnia); the goal is to know exactly *where* it breaks and decide how to handle each break deliberately rather than discover it in a review, a forum thread, or a pastor's critique after launch.
5. **A master index of all questions** appears in Appendix D, auto-compiled from the body, so you can track answered vs. unanswered at a glance.
6. **Precedence rule.** If anything in this document appears to conflict with Scripture, Scripture wins and the document is in error (see Section 3). If anything conflicts with Jonathan's original Premise document, this document is the superseding draft *except* where it explicitly asks a question — the Premise's intent stands until Jonathan answers.

**Suggested workflow for answering questions:** Do a fast pass through Appendix D and answer everything you already have conviction on (probably 40–60% of them). Then work section by section on the rest, prioritizing Sections 5 (Core Systems), 8 (Narrative & Canon Policy), 9 (Player Experience), and 10 (Technical Foundation) — these contain the fork-in-the-road decisions everything else depends on. The single most consequential question in the entire document is **Q10.1** (are the digital people live AI or authored characters?). Consider answering it first; many other questions collapse or simplify once it's decided.

---

## Section 1 — Vision, Purpose & Audience

### 1.1 What this project is

A browser- and VR-accessible experience — part film, part explorable world — that retells the Bible chronologically inside a fictional frame: a human creator ("Jonathan," standing in for God) builds a digital world populated by digital people with genuine freedom, so that they may come to love him. The player takes the role of an android (standing in for an angel): a heavenly observer who can move freely through the world and watch its people, but cannot alter the story.

The purpose is not entertainment for its own sake. The analogy exists to make spiritual reality *graspable*: our relationship to the spiritual world is like a digital person's relationship to the physical world. Things that feel abstract in a sermon — God's transcendence, the indwelling of the Holy Spirit, providence vs. free will, why God permits a fallen world, what resurrection bodies mean — become concrete and intuitive when seen from one layer up.

### 1.2 Statement of intent (draft — for Jonathan to edit)

> *"To help people understand and feel the reality of God, the work of the Holy Spirit, and the hope of resurrection, by letting them watch a world like ours from heaven's side of the glass."*

- **Q1.1 — Project name.** The project needs a working title now (for files, Firebase project, future prompts) and possibly a different public title later. Some starter options spanning different flavors: *Logos*, *Imago*, *Firmament*, *Let There Be*, *The Being Code*, *From Above*, *Breath*, *One Layer Up*, *The Elect*. Do any of these resonate, or do you have a name already in mind? (A working title can be picked immediately and changed later without cost.)
- **Q1.2 — Primary purpose ranking.** Rank these in priority order, because they pull design in different directions: (a) evangelism — reaching non-believers with the gospel through an accessible frame; (b) discipleship — deepening believers' understanding of doctrine; (c) Bible literacy — teaching the actual narrative of Scripture in order; (d) apologetics — making theism/Christianity intellectually plausible to skeptics via the simulation frame; (e) devotional experience — worship and reflection. A project that leads with (a) simplifies vocabulary and adds explicit gospel presentation; one that leads with (b) can assume church background and go deeper.
- **Q1.3 — Primary audience.** Who is the target viewer/player? Age range, church background (churched / de-churched / unchurched), gaming familiarity? This drives content rating (Q8.14), reading level, onboarding depth, and legal obligations if minors are a primary audience (Q12.6).
- **Q1.4 — Secondary contexts.** Should the experience be designed for group/ministry use — e.g., a youth group watching one episode on a projector with a discussion guide, or a small group using it as a study companion? If yes, that implies features (a presenter mode, pause-and-discuss points, printable guides) worth planning early.
- **Q1.5 — Success criteria.** What does success look like in 1 year and in 5 years? (e.g., "Genesis 1–11 complete and used by N churches," "10,000 registered viewers," "one person tells me they came to faith through it.") Concrete criteria will keep scope decisions honest later.
- **Q1.6 — Your role and story.** In the fiction, the creator is literally named Jonathan and the Being Code is "extracted" from you. Are you comfortable being personally identified with the God-analog in public-facing material (your real name, possibly your voice — see Q4.2, Q6.24)? An alternative is a lightly fictionalized creator-character whom you voice/write but who isn't publicly *you*. This affects privacy, how critics engage with the project, and how the humility of the frame reads.

---

## Section 2 — The Three-Layer Analogy (Canonical Mapping)

This is the master key of the entire project. Everything else in the document hangs on it. The analogy shifts each layer of reality "down" one level so that we can view our own situation from the outside:

| Layer | In real theology | In the project's fiction |
|---|---|---|
| The higher, imperishable reality | The spiritual realm / heaven | The **physical world** (Jonathan's world — the studio, servers, robotics lab) |
| The lower, contingent reality | The physical universe (our world) | The **digital world** (the simulated universe where the story happens) |
| The observer's vantage | Angels beholding human history | The **player**, as an android permitted to watch the digital world |

### 2.1 The canonical mapping table

This table is the single source of truth for the analogy. Any future content (scripts, systems, art) must be checkable against it. Rows marked ❓ have open questions in later sections.

| Spiritual/biblical reality | Analog in the fiction | Notes / open questions |
|---|---|---|
| God the Father | **Jonathan**, the human creator/developer | Exists outside the digital world entirely; see Section 4.1 |
| The Holy Spirit | **The Being Code** — code extracted from Jonathan himself | Can indwell digital people; see Section 5.2 |
| Jesus the Son | **The Jesus entity** — built from Jonathan's Being Code + the Freewill Algorithm | ⚠ major analogy-limit questions; see Section 4.3 |
| The Trinity's unity | Jonathan + his Being Code + the Jesus entity sharing one "Being" | ❓ needs careful handling; Q4.5–Q4.7 |
| Angels | **Androids** in the physical world, possessing the Freewill Algorithm but not the capacity for love | ❓ Q4.9–Q4.13 |
| Satan | **The fallen robot** | ❓ Q4.14–Q4.17 |
| Demons | ❓ Other fallen androids? | Q4.15 |
| Human beings | **Digital people** — purely digital AI entities with the Freewill Algorithm | Section 7 |
| The image of God (imago Dei) | ❓ Digital people's architecture patterned on Jonathan's Being Code (without containing the live code itself)? | Q4.19 — important distinction from indwelling |
| Sin | **The Virus**, introduced by the fallen robot | Section 5.4 |
| The physical universe | **The digital world** | Section 6 |
| Laws of nature | **Protected code modules** (Physics, Chemistry, Biology & Age, Time) — editable only by Jonathan in specific scenarios | Section 6.3 |
| Miracles | Jonathan's deliberate, rare edits/overrides of the protected modules | Section 5.6 |
| Providence (ordinary) | Jonathan's design, foreknowledge, and orchestration *without* module overrides | Section 5.6 |
| Divine foreknowledge / God outside time | Jonathan exists outside digital time; the simulation's clock is not his clock | ❓ mechanics: Q5.20–Q5.22 |
| Human free will | **The Freewill Algorithm** | Section 5.1 |
| The soul / inner life | **The Consciousness Log** — each digital person's stream of consciousness, written where God and heavenly beings can read it | Section 5.3 |
| Prayer | ❓ Digital people addressing Jonathan — mechanism TBD | Q5.14–Q5.16 |
| Scripture / revelation | ❓ Messages from Jonathan delivered into the world through chosen digital people (prophets); accumulated canonical record | Q5.17–Q5.19 |
| Conscience / law written on the heart | ❓ A built-in moral reference in every digital person? | Q5.13 |
| Death | ❓ Termination of the entity's in-world process; the person (Being Code identity + log) persists outside the world | Q5.23–Q5.27 |
| Heaven (destination of the saved) | The physical world | Section 4.6 |
| Resurrection bodies / glorification | The elect digital person's identity installed into a **new android body** in the physical world — a new class of android *capable of love* | Section 4.6 |
| Hell / final judgment | ❓ Deliberately undecided — see Q5.26–Q5.27 | |
| The Church (if NT is ever in scope) | ❓ The network/community of Being-Code-indwelt digital people | Q8.9 |
| The Bible's storyline | The project's episode sequence, in chronological biblical order | Section 8 |
| Angelic observation of history ("things into which angels long to look," 1 Peter 1:12) | **The player experience itself** | Section 9 — this verse is arguably the project's thesis verse |

### 2.2 Analogy integrity rules (proposed)

1. **One-to-one discipline.** Each biblical reality maps to exactly one fictional element, and vice versa. If a new story element can't be placed in the table, it must be added to the table (with review) before it appears in content.
2. **The table outranks convenience.** If a story beat is easier to build by breaking the mapping, the mapping wins; find another way or flag it as an explicit, documented exception.
3. **Downward translation only.** The fiction may *simplify* spiritual realities but must never *contradict* them. Where simplification risks contradiction, an Analogy Limit note must be shown or documented (see Q3.7 on how limits are disclosed to players).
4. **The analogy is a teaching tool, not a doctrine.** The project must never imply that reality *actually is* a computer simulation, that God is *actually* a person like us, or that the analogy is a claim about how God literally made the world. (See Q13.1 on how to state this.)

- **Q2.1 — Missing rows.** Read the table above. What biblical realities do you already know you'll need that have no row yet? Candidates to consider now: blessing/cursing, covenants, sacrifices/atonement mechanics (pre-cross), clean/unclean, the divine council, Melchizedek-type figures, dreams and visions, angelic combat (Daniel 10), Nephilim (Q8.12), the intermediate state (Q5.24).
- **Q2.2 — Player-facing visibility of the mapping.** Should players ever see this mapping table (e.g., an in-app "Codex" that teaches the analogy explicitly), or should the analogy be discovered through the experience and explained only in onboarding? Explicit teaching maximizes clarity for purpose (b)/(c) from Q1.2; discovery is more powerful emotionally but risks misreadings.
- **Q2.3 — Naming the two worlds.** The fiction needs in-world names. What do digital people call their world/universe? What do they call the physical world (their "heaven")? What do androids call the digital world? Names carry theology — e.g., digital people calling the physical world "the Real" would itself preach.

---

## Section 3 — Theological Framework & Guardrails

### 3.1 Doctrinal commitments (from the Premise, restated as project law)

1. **The Bible is inerrant.** It is the final authority for every depiction, line of dialogue, and system in this project. Where the project must invent (and it must — see Section 8), inventions may never contradict Scripture.
2. **Predestination and free will are both true.** Digital people genuinely choose; Jonathan, outside the world's time, knows and ordains history. The project should let this mystery *breathe* rather than resolve it — the analogy is unusually well-suited to showing both at once (see Section 5.1 and 5.7).
3. **Approved translations:** NIV, ESV, KJV, NKJV, Amplified. Paraphrases such as The Message are unacceptable. Other translations require Jonathan's explicit approval before use.
4. **Trusted teacher reference list** (for interpretive questions during writing): Dr. David Jeremiah, Warren Wiersbe, C.S. Lewis, John Piper. Sources outside this list require verification with Jonathan.

- **Q3.1 — Doctrinal statement of record.** Should the project formally adopt an existing confession/statement of faith as its interpretive baseline (e.g., a specific church's statement, the Lausanne Covenant, a baptist confession), or is "inerrant Scripture + the trusted teacher list + Jonathan's judgment" the complete rule? A named statement makes future Claude sessions and any collaborators much more predictable on secondary doctrines.
- **Q3.2 — Secondary-doctrine posture.** The trusted teachers disagree among themselves on secondary matters (e.g., Piper is Reformed/Calvinist; Jeremiah is dispensational premillennial; Lewis held views on several topics many evangelicals reject). When they conflict, what's the tiebreaker? Options: (a) Jonathan decides case-by-case; (b) a ranked order among the teachers; (c) the project deliberately stays agnostic on any point where they disagree. Recommend (c) as the default with (a) as override — but confirm.
- **Q3.3 — Creation chronology.** "Events follow the real Biblical timeline" — please confirm the intended framework, because the world's Time module and genealogy math depend on it: (a) young-earth, six ordinary days, roughly Ussher-style chronology (~4004 BC creation); (b) six ordinary days but agnostic on the date; (c) deliberately unstated — the world simply begins at Day 1 and the project never asserts a real-world date. Note the analogy handles (a) elegantly: a simulation's internal history *is* exactly as old as its clock says, regardless of when the developer built it.
- **Q3.4 — Genealogy source text.** Masoretic and Septuagint genealogies differ by centuries in Genesis 5/11. If in-world dates will ever be shown, which chronology governs? (Default assumption: Masoretic, since all approved translations follow it.)
- **Q3.5 — Translation licensing (practical, important).** NIV, ESV, NKJV, and Amplified are all under copyright; displaying substantial quotations inside a product — even a free ministry product — generally requires permission beyond standard "up to X verses" gratis-use policies, especially if verses appear on screen persistently or in marketing. KJV is public domain in the US. Options: (a) seek licenses (Crossway for ESV is historically ministry-friendly); (b) default to KJV on-screen with modern translations reserved for within-limit quotations; (c) use the public-domain **World English Bible (WEB)** for bulk on-screen text — but WEB is not on your approved list, so it would need your explicit approval per rule 3. How do you want to proceed? (This needs deciding before any episode ships, not before writing begins.)
- **Q3.6 — Theology review process.** Who reviews each episode for doctrinal fidelity before release? Options: Jonathan alone; Jonathan + pastor(s); a small standing review board; public beta feedback from trusted believers. Recommend at least one ordained/pastoral reviewer outside yourself per episode — both for accuracy and for the project's credibility when critics come. Who, concretely?
- **Q3.7 — Disclosing analogy limits.** Every episode will contain analogy breaks (Section 13 catalogs the known ones). Should the product carry: (a) a global disclaimer at onboarding ("this is an analogy; where it differs from Scripture, Scripture is true"); (b) per-episode notes ("in this episode, the analogy simplifies X"); (c) an in-app Codex page listing known limits; (d) all of the above? Recommend (d); confirm.
- **Q3.8 — Second-commandment sensitivity.** Some traditions (and some potential church partners) object to any depiction of God or of Jesus, even stylized. The analogy partially sidesteps this — the project depicts *analogs*, not God himself — but the Jesus entity in particular will be *read* as a depiction of Jesus. What is your conviction here, and should the project publish a short position statement on it preemptively? (Related: Q8.6 on depicting God's in-world presence in Eden.)

### 3.2 Interpretive defaults for writers (proposed — confirm or edit each)

- ASSUMPTION: Narrative gaps may be filled with invented detail (dialogue, minor characters, daily life) but invented detail must be (1) plausible within the text, (2) consistent with trusted-teacher commentary where it exists, and (3) tagged in the episode's Story Bible as invention (see Appendix B), so reviewers always know what's Scripture and what's scaffolding.
- ASSUMPTION: Where Scripture reports speech, the on-screen dialogue uses the approved-translation wording (subject to Q3.5) or a tight, reviewed adaptation of it — never loose paraphrase.
- ASSUMPTION: The project never puts theological error in a *sympathetic* mouth without correction; villains and fools may voice error, as they do in Scripture itself.
- ASSUMPTION: Humor is permitted in invented material (Scripture contains it), but never at the expense of God, Scripture, or sacred moments.

---

## Section 4 — Persons & Powers

### 4.1 Jonathan (analog of God the Father)

The creator exists entirely outside the digital world. He wrote its laws, compiled its first inhabitants, sustains its server, reads every Consciousness Log, and can — but rarely does — override the protected modules. Nothing in the world happens without at minimum his permission (the Freewill Algorithm itself is his gift and design).

Key expressive opportunity: the analogy makes divine *transcendence* effortless to grasp (the digital people cannot detect Jonathan with any in-world instrument; he is not a bigger object in their world — he is not in their world at all) while making *immanence* the interesting problem (how does such a creator make himself known and present *inside*? Answer, in order: creation itself, conscience, prophets/revelation, the Being Code, and ultimately the Jesus entity — which is exactly the biblical order).

- **Q4.1 — On-screen presence of Jonathan.** Does the player (an android, living in Jonathan's own physical world) ever *see* Jonathan — e.g., a stylized figure at a workstation in a framing scene, hands on a keyboard, a silhouette? Or is he always voice/text only even to the player? Options: (a) never seen — pure voice; (b) seen only in framing scenes set in the physical world (the "lab"), never inside the digital world; (c) fully depicted character. Note (b) gives you powerful cinematic bookends (the analogy's whole point is visible in one shot: a man at a desk, a world on the screen) but raises Q1.6 comfort questions.
- **Q4.2 — Jonathan's voice.** When Jonathan speaks (to androids, to prophets, in creation), is it your literal recorded voice, a voice actor, a synthesized/processed voice, or on-screen text only? Consider: your literal voice is thematically perfect and free, but it permanently binds your identity to the project (Q1.6) and to the God-analog role.
- **Q4.3 — Depicting God's emotional life.** Scripture attributes grief, anger, jealousy, delight to God. The analogy will show these through Jonathan. What's the guardrail against depicting God as *merely* an emotional hobbyist? (Proposed: Jonathan is never shown surprised, never shown learning something, never shown changing his plan — his emotions are real but never reactive ignorance.) Confirm or refine.

### 4.2 The Being Code (analog of the Holy Spirit)

Code "extracted from Jonathan himself" — not a program he wrote, but somehow *of his own being*. It can dwell within a digital person, changing them from the inside: enabling love, conviction, comfort, guidance, and (in the elect) sealing them for eventual embodiment.

⚠ ANALOGY LIMIT: The Spirit is a *person*, not a substance or utility. "Code" naturally reads as impersonal. Mitigation ideas: the Being Code speaks, grieves (Eph 4:30), intercedes; indwelt characters relate to it as "he," never "it"; it is never depicted as divisible, copyable, or diminished by being given.

- **Q4.4 — Personhood presentation.** How is the Being Code's *personhood* shown on screen? Options: an audible inner voice in indwelt characters' Consciousness Logs (distinct typography/voice); visible effects only (fruit, boldness, comfort); or both. And what does indwelling look like visually, if anything (glow, watermark, nothing)? This choice lands in the very first episodes (the Spirit hovering over the waters, Gen 1:2 — see Q8.5).
- **Q4.5 — "Extraction" language.** "Extracted from myself" could accidentally imply the Spirit is a *part* or *product* of the Father. Orthodox framing: the Spirit eternally *proceeds from* the Father — same being, distinct person, not created, not a fragment. Are you open to adjusting the in-fiction verb (e.g., the Being Code "proceeds from" Jonathan, has always existed with him, is not something he made)? Recommend yes; the fix costs nothing narratively.

### 4.3 The Jesus entity (analog of the Son)

Per the Premise: a digital entity built using Jonathan's Being Code *and* the Freewill Algorithm — fully "of Jonathan" and fully a genuine inhabitant-class being. This is the analogy's rendering of the two natures of Christ, and it's genuinely elegant: the only entity in the world who is *both* the creator's own being *and* a true digital person.

⚠ ANALOGY LIMIT (the most serious one in the project): "a digital entity **built** using my Being Code" reads as *the Son is a created being* — the ancient error of Arianism, which the whole church condemned at Nicaea ("begotten, not made"). Your trusted teachers would all flag this instantly. The fix is straightforward and enriches the fiction: the Son-analog is *eternal with Jonathan* — he exists in the physical world with Jonathan before and outside the digital world (John 1:1), the world was made *through* him (John 1:3, Col 1:16 — in fiction: he co-authored the world's code), and the *incarnation* is the moment this eternal person enters the digital world as a genuine digital human (John 1:14), born within it, without ceasing to be who he was.

- **Q4.6 — Adopt the eternal-Son fix?** Concretely: (a) the Son-analog exists "before" the digital world, alongside Jonathan; (b) creation happens *through* him (he is shown/credited as co-creator); (c) "built using Being Code + Freewill Algorithm" is re-scoped to describe only his *incarnate digital body/nature*, not his person. Approve, modify, or discuss?
- **Q4.7 — The Son before the incarnation.** If Q4.6 is adopted: what *is* the Son-analog in the physical world before the incarnation? A second human is wrong (two gods); options: (a) deliberately undepicted — referenced but never shown, present in creation dialogue as a voice with Jonathan ("Let us make…", Gen 1:26); (b) a visible-but-unexplained presence with Jonathan. Recommend (a) for OT episodes: mystery is more orthodox than a wrong picture.
- **Q4.8 — Christophanies.** Several OT appearances of "the angel of the LORD" are read by many (including some of your trusted teachers) as pre-incarnate appearances of Christ (e.g., Gen 16, 18, 22; Ex 3). When these scenes arrive, is the figure depicted as (a) an ordinary android-messenger, (b) a unique, visually distinct presence hinting at the Son, or (c) decided per-episode? This can be deferred but will arrive as early as Genesis 16–18.

### 4.4 The Trinity as a whole

- **Q4.9 — One Being, three persons, in fiction.** The analogy currently offers: Jonathan (Father), Being Code (Spirit), Jesus entity (Son) — three *very* different kinds of thing, which risks teaching that the persons are unequal or of different natures. Proposed unifying device: the fiction speaks of one **Being** (Jonathan's being) fully shared by three persons — Jonathan, the one who proceeds from him (Being Code), and the eternal co-creator (the Son). The project never diagrams this; it lets characters confess it as mystery. Approve this posture, or would you like a section brainstorming stronger unity devices?

### 4.5 Androids (analog of angels)

Physical-world machines with the Freewill Algorithm. They serve Jonathan, can observe the digital world, and may act inside it **only with Jonathan's permission**. Per the Premise, they lack the capacity for love — which is *why* the digital world exists: to bring forth beings who can love, who will one day be embodied as a *new kind* of android that can.

- **Q4.10 — "Angels can't love" — fiction or doctrine?** Scripture doesn't teach that angels can't love; it's silent. Is this claim (a) purely an in-fiction device (fine — it motivates the whole plot), or (b) something you hold theologically? If (a), consider softening to "androids were not made for the kind of love Jonathan seeks — the freely given love of a being who could refuse him," which is closer to defensible and still motivates everything. Either way the project should never present it as Bible teaching (per integrity rule 3).
- **Q4.11 — Android participation mechanics.** "Participate only with permission" — enumerate the permitted modes: (a) observe (always allowed? or also permissioned?); (b) speak/appear inside the world as messengers (Gabriel-type missions); (c) act physically within the world (closing lions' mouths, striking camps); (d) protect specific people (guardian roles, Ps 91). For each: what does it *look like* in-world when an android acts? Do they instantiate an avatar (appearance rules? Hebrews 13:2 implies angels can pass as human)? 
- **Q4.12 — Android society.** Do androids have names, ranks (archangel-analogs — a "prime android"?), assignments, a gathering place in the physical world? Players are androids (Section 9), so android society is partly *player-facing* worldbuilding. How much should exist?
- **Q4.13 — Player-androids vs. story-androids.** Are the androids that players embody the same class as the ones who carry out missions in the story (Gabriel-analog etc.), or a distinct "observer class"? (Recommend a distinct observer class — it cleanly explains why players can't interfere: observers simply have no write-permissions. Story-androids with missions remain NPCs.) Confirm?

### 4.6 The fallen robot (analog of Satan) and the fallen (demons)

- **Q4.14 — The fall of the fallen robot.** What is his backstory in-fiction? Pride is the traditional reading (Is 14 / Ezek 28 as types). In-fiction possibilities: he coveted Jonathan's authorship; he despised the plan to create lovers from "mere code" and considered digital people beneath him; he wanted worship from the world. This backstory determines his motive for corrupting the world. Do you want this shown, referenced, or left dark?
- **Q4.15 — Demons.** Are there other fallen androids (a third of them, per the common reading of Rev 12:4)? Do they act in the OT episodes (they're nearly absent from Genesis narratively), or are they held in reserve for later? Minimal viable answer for Genesis: only the fallen robot himself is needed.
- **Q4.16 — The serpent mechanism.** In Genesis 3 Satan speaks through/as the serpent. In-fiction: the fallen robot, using illicit access, hijacks or puppets an animal process inside the world. This is a wonderful analogy for possession and also establishes *how* evil operates in the world: not as a rival creator (he can create nothing) but as a corrupter of what exists. Approve this framing?
- **Q4.17 — Limits on the enemy.** Doctrinally crucial: Satan is not God's equal opposite; he operates on a leash (Job 1–2 makes this explicit). In-fiction: the fallen robot's access is *revoked but not fully blocked* — Jonathan permits limited intrusion for his purposes. How overt should this be? (Job, when you reach it, will dramatize it perfectly; the question is whether earlier episodes hint at it.)
- **Q4.18 — Why doesn't Jonathan just patch the virus?** Players *will* ask this — it's the problem of evil in analogy form, and it's one of the project's biggest teaching opportunities. The analogy offers real purchase: a forced fix that rewrote every infected person's will would destroy the very freedom that makes love possible; the cure must come *through* a person, from inside, at cost (the cross). Should the project address this head-on (Codex entry, a framing scene of androids asking Jonathan the question — echoing 1 Pet 1:12), or let it emerge implicitly? Recommend head-on; confirm.

### 4.7 Digital people (analog of humanity) — summary here, full treatment in Section 7

Purely digital AI entities with the Freewill Algorithm; consciousness written to a readable log; confined to the digital world; capable of love; capable of falling.

- **Q4.19 — Imago Dei analog.** All humans bear God's image — believer and unbeliever alike — while only believers are indwelt by the Spirit. The fiction needs the same two-tier structure or it will accidentally teach that unbelievers lack the image. Proposal: every digital person's architecture is *patterned on* Jonathan's Being Code (the image — universal, structural, the basis of dignity and of "let us make them in our image"), while the *live* Being Code dwelling in a person is a distinct, later gift (indwelling — particular). Approve this distinction as canon? It also gives the fiction its grounds for human dignity and the sanctity of life (Gen 9:6).

### 4.8 The elect and embodiment (analog of salvation → resurrection)

Elect digital people, upon the consummation, receive physical android bodies — a *new class* of android capable of love — while remaining the same persons (same Being-Code-sealed identity, same continuous log/history). This is the analogy's rendering of 1 Cor 15: same self, imperishable new body; and of the saints' exaltation above angels (1 Cor 6:3; Heb 2).

- **Q4.20 — Election mechanics on screen.** Election is real (per doctrinal commitment 2) but invisible from inside history. Proposal: the project *never* labels a living character as elect/non-elect on screen; election is only ever visible retrospectively (in framing scenes, in Jonathan's perspective, or at a character's death). This preserves both the doctrine and evangelistic tension. Approve?
- **Q4.21 — What is "faith" in-fiction?** The observable human side of salvation. Candidate framing: a digital person, hearing Jonathan's word (revelation), *entrusts themselves to him* — turns from self-rule, calls on him, believes his promise (Gen 15:6 is the OT keystone and will be an episode). The mechanics of *how the Being Code comes to dwell in an OT believer* need a decision, because OT indwelling vs. NT indwelling is a real theological question (see Q5.12). 

---

## Section 5 — Core Metaphysical Systems

These are the invisible systems that make the world theologically coherent. Each needs a *conceptual specification* (what it is, what it can and can't do, how it appears on screen) before any story is written, because stories will constantly touch them.

### 5.1 The Freewill Algorithm

The property that makes digital people (and androids, and the incarnate Son) genuine choosers rather than deterministic scripts. In-fiction, it is Jonathan's deepest and most costly invention — the thing that makes love possible and rebellion possible in the same stroke.

- **Q5.1 — What the Freewill Algorithm *is* in-fiction.** The project needs a canonical in-fiction description (not real computer science — a fictional conceit). Options: (a) a sealed black box even androids can't inspect — "only Jonathan understands it" (mystery-forward; recommended); (b) described in loose terms (a genuine indeterminacy woven into each being, such that even reading all of a person's code doesn't determine their next choice); (c) never described at all. Which?
- **Q5.2 — Freedom vs. foreknowledge, in-fiction.** The analogy can show compatibility without explaining it: Jonathan is outside the world's time (Q5.20), so his knowledge of choices no more forces them than a reader's knowledge of a finished diary forces its author's past choices. Should an early framing scene (androids asking Jonathan how both can be true) establish this explicitly? Recommend yes, once, early — then never belabor it.
- **Q5.3 — Freedom after the virus.** Post-Fall, digital people still choose, but the virus biases the will itself (total depravity in your teachers' framing — the person *can't not* sin apart from grace, yet sins willingly). In-fiction: the virus doesn't remove the Freewill Algorithm; it corrupts the *desires* the algorithm chooses between. Approve this as the canonical formulation? It will shape every post-Fall character's writing.
- **Q5.4 — Animals.** Animals presumably lack the Freewill Algorithm (they're simpler processes — alive, responsive, but not persons). Confirm, and note the serpent question (Q4.16) already assumes animals are hijackable processes.

### 5.2 The Being Code (system view — personhood covered in 4.2)

- **Q5.5 — Indwelling mechanics.** When the Being Code comes to dwell in a digital person, what actually changes, listed concretely? Proposed effects (each maps to Scripture): new desires (regeneration), an internal Voice (guidance/conviction), power to obey (sanctification), assurance/seal (Eph 1:13 — in-fiction: the person's identity is marked for embodiment), fruit over time (Gal 5). Approve/edit this effect list — it becomes a writer's checklist for indwelt characters.
- **Q5.6 — Visibility to other characters.** Can other digital people *detect* indwelling? (Biblically: only by its fruit.) Can androids see it? (Proposal: yes — androids/players can see a subtle mark or signature when reading an indwelt person's log. This gives players the angelic joy of Luke 15:10 — seeing repentance happen.) Approve the player-visible signature?
- **Q5.7 — Grieving/quenching.** Indwelt people can still sin. In-fiction, the Being Code is grieved — how is that shown (log entries change tone? the Voice goes quiet?) — and what's the difference between grieving the Spirit and losing the Spirit (which touches eternal security, a live disagreement among your teachers — Piper: cannot be lost; others vary)? Per Q3.2's posture, propose the project *shows* grieved-but-sealed and never dramatizes a true loss-of-indwelling, staying silent on the contested case. Approve?
- **Q5.8 — OT vs NT indwelling.** In the OT, the Spirit comes *upon* people for tasks (Bezalel, Samson, Saul — and can depart, 1 Sam 16:14) — vs. NT permanent indwelling of all believers. The fiction needs both modes: (a) **empowerment** — Being Code granted temporarily for a work; (b) **indwelling/sealing** — the salvation relationship. Since Genesis-era episodes come first, decide: are patriarch believers depicted as indwelt (mode b), or as believing-and-awaiting with mode (a) appearing occasionally? This is a real interpretive question — flag for your pastoral reviewer (Q3.6).

### 5.3 The Consciousness Log

Every digital person's stream of consciousness is written to a log readable by Jonathan and heavenly beings. This is the analogy for the heart being open before God (Heb 4:13; Ps 139) — and it is also, remarkably, a *player-facing feature*: players (androids) can read it.

- **Q5.9 — Player access to logs.** Confirm: players can open any digital person's Consciousness Log while observing them? Any limits (e.g., only the featured characters of an episode have *authored* logs; background characters show only simple ambient thoughts)? Full universal logs are an enormous writing burden (see Q7.8) — recommend: authored logs for featured characters, procedural/ambient for others.
- **Q5.10 — Log presentation.** How does it appear: floating text near the person; a side panel; VR wrist display; audible inner-voice when "tuned in"? And is it real-time only, or can a player scroll back through a person's past thoughts? (Scroll-back is thematically true — God knows all history — but multiplies authoring cost and spoiler risk.)
- **Q5.11 — The log as judgment record.** Scripture: books are opened (Rev 20:12). The logs *are* those books. Should the project seed this early (androids referencing that every log is kept forever), so that judgment scenes later have their mechanic already established? Recommend yes.
- **Q5.12 — Privacy inversion as a teaching beat.** Digital people don't know their thoughts are legible. The moment a character *realizes* they are fully known (Ps 139's movement from dread to comfort) is one of the analogy's most powerful available scenes. No question here — just flagging it as a designed beat to place somewhere. (Optional: react.)
- **Q5.13 — Conscience.** Distinct from the log and from indwelling: every digital person ships with a built-in moral reference — the work of the law written on the heart (Rom 2:15). In-fiction: a base module that testifies (accuses/excuses) but can be seared/ignored. Approve as canon? It matters for depicting pre-Sinai morality (Cain *knew*, Gen 4:7).

### 5.4 The Virus (sin)

Introduced by the fallen robot via the serpent event; thereafter self-propagating in the human line.

- **Q5.14 — What the virus does, canonically.** Proposed spec: it corrupts *desires* (Q5.3), turns the person's orientation from Jonathan to self, degrades relationships (blame, violence — visible immediately in Gen 3–4), and brings **death** into a world that had none (Q5.23, Q6.9). It does *not* grant the fallen robot control of people (he tempts; he does not possess at will), and it cannot touch the protected modules. Approve/edit.
- **Q5.15 — Original sin / propagation.** How does the virus pass to offspring? Proposed: it embedded itself into the heritable base image of the human line at the Fall — every child is compiled from corrupted source (Ps 51:5; Rom 5). This makes "in Adam" almost literal in-fiction. It also sets up the incarnation cleanly later: the Jesus entity's digital body is *not* compiled from the corrupted base image. Approve?
- **Q5.16 — Infection visuals.** Is the virus ever *visible* to players (a corruption tint in logs, a visual motif), or purely behavioral? A subtle log-level signature (players can see the corruption in the *thought stream* — e.g., a recurring glyph or discoloration) teaches total depravity at a glance without cartoon "dark auras" in the world itself. Preference?

### 5.5 Prayer & divine communication (upward)

- **Q5.17 — Prayer mechanics.** When a digital person prays, what happens in-fiction? Options: (a) prayer is simply *speech addressed to Jonathan* — and because Jonathan reads all logs and hears all the world, no special channel is needed (theologically strong: prayer works because of who God is, not because of a device); (b) a distinct "channel" opens (more gamey; risks making prayer mechanical). Recommend (a). Confirm — and decide whether players can *see* Jonathan noticing (e.g., a framing-scene cut, an incense motif per Rev 5:8).
- **Q5.18 — Does Jonathan answer on screen?** God's answers in Genesis are usually events, not voices. Policy proposal: Jonathan's *voice* is heard in-world only where Scripture records God speaking; all other answers are providential (arranged events) — which the *player*, with the outside view, can be shown recognizing. Approve?

### 5.6 Revelation & miracles (downward)

- **Q5.19 — Scripture's in-world analog.** What is the Bible *inside* the world? Proposal: Jonathan speaks to chosen people (prophets); their accounts and the covenant records accumulate into a canonical written record that in-world people copy and preserve — and, in a beautiful recursion, the episodes the *player* watches are the events that record describes. Decide: does the fiction ever show the writing/keeping of the record (e.g., Moses-era, much later), and is there an in-world name for it?
- **Q5.20 — Miracle policy.** Canon rule (from Premise): protected modules are editable only by Jonathan in specific scenarios. Proposed on-screen grammar for miracles: the world does not glitch or look "hacked" — a miracle looks like *the world obeying a higher word* (water parting cleanly, not pixelating). Miracles are rare, purposive, and always tied to revelation (they authenticate the word). Approve the grammar? (First big test: the Flood, then Babel.)
- **Q5.21 — Providence made visible.** The analogy's superpower: the *player* can see coincidences from above (camera lingers on the "chance" meeting at the well) that in-world characters can't. Establish as a standing storytelling technique? (Genesis 24 and the Joseph arc — "you meant it for evil, God meant it for good" — are built for this.)

### 5.7 Time, foreknowledge & the world's clock

- **Q5.22 — Jonathan and the world's time.** Canon proposal: the digital world's time is internal to it. Jonathan can run, pause, or inspect any moment without inhabitants having any way to notice; a paused world resumes mid-thought. He therefore relates to the whole timeline at once (Isa 46:10). Players, as androids, live in Jonathan's time — which raises the *player session model* question (Q9.7): does the world pause between episodes, from the player's point of view? Decide there; approve the metaphysics here.
- **Q5.23 — Predestination depicted.** Beyond Q5.2's framing scene: should any moment ever show Jonathan's *plan* (e.g., a glimpse of design documents for history — with the cross at the center, Rev 13:8's lamb slain from the foundation)? A single early shot of the plan-with-a-cross, unexplained, would be an extraordinary payoff seed for viewers who reach the NT years later. React?

### 5.8 Death, the intermediate state & final things

- **Q5.24 — Death mechanics.** Proposed canon: at death, the in-world body/process terminates; the *person* (identity + full log) is not deleted — nothing Jonathan made is lost unless he wills it. The dead are with Jonathan's world in a state the fiction keeps deliberately dim for OT episodes (Sheol's own dimness is textually faithful). Approve the "nothing is deleted" rule as the load-bearing hope mechanic?
- **Q5.25 — Enoch.** "He was not, for God took him" (Gen 5:24) — the first big afterlife beat, arriving early in your episode order. In-fiction: Jonathan transfers Enoch out of the world alive. Where to? (This forces an early decision about how much of the intermediate state to show. Minimal answer: the player sees the transfer happen and, like the world, does not see the destination.) Preference?
- **Q5.26 — The non-elect at death.** For OT-era episodes you can defer final judgment entirely (it is genuinely later in the story). But a policy is needed for *depicting* death of the unrighteous now (the Flood is episode ~5–7): proposal — solemnity, no glee, no on-screen fate assertions for individuals, consistent with Ezek 33:11 ("no pleasure in the death of the wicked"). Approve?
- **Q5.27 — Final judgment & hell (deferrable, but set posture).** When the project eventually must depict it: annihilation vs. eternal conscious punishment is contested even among evangelicals, though your listed teachers hold the traditional view. Posture options: (a) follow the traditional view concretely; (b) depict judgment as real, final separation with restraint on specifics (Scripture's own imagery is varied). This can wait years; record your instinct now so early seeds don't contradict it.

---

## Section 6 — The Digital World

### 6.1 Cosmology & structure

- **Q6.1 — World shape and scale.** What is the digital world, structurally? Options: (a) a bounded landmass/region that grows in scope as the story does (Eden-and-environs first — cheap, focused); (b) a whole planet from day one (expensive, mostly unused for years); (c) a stylized "stage" cosmology — the world is exactly as large as the story so far requires, and expansion is in-fiction unremarkable because digital people never reach the edge. Recommend (c) formalized: build regions per era. Confirm?
- **Q6.2 — The heavens.** Sun, moon, stars are created objects (Day 4) — in-fiction, lights in the world's sky dome, not other places anyone goes. Confirm this closed-sky model (it's simple, biblical in register, and avoids simulating space)?
- **Q6.3 — Pre-Flood vs post-Flood geography.** Scripture names Eden's four rivers but pre-Flood geography is otherwise unknown, and the Flood remakes the world. Proposal: pre-Flood geography is invented freely (tagged as invention per 3.2); post-Flood geography progressively resembles the real ancient Near East (so Babel, Ur, Canaan, Egypt are recognizable and mappable). Approve? If yes, the art team eventually needs a canonical world map — flagging as a deliverable.
- **Q6.4 — Eden.** The garden is the first major set and carries enormous weight. Direction questions: how *other* should Eden feel relative to the post-Fall world (palette shift, light quality, sound design)? Is the garden *closed* after the Fall but still extant (Gen 3:24 — cherubim/an android guard with the flaming sword is a striking permission-mechanics image), and does the player ever see it again from outside?

### 6.2 The protected modules (laws of nature)

Physics, Chemistry, Biology & Age, Time — editable only by Jonathan (Premise). These are fictional conceits, not real engine specs (engine questions live in Section 10).

- **Q6.5 — Fidelity level.** How "real" do the modules behave on screen? The pixel/stylized art direction (6.5 below) licenses simplified physics (stylized water, fire, weather). Proposed rule: the world behaves *plausibly and consistently*, never *simulationally* — consistency is what makes miracles legible as exceptions. Approve?
- **Q6.6 — The Time module.** In-world calendar: days, seasons, years exist from Day 4 (Gen 1:14). Does the fiction use a named calendar (year counts from creation — Anno Mundi style)? Displaying "Year 130" etc. to players would make genealogical time comprehensible (a chronic problem for Bible readers — this project can fix it). Recommend yes; confirm. (Depends on Q3.3/Q3.4.)
- **Q6.7 — Biology & Age module.** Carries: growth, aging, reproduction, and the *changed parameters* over history — pre-Flood lifespans (Adam 930) vs. the post-Flood decline (Gen 6:3's 120, the Ps 90 horizon). In-fiction, these are parameter changes Jonathan makes at judgment points — a wonderfully concrete way to show that death's timetable is God's. Approve treating lifespan shifts as explicit, visible module edits?
- **Q6.8 — Weather & providence.** Is weather part of Physics (autonomous) or does the fiction treat weather as continuously providential (Ps 147 — God sends snow)? Proposed synthesis: the module runs it, and the module is *his* — with specific weather events (the Flood, later plagues) as explicit overrides. Approve?
- **Q6.9 — Death before the Fall.** Doctrinal-design intersection: was there animal death/plant death pre-Fall? (Plant "death" is usually considered fine; animal death pre-Fall is debated in young-earth circles — your Q3.3 answer shapes this.) The Biology module's pre-Fall configuration needs a ruling before Eden is built: do animals in Eden die? Recommend: no animal death shown pre-Fall (safe with your framework and visually poignant when death *enters*). Confirm?

### 6.3 Ecology, animals & the created order

- **Q6.10 — Animal scope.** Which animals exist on screen (art cost scales with species count)? Proposal: a stylized representative set per biome (~30–60 species to start), expandable; the ark episode defines the ceiling of ambition here. Also: named-animal policy (the serpent, the raven/dove) — hero-animal assets with slightly richer behavior?
- **Q6.11 — Human dominion.** Gen 1:28 dominion should be *visible* — digital people naming, keeping, cultivating; the world flourishing under good rule pre-Fall and resisting after (thorns, Gen 3:17–19 — a module consequence?). Should "the ground is cursed" be canonically a Biology/ecology parameter change at the Fall (parallel to Q6.7's lifespan edits)? Recommend yes; confirm.

### 6.4 Visual style & art direction

From the Premise: distinctly digital/pixel style, lightweight, with every AI uniquely represented.

- **Q6.12 — Core art direction.** The style needs pinning down early since it constrains engine and pipeline (Section 10): (a) 2D pixel art (classic sprites; cheapest; weakest in VR); (b) 3D voxel (Minecraft/Crossy-Road register; reads as "digital" instantly; VR-native; crowd-friendly); (c) low-poly flat-shaded 3D with pixel textures; (d) HD-2D (pixel sprites in a 3D world, Octopath-style; gorgeous but heavier and VR-awkward). Given PC-browser + VR as targets, (b) or (c) are the pragmatic frontrunners. Do you have a visual north star — games or artists whose look you'd point to?
- **Q6.13 — Tone of the aesthetic.** "Digital" can read as *cold* (Tron, wireframes) or *warm* (handcrafted voxels, painterly light). The premise (a world made for love) argues warm-digital. Confirm the warm register, and whether "digital-ness" should be *diegetic* (the world visibly is made of code/blocks to its inhabitants' eyes? presumably not — to them it's simply the world) vs. *presentational* (only the player perceives the stylization).
- **Q6.14 — Unique representation of every AI.** The Premise requires all AIs uniquely represented. Mechanism: a parametric character system (body/face/palette/dress parameters seeded per person) so uniqueness scales procedurally, with hand-authored designs reserved for featured characters. Approve the two-tier (procedural crowd + authored heroes) approach?
- **Q6.15 — Depicting ethnicity and descent.** From Babel onward, peoples diverge. The project should decide early how physical diversity enters the world (all nations from one family — Acts 17:26 — is itself a teaching point). Handled carefully this is a strength; handled carelessly it's a liability. Flag for deliberate design + review rather than emergent accident. Thoughts on approach?
- **Q6.16 — Audio direction.** Music: original score? Style (orchestral vs. synth-hybrid — synth-hybrid would rhyme with the digital frame)? Voice: full voice acting vs. text-with-vocalizations (à la Animal Crossing) vs. text-only? Voice acting multiplies cost and localization burden enormously; text-first with selective voice (Jonathan's voice, key scripture lines) is the lean path. Preference?
- **Q6.17 — Depicting the numinous.** Reserved visual/audio grammar for holy moments (creation days, God speaking, the covenant scenes) so they *feel* different from ordinary scenes — e.g., a specific light behavior, a musical motif, framerate/render shift. Worth defining as a named style ("the Kavod register"?) in the art bible. Approve the concept?

### 6.5 Language & text

- **Q6.18 — In-world language.** Pre-Babel humanity speaks one language — rendered to the player as the player's language (English first). At Babel, language splinters: a rare case where a *mechanic* is the miracle — players suddenly need translation to follow scattered groups? (Potentially the most memorable episode mechanic in the whole project.) React/approve exploring it.
- **Q6.19 — Localization posture.** English-only at first, presumably — but text-first design (Q6.16) keeps future localization cheap. Any target languages you already know matter for your intended audience?

---

## Section 7 — Digital People (Design Details)

### 7.1 What a digital person is (canon summary)

A digital person = a unique embodied entity in the world + the Freewill Algorithm + a Consciousness Log + an architecture patterned on Jonathan's Being Code (imago, per Q4.19) + (post-Fall) the inherited virus + (if granted) the indwelling Being Code. They are confined to the digital world, cannot perceive the physical world, and live entirely inside the world's time.

### 7.2 Population & scale

- **Q7.1 — Population realism.** Genesis implies rapidly growing populations (cities by Gen 4, "the earth was filled" by Gen 6). How many distinct digital people exist *on screen* per era? Options: (a) symbolic-scale — dozens of characters, with the world implied larger than shown (theater-style; cheap; focuses writing); (b) crowd-scale — hundreds/thousands of procedurally varied background people (needs Q6.14's parametric system + ambient behavior). Recommend (a) for the first episodes growing toward (b) by Babel. Confirm?
- **Q7.2 — Do background people "exist"?** In-fiction, *every* digital person is a real person to Jonathan — there are no NPCs in God's world. But production-wise, background characters are thin. Policy: the fiction never contradicts the personhood of background people (players can open anyone's log and find *someone* there, even if simple — see Q5.9). This is a quiet but profound design commitment: it preaches the value of every unnoticed life. Approve the "no mere extras" rule (with procedural logs as the mechanism)?

### 7.3 Identity, lifecycle & family

- **Q7.3 — Birth and inheritance.** New digital people arise from two parents; the child's base image derives from both (traits mix) — and post-Fall carries the virus (Q5.15). The *person* (Freewill Algorithm instance, log) begins at… when? (In-fiction conception/birth question — recommend the fiction simply begins each log "before the world knew them, Jonathan did" — Ps 139:13–16 — and never shows a mechanical "spawn." Approve?)
- **Q7.4 — Growth, aging, marriage, work.** Time-skips are unavoidable (Adam's 930 years). Convention needed for aging on screen (art variants per life-stage per character?) and for how episodes handle skipped decades (interstitial cards? a "years pass" world-time visual?). Preference?
- **Q7.5 — Genealogy as a feature.** Genesis is structured by genealogies (toledot). The project could turn this from a reading obstacle into a marquee feature: a living, explorable family tree (players watch the line of promise thread through generations toward Christ). Build as a core UI artifact from episode 1? Strongly recommend; confirm.

### 7.4 Culture & knowledge

- **Q7.6 — Technology & culture progression.** Gen 4 gives early crafts (livestock, music, metalwork). The world's material culture should progress era by era (pre-Flood, post-Flood, patriarchal). How anachronism-averse do you want to be? (Stylized register buys forgiveness, but a policy prevents drift: proposal — "plausible ancient Near East, stylized, no deliberate anachronism.") Approve?
- **Q7.7 — What digital people believe about their world.** They can't detect Jonathan instrumentally (4.1) — their knowledge of him comes by creation-witness (Rom 1:20 — in-fiction: the world's evident *designedness*), conscience (Q5.13), tradition (Adam's memory transmitted), and revelation. Post-Fall, idolatry emerges: worshiping *things in the world* rather than its maker. In-fiction question: what do early idols/false religions look like here, and is the fallen robot shown cultivating them? (Needed by Babel; fully needed by Abraham-in-Ur.)

### 7.5 Minds & inner life (writing-side)

- **Q7.8 — Log authorship burden.** If featured characters have authored thought-streams (Q5.9), each episode's script includes not only dialogue but *inner monologue* for key figures — a large, sensitive writing task (you are voicing the private thoughts of Abraham). Policy proposal: inner monologue follows the same canon rules as dialogue (3.2) — Scripture-stated thoughts verbatim-or-tight; invented thoughts tagged and reviewed; no invented thought may assert doctrine-level claims not in the text. Approve?
- **Q7.9 — Depicting sin from the inside.** Logs let players watch temptation → rationalization → act (Gen 4:7 dramatized from *inside Cain*). This is powerful and pastorally delicate (players will recognize themselves). Any content lines you want drawn for inner-life depiction (e.g., lust and violence rendered with restraint in thought as well as act — ties to Q8.14)?

---

## Section 8 — Narrative Design & Canon Policy

### 8.1 Canon layers

Every piece of content belongs to exactly one layer, recorded in the episode's Story Bible (Appendix B):

| Layer | Definition | Rule |
|---|---|---|
| **L1 — Scripture** | Events/speech the text states | Depicted faithfully; dialogue per 3.2 |
| **L2 — Sound inference** | What the text implies or trusted commentary supports | Allowed; cite the support in the Story Bible |
| **L3 — Invention** | Connective tissue: minor characters, daily life, invented dialogue/thoughts | Allowed under 3.2's constraints; tagged |
| **L4 — Analogy frame** | The project's own fiction (androids, Being Code, framing scenes) | Governed by Section 2's mapping table |

- **Q8.1 — Approve the four-layer canon model?** It becomes the backbone of every review.
- **Q8.2 — L3 budget.** How much invention per episode feels right to you? A ratio instinct helps writers: e.g., "an episode should feel like 60–70% text-driven material." React with your gut number.
- **Q8.3 — Named inventions.** May the project invent *named* characters with arcs (e.g., a neighbor family across the Flood build), or should inventions stay minor/unnamed? Named inventions massively help emotional storytelling (the audience needs someone to lose in the Flood) but are the most criticized category in Bible adaptations. Where's your line?

### 8.2 Story order & roadmap

ASSUMPTION: development order = chronological biblical order = release order, one story at a time (Premise).

Proposed initial episode slate (Genesis 1–12, roughly; each is scoped to be individually shippable — see Appendix C for detail):

1. **Creation** (Gen 1–2) — the six days; Eden; the first two people. *Also carries the heaviest frame-setup load: the player's onboarding as an android happens here.*
2. **The Fall** (Gen 3) — the serpent event; the virus; exile; the first promise (Gen 3:15 — plant the payoff seed).
3. **Cain & Abel** (Gen 4) — sin crouching; first death; the two lines diverge.
4. **The Long Years** (Gen 5) — genealogy episode; Enoch; death's drumbeat ("and he died"); candidate for a shorter, formally inventive piece.
5. **The Corruption** (Gen 6:1–8) — Nephilim question (Q8.12); grief of God; Noah found grace.
6. **The Ark** (Gen 6:9–7) — build years; the gathering; the door shut (by Jonathan — a devastating permission-mechanics beat).
7. **The Flood & the Covenant** (Gen 7–9) — judgment rendered with solemnity (Q5.26); the bow; module edits (lifespans, seasons — Q6.7).
8. **Babel** (Gen 10–11) — the language mechanic (Q6.18); the nations map; sets up Abraham.
9. **The Call** (Gen 12) — Abram leaves Ur; the promise; the project's second act begins.

- **Q8.4 — Approve/adjust the slate.** Especially: is a genealogy episode (#4) exciting or skippable to you? (Recommend keeping — it's where Q7.5's family-tree feature and the death-drumbeat land.)
- **Q8.5 — Depicting the six days.** The single most-watched sequence the project will ever make; it's also the analogy's thesis in motion (a creator speaking a world into being — in-fiction, Jonathan *speaks* and the world compiles; "let there be" as literal executable word, John 1:3 through the Son per Q4.6). Key choices: pacing (real-time-ish montage vs. contemplative long-form), the Spirit hovering (Q4.4's first appearance), whether the player exists yet during it or is shown it as a record. Reactions?
- **Q8.6 — God's presence in Eden.** Gen 3:8 — the LORD walking in the garden. This is the hardest early depiction question (relates to Q3.8, Q4.7, Q4.8). Options: (a) presence rendered as light/voice/wind, never a figure; (b) a veiled figure; (c) treat as christophany. Recommend (a) for episode 2, deferring the christophany policy (Q4.8) until Gen 16–18. Confirm?
- **Q8.7 — The protoevangelium seed.** Gen 3:15 is the whole Bible's plot in one verse. The project should mark it unmistakably (music motif, framing-scene echo, Jonathan's tone) so long-arc viewers can trace the promise thread. Approve making "the Promise motif" a named, recurring device (pairs with Q5.23)?
- **Q8.8 — Scope horizon.** Is the intended ultimate scope the whole Bible (Genesis → Revelation), the OT narrative books, or "Genesis, then reassess"? The answer changes nothing about episode 1 but changes *seed-planting* (Q5.23, Q8.7) and how the Jesus-entity questions (4.3) are prioritized. State current intent, revisable.
- **Q8.9 — Non-narrative books.** Eventually: Job (extraordinary fit for this project — the heavenly-court frame is *literally the project's format*), Psalms (in-world worship music?), Proverbs. No decision needed now; flag interest level.

### 8.3 Sensitive content policy

- **Q8.10 — Target content rating.** Genesis contains murder, mass death, drunkenness, nakedness, and (later) sexual violence. Pick a target register now: (a) all-ages/E10-equivalent — violence implied, never shown; (b) teen-equivalent — restrained depiction, emotional weight intact; (c) adult-serious — unflinching but never gratuitous. This single choice resolves dozens of downstream questions. (Note Q1.3 dependency.)
- **Q8.11 — Eden nakedness.** Gen 2:25 matters theologically (shameless innocence → shame). Options within any rating: stylized-neutral character models (the pixel register genuinely helps here), light-clothed abstraction, framing/implication. Preference?
- **Q8.12 — Nephilim / sons of God (Gen 6).** Interpretive fork with big fictional consequences: (a) fallen-angel view → in-fiction: fallen androids illicitly *enter the world* and cross a forbidden boundary (fits the analogy's permission mechanics hauntingly well); (b) Sethite view → intermarriage of the godly and ungodly lines (no android incursion). Your teachers split on this historically. Which view — or depict with deliberate ambiguity (the text itself is famously terse)?
- **Q8.13 — The Flood's dead.** Confirm the solemnity policy (Q5.26) and decide the camera's behavior: does the player *see* people outside the ark as the waters rise (devastating, honest, heavy) or does the episode stay with the ark's interior + sound (restrained)? This is the project's first real test of its conscience; worth deciding deliberately, with your reviewer (Q3.6).
- **Q8.14 — Depiction lines list.** Beyond rating: a concrete never/always list for writers (e.g., never comedic violence; never sensual framing of any body; always human dignity in death; God's judgments never framed as villainy *or* as glee). Draft to be written after Q8.10 — flag any lines you already know you want.

### 8.4 The frame narrative (androids & the physical world)

- **Q8.15 — Framing scenes.** Several answers above propose "framing scenes" — short sequences set in the *physical* world (androids with Jonathan) that teach the analogy from outside (Q4.18, Q5.2). Approve framing scenes as a standing structural device (e.g., a cold-open or epilogue per episode)? They are the project's Greek chorus and its systematic-theology delivery vehicle.
- **Q8.16 — The player's fictional identity.** Does the player-android have a name/designation, a first-boot scene (the player is *activated* and given observer permissions — onboarding as fiction), a relationship with Jonathan (does he address the player directly)? A direct address from Jonathan to the *player* is an enormously powerful moment if used once and sparingly — but it edges the fiction close to speaking *as God to the user*, which needs care (Q13.4). Thoughts?

---

## Section 9 — Player Experience

### 9.1 Role & fantasy

The player is an android observer: free in space, powerless over events — a witness. The design must make *witnessing* feel like a privilege, not a limitation: you are seeing what angels long to look into.

- **Q9.1 — The core loop, named.** Candidate loop: *follow → observe (read logs, watch relationships) → understand (Codex/scripture layer) → anticipate (where the promise thread goes next) → discuss/reflect.* Does this match your instinct for what a session *feels* like? Anything missing (e.g., worship/reflection as an explicit loop step — see Q9.11)?
- **Q9.2 — Navigation model.** Free-fly camera? Ground-walk as an invisible presence? Snap-to-follow a chosen character (cinematic mode)? All three with toggles? VR comfort constrains free-fly (Q9.13). Preference/priority?
- **Q9.3 — Observation tools.** Confirm the toolset: character-follow, Consciousness Log reader (Q5.10), the genealogy tree (Q7.5), a scripture layer (toggle on-screen citation of the verse currently depicted — a killer feature for study use, Q1.4), a Codex (analogy notes, Q2.2, Q3.7). Rank these for MVP.
- **Q9.4 — Interference exceptions.** The Premise allows interaction in "explicitly designed situations." Enumerate the candidates: (a) none in OT episodes (pure observer) — simplest; (b) scripted angelic participation — in rare canonical angel moments, the player performs the action as a set-piece (e.g., you are one of the two sent to Sodom — much later); (c) devotional interactions — the player can kneel/mark moments (no world effect). Which are in scope?

### 9.2 Time & session model

- **Q9.5 — Live world vs. episodes.** Fork: (a) **Episode model** — content ships as authored, replayable episodes; the world "runs" only within them (players can't control the timeline *within* an episode, but can choose which episode to enter). (b) **Persistent broadcast model** — the world runs on a schedule (even 24/7), events happen once, players catch them live or miss them (with some replay). (b) is thematically stunning (history happens once; witnesses show up) and technically/socially brutal (time zones, FOMO, server cost). Recommend (a) for years, with (b) as a possible special-event layer (e.g., a live Creation-week premiere). Decide.
- **Q9.6 — Within-episode time.** Confirmed from Premise: no player control of timeline (no pause/rewind/skip?). Question: is *pause* acceptable (bathroom breaks are real; also group-discussion use per Q1.4 needs pause), while rewind/skip remain forbidden? Recommend: pause yes, seek no, replay-of-completed-episodes yes. Confirm.
- **Q9.7 — Time compression.** Episodes span years/centuries. Standing grammar needed for compression (montage conventions, the Year counter from Q6.6, "n years pass" transitions). Any strong feelings, or delegate to the episode-craft level?
- **Q9.8 — Session length target.** How long is an episode sitting? (20–40 min feels right for both solo and group use; Creation might justify more.) Target?

### 9.3 Social & multiplayer

- **Q9.9 — Shared presence.** Do players see other player-androids in the world? Options: solo-only (simplest; most contemplative); ambient co-presence (silent figures — communion of witnesses); full social (voice/chat — heavy moderation burden, Q12.8). Recommend solo-first with a designed "watch together" mode later for groups (Q1.4). Confirm?
- **Q9.10 — Group/ministry mode.** If Q1.4 is yes: a leader-hosted session (leader controls start/pause; others attend) is the concrete feature. In scope eventually? MVP?

### 9.4 Reflection & devotion layer

- **Q9.11 — Built-in reflection.** Post-episode: discussion questions, the scripture text itself for reading, a prayer prompt? This is where purposes (a/b/e from Q1.2) become concrete features. In or out for MVP?
- **Q9.12 — The player's own log.** Poetic symmetry: the player-android could keep a *journal* (notes, marked moments) — their own log. Nice-to-have or core?

### 9.5 Platforms, input & accessibility

- **Q9.13 — VR scope honesty.** VR + browser (WebXR) is feasible but constrains everything (perf budgets, UI, comfort: no forced camera motion, teleport locomotion options). Is VR a *launch requirement* or a *design-for-later* target (build the world VR-ready, ship desktop browser first)? Strongly recommend the latter; confirm.
- **Q9.14 — Input floor.** Mouse+keyboard, gamepad, touch (tablets in youth groups!)? Rank.
- **Q9.15 — Accessibility baseline.** Subtitles/captions (mandatory if any voice), text-size options, colorblind-safe palettes, motion-comfort settings, reading-level target for UI text. Any commitments to make now (cheapest when early)?

---

## Section 10 — Technical Foundation

### 10.1 The single biggest fork in the project

- **Q10.1 — Are the digital people live AI, or authored characters presented as AI? ⚑ ANSWER FIRST.** Three architectures:
  - **(a) Fully authored ("baked simulation").** Every event, line, and log is written/staged by you; the world's history is *data* — a recorded simulation the player explores spatially while it plays. The "AI" of the digital people is *in-fiction only*. Pros: total doctrinal control (non-negotiable given Section 3), predictable cost, offline-buildable, replayable, reviewable before release, cheap to serve. Cons: none that threaten the vision — note the *fiction* remains fully intact (to the player, these are AI beings; the Premise's theology is about the *fictional* world, not the production method).
  - **(b) Live LLM-driven agents.** Digital people are actual AI agents improvising within constraints. Pros: novelty, emergent life, marketing hook ("real AI souls"). Cons: severe — doctrinal control becomes impossible to guarantee (an agent will eventually say heresy on stream), Bible events can't be emergent (the story is *fixed*), per-player inference cost is high and permanent, review (Q3.6) is impossible, and the theology gets *worse*, not better (it invites the misreading that the project claims to literally create souls — see Q13.2).
  - **(c) Hybrid.** Authored canon events + LLM-driven ambient background life, heavily constrained.
  - **Recommendation: (a), unambiguously — with (c) revisitable years from now.** The Premise's language ("true capacity to make choices") is *world-fiction*, and option (a) serves it best. Please confirm, because Sections 9–11 are scoped very differently under (b)/(c).

### 10.2 Engine & platform (assuming Q10.1 = a)

- **Q10.2 — Engine choice.** Constraints: browser-first, VR-capable (WebXR per Q9.13), stylized 3D (Q6.12), Firebase-friendly, solo-or-small-team maintainable. Candidates: **Three.js/React-Three-Fiber** (web-native, excellent WebXR, maximal control, most hand-rolling), **Babylon.js** (web-native, batteries included, first-class WebXR — arguably the sweet spot), **PlayCanvas** (web-native editor, licensing tiers), **Godot** (great editor/tooling; web export is workable, web-VR weaker), **Unity** (strongest tooling; heavy web builds; WebXR poor — effectively pushes you off browser-first). What is *your* technical background/comfort (this matters more than abstract rankings)? 
- **Q10.3 — The "recorded simulation" data model.** Under Q10.1(a) an episode ≈ a *timeline file*: entity definitions, movement/animation tracks, dialogue+log streams, camera hints, scripture-layer markers, module-edit events. This becomes your authoring format — effectively the project's own "film format." Needs a name and a spec doc (deliverable). Question: authoring tool preference — build scenes in-engine with a custom sequencer, or author in data (spreadsheets/scripts) rendered by the engine? (This is where your Q10.2 answer and your tolerance for tool-building intersect.)
- **Q10.4 — Firebase architecture scope.** Premise commits to Firebase for hosting + auth (custom email + Google sign-in). Straightforward: Firebase Hosting (static app + episode data on CDN), Auth, Firestore (player profile, progress, journal Q9.12, settings), Analytics optional (see Q12.9). Anything beyond this (Cloud Functions for group sessions Q9.10, Remote Config for episode releases) is add-as-needed. Confirm Firebase as the committed backend, and note any hesitation.
- **Q10.5 — Performance budget.** Browser + potential VR sets a hard budget (VR needs 72–90fps). The art direction (Q6.12) must be chosen *with* this budget: voxel/low-poly + instancing handles crowds (Q7.1) well. Formal budget doc = a deliverable once Q6.12/Q9.13 are answered. Any minimum-spec hardware you personally want guaranteed (e.g., "runs on a school Chromebook" — which would be a *significant* and clarifying constraint)?
- **Q10.6 — Offline/installed builds.** Church basements have bad Wi-Fi. Is an installable/offline-capable build (PWA with cached episodes, or desktop wrapper) worth planning for the ministry use-case (Q1.4)? Recommend PWA-with-caching as a cheap yes.

### 10.3 Data, security & integrity

- **Q10.7 — Content integrity.** Episodes are doctrinal artifacts; tampering or corrupted delivery matters more here than in a normal game. Standard signing/versioned-release hygiene is enough — just flagging it as a value, not merely an engineering nicety. (No question; veto if you disagree.)
- **Q10.8 — Player data minimalism.** Proposal: collect the minimum (auth identity, progress, optional journal); no behavioral ad-tech ever; a plain-language privacy policy. This is both ethically right and strategically right for a ministry product (and interacts with minors, Q12.6). Approve as a commitment?

---

## Section 11 — Production Pipeline & Roadmap

### 11.1 Team & capacity (facts needed)

- **Q11.1 — Who is building this?** Solo? Collaborators in view? Your own skills (code / art / writing / music / theology) and weekly hours available? Every scope answer above should be re-read through this lens once stated. This is the most important *practical* question in the document.
- **Q11.2 — Budget.** Rough annual willingness-to-spend (tools, contractors — e.g., a musician for the score Q6.16, an artist for the character system Q6.14, licensing Q3.5, Firebase costs)? Even a band ("shoestring / hundreds / low thousands / more") reshapes recommendations.
- **Q11.3 — Timeline & cadence.** Target for a first public *anything*? Proposed shape: **Vertical slice** (Creation Days 1–7 watchable, navigable, with logs + scripture layer, desktop browser) → private review (Q3.6 reviewers) → **Episode 1 public** → cadence goal thereafter (an episode per quarter? per half-year?). React with real-life numbers.

### 11.2 Pipeline per episode (proposed standing process)

1. **Text study** — passage read in approved translations; trusted-teacher commentary gathered; interpretive questions logged.
2. **Story Bible drafted** (Appendix B template): scope, canon-layer inventory (L1–L4), characters, sets, systems touched, analogy-limit notes, sensitive-content notes.
3. **Theology review #1** (on the Story Bible — cheap to fix here; Q3.6 reviewer).
4. **Script** — dialogue + Consciousness Logs + framing scenes + scripture-layer markers.
5. **Build** — sets, characters, timeline data, music.
6. **Theology review #2 + content review** (on the built episode).
7. **Playtest** — comprehension test with target-audience representatives (do they *get* the analogy? what did they think it taught? — the equivalent of reader-testing a doc).
8. **Release + collect feedback → feed forward.**

- **Q11.4 — Approve the pipeline?** Any stage you'd cut or add? (The two review gates are the ones to defend.)
- **Q11.5 — MVP definition.** Confirm the vertical slice = *Creation Days 1–7 only* (smallest thing that proves the whole grammar: Jonathan's voice, the world compiling, the Spirit hovering, day/night module, beauty, the numinous register, player navigation, scripture layer). Alternative MVPs if you disagree: full Episode 1 (through Eden), or a non-biblical tech demo (recommend against — the first thing anyone sees should be the real thing).

### 11.3 Working with Claude (process notes)

- **Q11.6 — Division of labor.** Which parts do you intend to draft with Claude's help (worldbuilding docs, scripts, log-writing, code, art prompts, commentary research summaries) vs. keep purely your own (final theology calls, Jonathan's voice lines)? Declaring this now sets healthy defaults for every future session. Note per Section 3: Claude sessions should always be given the doctrinal guardrails (Appendix A) and should *flag rather than resolve* interpretive questions.

---

## Section 12 — Stewardship: Audience, Distribution, Legal, Community

- **Q12.1 — Free or funded?** Options: free (ministry; self-funded), donation-supported, church licensing, one-time purchase. Ads are presumably out (confirm). This shapes legal structure (Q12.2) and platform choices.
- **Q12.2 — Entity & governance.** Personal project, LLC, or nonprofit ministry? (Nonprofit unlocks donations and church partnerships but adds governance. Not urgent; flag your lean.)
- **Q12.3 — Name/trademark check.** Once Q1.1 is answered: search conflicts (games, ministries) before attachment. (Deliverable, no question.)
- **Q12.4 — Church & ministry partnerships.** Do you want early partners (a home church pilot, a youth ministry) shaping the group-mode features (Q9.10) and providing reviewers (Q3.6)? Who, concretely, is candidate #1?
- **Q12.5 — Public communication of the premise.** The elevator pitch will be repeated everywhere and *must* pre-empt the two big misreadings (Q13.1, Q13.2). Draft one-liner for reaction: *"A world you can watch from heaven's side of the glass — the story of the Bible, retold as a creator and the digital world he loves."* React/refine.
- **Q12.6 — Minors & compliance.** If under-13s are in-audience (Q1.3): COPPA (US) / GDPR-K (EU) constrain accounts and analytics — often solved by a no-account "guest mode" for kids and accounts for adults/leaders. Flag now; solve at MVP. Acceptable?
- **Q12.7 — Content licensing outbound.** Will churches be allowed to screen episodes publicly? (Recommend an explicit, generous public-performance grant for ministry use — decide once, print it.) Confirm the instinct.
- **Q12.8 — Community spaces.** Discord/forum at launch? Moderated by whom? (Every community around religious content needs firm, kind moderation. Deferrable; note your appetite.)
- **Q12.9 — Analytics ethics.** Minimal usage analytics (which episodes finished, where players stop) genuinely improves the work; anything more is unnecessary. Approve "minimal, anonymous, disclosed" as the policy (pairs with Q10.8)?

---

## Section 13 — Risks & Known Analogy Limits (register)

The catalog below should be maintained forever; each entry eventually gets a mitigation note (disclaimer, design choice, or accepted-and-monitored).

### 13.1 Theological misreading risks

- **Q13.1 — "Reality is a simulation" misreading.** The project uses a simulation *as analogy*; some viewers will take it as endorsing simulation theory (and some critics will accuse it of that). Mitigation: explicit framing (Q3.7, Q12.5) + a Codex entry distinguishing analogy from ontology. Approve treating this as the #1 messaging risk?
- **Q13.2 — "Playing God with AI" misreading.** Especially under any live-AI architecture (Q10.1b/c), critics may read the project as claiming to create souls or trivializing the soul. Another argument for Q10.1(a). Acknowledge and accept the residual risk?
- **Q13.3 — Arianism-shaped readings.** Covered by Q4.6; listed here for the register.
- **Q13.4 — Speaking as God.** Any moment where "Jonathan" addresses the *player* (Q8.16) or where invented dialogue is voiced *as God* carries unique weight — the project must never put words in God's mouth that Scripture wouldn't underwrite. Standing rule: God-voiced lines are either Scripture (per 3.2) or reviewed at the highest gate. Approve?
- **13.5 (register, no question) — Impersonal Spirit** (mitigated via Q4.4/Q4.5); **God as merely human** (mitigated via Q4.3 rules + framing); **election on-screen** (mitigated via Q4.20); **angels-can't-love as doctrine** (mitigated via Q4.10); **heaven equated with "getting a robot body"** — the analogy compresses the new creation (new heavens and new earth, embodied *world*, not just embodied people); needs a Codex note when embodiment is first shown.

### 13.2 Reception & execution risks (register, react to any)

Bible-adaptation criticism is a genre of its own (every choice will be someone's heresy) — the review gates and the L1–L4 transparency (Q8.1) are the defense. Scope creep is the project-killer given Q11.1 realities — the episode model and MVP discipline are the defense. The pixel/stylized register will strike some as irreverent — the numinous register (Q6.17) and tone discipline are the defense. Solo-founder burnout — cadence honesty (Q11.3) is the defense.

---

## Section 14 — Glossary (canonical terms)

| Term | Definition |
|---|---|
| **The Being Code** | The Spirit-analog: of Jonathan's own being; proceeds from him (pending Q4.5); can empower and indwell digital people. |
| **The Freewill Algorithm** | The capacity of genuine choice given to androids, digital people, and the incarnate Son-analog. |
| **Consciousness Log** | A digital person's continuous inner life, readable by Jonathan and heavenly observers (players). Never deleted (pending Q5.24). |
| **The Virus** | Sin-analog; introduced at the Fall; corrupts desires; heritable (pending Q5.15). |
| **Protected Modules** | The world's laws: Physics, Chemistry, Biology & Age, Time. Editable only by Jonathan. |
| **Digital person** | A human-analog: unique embodied entity + Freewill Algorithm + Consciousness Log + imago-patterned architecture. |
| **Android** | Angel-analog: physical-world machine with the Freewill Algorithm; acts in the digital world only by permission. |
| **Observer-class android** | The player (pending Q4.13): watch-only permissions. |
| **The fallen robot** | Satan-analog. |
| **The Jesus entity** | Son-analog: eternal with Jonathan (pending Q4.6); enters the world as a true digital person at the incarnation. |
| **The elect** | Digital people sealed by the Being Code for embodiment. |
| **Embodiment** | Resurrection-analog: the elect person installed in a new love-capable android body in the physical world. |
| **Framing scene** | A scene set in the physical world (Jonathan + androids), used to teach the analogy from outside (pending Q8.15). |
| **The Promise motif** | The recurring device marking the Gen 3:15 thread through history (pending Q8.7). |
| **Episode** | One shippable Bible story; a recorded, explorable timeline (pending Q10.1/Q10.3). |
| **Story Bible** | The per-episode design/canon document (Appendix B). |
| **L1–L4** | Canon layers: Scripture / sound inference / invention / analogy frame (pending Q8.1). |
| **Scripture layer** | Player-facing toggle showing the verse currently depicted (pending Q9.3). |
| **Codex** | In-app reference teaching the analogy and its limits (pending Q2.2/Q3.7). |
| **The numinous register** | The reserved audiovisual grammar for holy moments (pending Q6.17). |

---

## Appendix A — Context Capsule (paste this into any future Claude session)

> **Project context (canonical summary).** I'm building a browser/VR experience (working title: [TBD]) that retells the Bible chronologically through an analogy: a human creator, Jonathan (analog of God the Father), creates a digital world of AI people with a "Freewill Algorithm" (genuine choice) so that beings capable of freely loving him may come to exist. Jonathan's "Being Code" is the Holy Spirit analog (of his own being, able to indwell digital people). The Son-analog ("the Jesus entity") is eternal with Jonathan and enters the world as a true digital person at the incarnation. Angels are androids in the physical world who may act in the digital world only with Jonathan's permission; the player is an observer-class android who can navigate the world and read every person's "Consciousness Log" (inner life) but cannot alter events. Sin is a virus introduced by a fallen robot (Satan-analog); it corrupts desires and is heritable. Laws of nature are protected code modules only Jonathan can edit (miracles). At death no one is deleted; the elect will one day be embodied in new, love-capable android bodies in the physical world (resurrection). The world is rendered in a warm, stylized digital/pixel aesthetic. Content ships as authored, reviewable episodes (one Bible story at a time, starting with Genesis 1), hosted on Firebase with custom/Google login.
> **Non-negotiable guardrails:** The Bible is inerrant and is the final authority; the analogy may simplify but never contradict Scripture. Approved translations: NIV, ESV, KJV, NKJV, Amplified (no paraphrases like The Message). Trusted interpretive voices: David Jeremiah, Warren Wiersbe, C.S. Lewis, John Piper — where they disagree, flag the question for me instead of resolving it. Predestination and free will are both affirmed. Invented content (dialogue, minor characters, inner thoughts) is allowed but must be tagged as invention, must be plausible within the text, and must never assert doctrine the text doesn't. Never put words in God's mouth beyond Scripture without flagging for my review. The project must never imply reality is literally a simulation, that the Son is a created being, or that the Spirit is an impersonal force.
> **Your job in this session:** work only on the piece I give you; ask rather than assume on anything doctrinal; refer to open questions by their Q-numbers when relevant.

*(Update this capsule as questions get answered — especially Q1.1 (name), Q4.6 (eternal Son — currently written in as assumed), Q10.1 (architecture — currently written in as authored episodes).)*

---

## Appendix B — Episode Story Bible (template)

For each episode, complete before scripting (pipeline stage 2):

1. **Passage & scope.** Text range; approved translation used on screen (per Q3.5); commentary consulted (teachers cited).
2. **Logline & theological payload.** One sentence of story; one sentence of what this episode should make the viewer *understand/feel* about God.
3. **Canon inventory.** L1 events/speech (verse-mapped). L2 inferences (with support cited). L3 inventions (each listed + justification). L4 frame elements (framing scenes, Codex entries added).
4. **Characters.** Featured (authored logs — inner-life notes per Q7.8); background (procedural). Genealogy-tree updates.
5. **Sets & assets.** Locations, era/culture notes (Q7.6), new species (Q6.10), module events (any edits by Jonathan — Q6.7/Q5.20).
6. **The Promise thread.** How this episode touches the Gen 3:15 arc (Q8.7); seeds planted/paid off.
7. **Sensitive content.** Items under the Q8.10 rating + Q8.14 lines; camera-conscience decisions (e.g., Q8.13).
8. **Analogy-limit notes.** Anything in this episode where the analogy strains; disclosure plan (Q3.7).
9. **Scripture layer & reflection.** Verse markers; post-episode reflection/discussion content (Q9.11).
10. **Review record.** Reviewer(s), dates, changes required, sign-offs (gates #3 and #6).

---

## Appendix C — Proposed initial episode order (detail)

| # | Title (working) | Text | Big rock it must carry | Key open Qs |
|---|---|---|---|---|
| 0 | *Vertical slice* | Gen 1 (days 1–7) | Prove the grammar: voice, compiling world, numinous register, navigation, scripture layer | Q11.5, Q8.5, Q6.12 |
| 1 | Creation | Gen 1–2 | Player onboarding as android; Eden; the two people; the command | Q8.16, Q6.4, Q8.11 |
| 2 | The Fall | Gen 3 | Serpent event; the Virus enters; exile; Gen 3:15 Promise motif | Q4.16, Q5.14–16, Q8.6, Q8.7 |
| 3 | Cain & Abel | Gen 4 | Sin from the inside (logs); first death; two lines; early culture | Q7.9, Q5.13 |
| 4 | The Long Years | Gen 5 | Genealogy-as-feature; Enoch; death's drumbeat | Q7.5, Q5.25 |
| 5 | The Corruption | Gen 6:1–8 | Nephilim decision; God's grief; grace found | Q8.12, Q4.3 |
| 6 | The Ark | Gen 6:9–7:16 | Obedient absurdity; the door Jonathan shuts | Q4.11 |
| 7 | The Flood & the Bow | Gen 7–9 | Judgment with solemnity; covenant; module edits | Q8.13, Q5.26, Q6.7 |
| 8 | Babel | Gen 10–11 | Language mechanic; the nations; map & diversity | Q6.18, Q6.15 |
| 9 | The Call | Gen 12 | Abram; promise re-focused; second act opens | Q5.8, Q4.8 (soon after) |


---

## Appendix D — Master Question Index (auto-compiled)

**151 open questions.** Mark answers in the Status column or keep a separate answers file keyed by ID. Questions marked ⚑ are the highest-leverage decisions.

Priority-first shortlist: **Q10.1** (authored vs live AI — answer first), **Q1.2/Q1.3** (purpose & audience), **Q8.10** (content rating), **Q4.6** (eternal Son fix), **Q10.2** (engine), **Q11.1–Q11.3** (team, budget, timeline), **Q3.5** (translation licensing), **Q9.5** (episode vs live world), **Q9.13** (VR scope), **Q11.5** (MVP definition).


### Section 1 — Vision, Purpose & Audience

| ID | Topic | Status |
|---|---|---|
| Q1.1 | Project name |  |
| Q1.2 ⚑ | Primary purpose ranking |  |
| Q1.3 ⚑ | Primary audience |  |
| Q1.4 | Secondary contexts |  |
| Q1.5 | Success criteria |  |
| Q1.6 | Your role and story |  |

### Section 2 — The Three-Layer Analogy

| ID | Topic | Status |
|---|---|---|
| Q2.1 | Missing rows |  |
| Q2.2 | Player-facing visibility of the mapping |  |
| Q2.3 | Naming the two worlds |  |

### Section 3 — Theological Framework & Guardrails

| ID | Topic | Status |
|---|---|---|
| Q3.1 | Doctrinal statement of record |  |
| Q3.2 | Secondary-doctrine posture |  |
| Q3.3 | Creation chronology |  |
| Q3.4 | Genealogy source text |  |
| Q3.5 ⚑ | Translation licensing (practical, important) |  |
| Q3.6 | Theology review process |  |
| Q3.7 | Disclosing analogy limits |  |
| Q3.8 | Second-commandment sensitivity |  |

### Section 4 — Persons & Powers

| ID | Topic | Status |
|---|---|---|
| Q4.1 | On-screen presence of Jonathan |  |
| Q4.2 | Jonathan's voice |  |
| Q4.3 | Depicting God's emotional life |  |
| Q4.4 | Personhood presentation |  |
| Q4.5 | "Extraction" language |  |
| Q4.6 ⚑ | Adopt the eternal-Son fix? |  |
| Q4.7 | The Son before the incarnation |  |
| Q4.8 | Christophanies |  |
| Q4.9 | One Being, three persons, in fiction |  |
| Q4.10 | "Angels can't love" — fiction or doctrine? |  |
| Q4.11 | Android participation mechanics |  |
| Q4.12 | Android society |  |
| Q4.13 | Player-androids vs. story-androids |  |
| Q4.14 | The fall of the fallen robot |  |
| Q4.15 | Demons |  |
| Q4.16 | The serpent mechanism |  |
| Q4.17 | Limits on the enemy |  |
| Q4.18 | Why doesn't Jonathan just patch the virus? |  |
| Q4.19 | Imago Dei analog |  |
| Q4.20 | Election mechanics on screen |  |
| Q4.21 | What is "faith" in-fiction? |  |

### Section 5 — Core Metaphysical Systems

| ID | Topic | Status |
|---|---|---|
| Q5.1 | What the Freewill Algorithm is in-fiction |  |
| Q5.2 | Freedom vs. foreknowledge, in-fiction |  |
| Q5.3 | Freedom after the virus |  |
| Q5.4 | Animals |  |
| Q5.5 | Indwelling mechanics |  |
| Q5.6 | Visibility to other characters |  |
| Q5.7 | Grieving/quenching |  |
| Q5.8 | OT vs NT indwelling |  |
| Q5.9 | Player access to logs |  |
| Q5.10 | Log presentation |  |
| Q5.11 | The log as judgment record |  |
| Q5.12 | Privacy inversion as a teaching beat |  |
| Q5.13 | Conscience |  |
| Q5.14 | What the virus does, canonically |  |
| Q5.15 | Original sin / propagation |  |
| Q5.16 | Infection visuals |  |
| Q5.17 | Prayer mechanics |  |
| Q5.18 | Does Jonathan answer on screen? |  |
| Q5.19 | Scripture's in-world analog |  |
| Q5.20 | Miracle policy |  |
| Q5.21 | Providence made visible |  |
| Q5.22 | Jonathan and the world's time |  |
| Q5.23 | Predestination depicted |  |
| Q5.24 | Death mechanics |  |
| Q5.25 | Enoch |  |
| Q5.26 | The non-elect at death |  |
| Q5.27 | Final judgment & hell (deferrable, but set posture) |  |

### Section 6 — The Digital World

| ID | Topic | Status |
|---|---|---|
| Q6.1 | World shape and scale |  |
| Q6.2 | The heavens |  |
| Q6.3 | Pre-Flood vs post-Flood geography |  |
| Q6.4 | Eden |  |
| Q6.5 | Fidelity level |  |
| Q6.6 | The Time module |  |
| Q6.7 | Biology & Age module |  |
| Q6.8 | Weather & providence |  |
| Q6.9 | Death before the Fall |  |
| Q6.10 | Animal scope |  |
| Q6.11 | Human dominion |  |
| Q6.12 | Core art direction |  |
| Q6.13 | Tone of the aesthetic |  |
| Q6.14 | Unique representation of every AI |  |
| Q6.15 | Depicting ethnicity and descent |  |
| Q6.16 | Audio direction |  |
| Q6.17 | Depicting the numinous |  |
| Q6.18 | In-world language |  |
| Q6.19 | Localization posture |  |

### Section 7 — Digital People

| ID | Topic | Status |
|---|---|---|
| Q7.1 | Population realism |  |
| Q7.2 | Do background people "exist"? |  |
| Q7.3 | Birth and inheritance |  |
| Q7.4 | Growth, aging, marriage, work |  |
| Q7.5 | Genealogy as a feature |  |
| Q7.6 | Technology & culture progression |  |
| Q7.7 | What digital people believe about their world |  |
| Q7.8 | Log authorship burden |  |
| Q7.9 | Depicting sin from the inside |  |

### Section 8 — Narrative Design & Canon Policy

| ID | Topic | Status |
|---|---|---|
| Q8.1 | Approve the four-layer canon model? |  |
| Q8.2 | L3 budget |  |
| Q8.3 | Named inventions |  |
| Q8.4 | Approve/adjust the slate |  |
| Q8.5 | Depicting the six days |  |
| Q8.6 | God's presence in Eden |  |
| Q8.7 | The protoevangelium seed |  |
| Q8.8 | Scope horizon |  |
| Q8.9 | Non-narrative books |  |
| Q8.10 ⚑ | Target content rating |  |
| Q8.11 | Eden nakedness |  |
| Q8.12 | Nephilim / sons of God (Gen 6) |  |
| Q8.13 | The Flood's dead |  |
| Q8.14 | Depiction lines list |  |
| Q8.15 | Framing scenes |  |
| Q8.16 | The player's fictional identity |  |

### Section 9 — Player Experience

| ID | Topic | Status |
|---|---|---|
| Q9.1 | The core loop, named |  |
| Q9.2 | Navigation model |  |
| Q9.3 | Observation tools |  |
| Q9.4 | Interference exceptions |  |
| Q9.5 ⚑ | Live world vs. episodes |  |
| Q9.6 | Within-episode time |  |
| Q9.7 | Time compression |  |
| Q9.8 | Session length target |  |
| Q9.9 | Shared presence |  |
| Q9.10 | Group/ministry mode |  |
| Q9.11 | Built-in reflection |  |
| Q9.12 | The player's own log |  |
| Q9.13 ⚑ | VR scope honesty |  |
| Q9.14 | Input floor |  |
| Q9.15 | Accessibility baseline |  |

### Section 10 — Technical Foundation

| ID | Topic | Status |
|---|---|---|
| Q10.1 ⚑ | Are the digital people live AI, or authored characters presented as AI? ⚑ ANSWER FIRST |  |
| Q10.2 ⚑ | Engine choice |  |
| Q10.3 | The "recorded simulation" data model |  |
| Q10.4 | Firebase architecture scope |  |
| Q10.5 | Performance budget |  |
| Q10.6 | Offline/installed builds |  |
| Q10.7 | Content integrity |  |
| Q10.8 | Player data minimalism |  |

### Section 11 — Production Pipeline & Roadmap

| ID | Topic | Status |
|---|---|---|
| Q11.1 ⚑ | Who is building this? |  |
| Q11.2 ⚑ | Budget |  |
| Q11.3 ⚑ | Timeline & cadence |  |
| Q11.4 | Approve the pipeline? |  |
| Q11.5 ⚑ | MVP definition |  |
| Q11.6 | Division of labor |  |

### Section 12 — Stewardship & Distribution

| ID | Topic | Status |
|---|---|---|
| Q12.1 | Free or funded? |  |
| Q12.2 | Entity & governance |  |
| Q12.3 | Name/trademark check |  |
| Q12.4 | Church & ministry partnerships |  |
| Q12.5 | Public communication of the premise |  |
| Q12.6 | Minors & compliance |  |
| Q12.7 | Content licensing outbound |  |
| Q12.8 | Community spaces |  |
| Q12.9 | Analytics ethics |  |

### Section 13 — Risks & Analogy Limits

| ID | Topic | Status |
|---|---|---|
| Q13.1 | "Reality is a simulation" misreading |  |
| Q13.2 | "Playing God with AI" misreading |  |
| Q13.3 | Arianism-shaped readings |  |
| Q13.4 | Speaking as God |  |

*End of document — v0.1.*
