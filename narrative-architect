---
name: "narrative-architect"
description: "10-dimension narrative generator built on the COLM 2026 StoryScope framework (Google DeepMind/UMD). Crafts fiction, brand origin stories, customer case studies, executive bios, and long-form narrative content using human-leaning structural features — nonlinear temporal framing, ambivalent moral polarity, thematically parallel subplots, implicit intertextuality, grounded character expression, and model-neutral prose. Produces narratives that score within human-range on all 30 StoryScope features from the start — no post-hoc humanization needed. Triggers: 'write a story', 'generate narrative', 'brand story', 'origin story', 'case study narrative', 'write fiction', 'narrative architect', 'StoryScope generation', 'human-grade story', 'write like a human'."
license: MIT
argument-hint: "[describe the story/narrative you want — genre, characters, themes, length, tone]"
metadata:
  version: 2.0.0
  build_pattern: "Path-A methodology skill — StoryScope COLM 2026 generation framework with deterministic structural scoring"
  research_basis: "StoryScope: Investigating idiosyncrasies in AI fiction (COLM 2026, UMD & Google DeepMind) — arXiv:2604.03136"
  companion_skill: "narrative-humanizer — for post-hoc humanization of AI-written text that wasn't generated with this skill"
  distinct_from: "Standard AI story generators that produce flat, linear, thematic-over-determined prose. Narrative Architect controls all 10 StoryScope dimensions at generation time, producing human-range structural scores from the first draft."
---

# Narrative Architect — StoryScope Generation Engine

**Generate stories that are structurally human from the first draft — no post-hoc humanization needed.**

Most AI story generation produces text that sounds plausible on the surface but has telltale structural flaws: linear timelines, preachy endings, embodied trope spam, single-track plots, and tidy moral resolutions. StoryScope research (COLM 2026, UMD & Google DeepMind) proved these discourse-level patterns — not vocabulary — are how AI fiction is detected (93.2% accuracy).

Narrative Architect controls narrative choices across **10 structural dimensions** during generation, producing text that scores within human-range on all 30 core StoryScope features from the first draft.

## What This Does

Takes a brief (genre, characters, setting, themes, length) and generates a structurally human narrative by:
1. Designing the structural blueprint across all 10 dimensions before writing a single word
2. Generating the narrative following the blueprint with human-range feature targets
3. Self-scoring the output against all 30 features to verify it's within human range
4. Offering a revision pass if any dimension falls outside human thresholds

The result: a story, brand narrative, or case study that reads like a human wrote it — because its structural architecture matches how humans actually construct narratives.

## Step 1 — Define the Narrative Brief

Collect or infer the narrative brief. Run the brief designer:

```bash
python3 scripts/narrative_brief_designer.py \
  --prompt "A founder who built a logistics startup after losing their first company to bankruptcy" \
  --genre "brand-origin" \
  --length "medium" \
  --tone "grounded, reflective" \
  --output brief.json
```

### Brief Parameters

| Parameter | Options | Default |
|-----------|---------|---------|
| `--genre` | `literary-fiction`, `scifi`, `thriller`, `romance`, `fantasy`, `brand-origin`, `case-study`, `executive-bio`, `memo`, `video-script` | Auto-detected from prompt |
| `--length` | `flash` (<1000 words), `short` (1000-3000), `medium` (3000-6000), `long` (6000-12000) | `medium` |
| `--tone` | Free text description | Inferred from prompt |
| `--pov` | `first`, `second`, `third-limited`, `third-omniscient`, `rotating` | `third-limited` |
| `--time-structure` | `linear`, `nonlinear`, `in-medias-res`, `frame-narrative`, `episodic` | `nonlinear` (human-preferred) |
| `--theme-approach` | `implicit`, `semi-explicit`, `explicit` | `implicit` (human-preferred) |
| `--moral-complexity` | `high`, `medium`, `low` | `high` (human-preferred) |

### Genre-Specific Defaults

The brief designer adjusts dimension targets based on genre:

| Genre | Time Structure | Moral Complexity | Subplots | Embodied Tropes Allowed |
|-------|:-------------:|:----------------:|:--------:|:----------------------:|
| Literary Fiction | Nonlinear | High | 1-2 parallel | Low (<30%) |
| Thriller | In-medias-res | Medium | 1 | High (<60%) |
| Brand Origin | Frame narrative | Medium | 0-1 | Low (<35%) |
| Case Study | Linear with flashbacks | Medium | 0 | Low (<30%) |
| Romance | Nonlinear | Medium | 1 parallel | Medium (<50%) |
| Sci-Fi | Episodic | High | 1-2 parallel | Low (<35%) |

If the user provides only a prompt without specifying genre or parameters, the designer auto-classifies the genre from the prompt content and sets appropriate defaults.

## Step 2 — Design the Structural Blueprint

Before generating any prose, design the structural blueprint across all 10 dimensions:

```bash
python3 scripts/blueprint_designer.py \
  --brief brief.json \
  --output blueprint.json
```

### The 10-Dimension Blueprint

The blueprint is a JSON document specifying structural decisions for each dimension:

```json
{
  "agent": {
    "introduction_method": "through_action",
    "emotional_expression": "behavioral_and_labels",
    "interior_access_depth": 3.5,
    "trait_reveal_sequence": ["stubbornness_via_dialogue", "fear_via_avoidance", "loyalty_via_sacrifice"]
  },
  "social_network": {
    "core_relationships": 3,
    "relationship_arcs": ["mentor→rival", "stranger→ally"],
    "community_presence": "background_only"
  },
  "event": {
    "causal_chain_type": "interrupted",
    "escalation_pattern": "surge_plateau_surge",
    "event_type_diversity": ["decision", "accident", "confrontation", "revelation", "quiet_moment"]
  },
  "plot": {
    "arc_structure": "descent_recovery_transformation",
    "subplots": [
      {"character": "business_partner", "arc": "parallel_failure_different_choice"}
    ],
    "resolution_type": "partial_with_cost",
    "moral_stance": "ambivalent"
  },
  "structure": {
    "theme_delivery": "implicit_through_action",
    "moral_polarity": "mixed",
    "intertextual_strategy": "named_reference_to_industry_event",
    "narrator_commentary": "minimal"
  },
  "setting": {
    "spatial_granularity": 2.2,
    "location_count": 4,
    "weather_mood_link": "decoupled",
    "sensory_modality_mix": ["visual", "auditory", "tactile"]
  },
  "time": {
    "chronology": "nonlinear_with_flashback",
    "flashback_trigger": "sensory_object",
    "time_skips": ["5_year_skip_act_2", "single_morning_expanded"]
  },
  "revelation": {
    "disclosure_schedule": ["setup_act1", "partial_act2", "reframe_act3"],
    "recontextualization_target": "the_founders_original_decision",
    "surprise_type": "inevitable_in_hindsight"
  },
  "perspective": {
    "focalization": "third_limited_protagonist",
    "fourth_wall": "none",
    "narrator_distance": "close",
    "reader_address_frequency": 0.0
  },
  "style": {
    "dialogue_to_narration_ratio": 2.95,
    "sensory_density": 3.5,
    "sentence_length_variance": "high",
    "paragraph_rhythm": "short_long_medium"
  }
}
```

### Human-Range Targets Built Into Blueprint

Every blueprint automatically targets human-range scores:

| Dimension | Target Range | How Blueprint Achieves It |
|-----------|:-----------:|--------------------------|
| Moral Polarity | 55-70% ambivalent | Resolution has real cost; no pure heroes/villains |
| Subplot Integration | 40-55% with subplots | At least 1 parallel subplot for texts >3000 words |
| Embodied Tropes | <45% of emotional expression | Behavioral actions + explicit labels preferred |
| Thematic Explicitness | <3.40 | Theme delivered through action, not narrator commentary |
| Chronological Discontinuity | >2.30 | At least 1 temporal disruption (flashback, time skip) |
| Dialogue Ratio | >2.85 | Dialogue-heavy scenes balanced with narration |
| Character Introduction | <35% external description | Characters revealed through action and dialogue |
| Setting-Mood Link | <3.70 | Weather decoupled from character emotion |

## Step 3 — Generate the Narrative

With the blueprint locked, generate the narrative:

```bash
python3 scripts/narrative_generator.py \
  --brief brief.json \
  --blueprint blueprint.json \
  --output story.md \
  --style-presets "grounded,no-em-dashes,no-purple-prose"
```

### Generation Rules (Enforced During Writing)

These rules prevent the 20 AI-Elevated Traps identified by StoryScope:

**Theme & Morality (Structure Dimension)**
- Never write a paragraph that summarizes what the story "means" or "teaches"
- Never end with the narrator reflecting on the lesson learned
- If the protagonist makes a "right" choice, show what it costs them
- If there's a moral question, let it remain partially unresolved
- Reference real-world events, books, or cultural touchstones by name (not vague allusions)

**Character Expression (Agent Dimension)**
- Maximum 1 embodied trope per 1,000 words ("throat tightened" etc.)
- Prefer: behavioral actions ("she set down the glass very carefully"), explicit labels ("he was afraid"), or dialogue that implies emotion
- Introduce every character through what they DO or SAY, not what they look like
- Characters should have contradictory traits — no purely consistent personalities

**Plot & Pacing (Event + Plot Dimensions)**
- Break the causal chain at least once — include a coincidence, interruption, or parallel event that doesn't directly cause the next scene
- Never resolve the central conflict through protagonist choice alone — external factors, other people's decisions, or systemic forces must play a role
- Avoid internal epiphany as resolution mechanism — change should come through accumulated experience, not sudden understanding
- Include at least one scene where nothing "happens" externally — a quiet plateau in the tension curve

**Time & Revelation (Time + Revelation Dimensions)**
- Include at least one temporal disruption: a flashback triggered by a sensory detail, a time skip the reader must navigate, or a scene that begins near the end and rewinds
- Design at least one revelation that forces re-reading earlier scenes with new understanding
- Surprise should feel inevitable in hindsight — not a "gotcha" that contradicts what came before

**Setting & Sensory (Setting + Style Dimensions)**
- Weather should NOT mirror character mood in more than 1 scene
- Sensory details should be selective (2-3 per scene), not exhaustive
- Vary sensory modality — don't default to visual; include auditory, tactile, olfactory (but not in every scene)
- Move through at least 3 distinct locations in medium-length narratives

**Dialogue & Perspective (Style + Perspective Dimensions)**
- Dialogue should include: fragments, interruptions, people talking past each other, saying things they don't mean, trailing off
- Never write dialogue where characters debate philosophy in complete, well-reasoned paragraphs
- Narrator should be close to the protagonist — not distant and retrospective
- Minimize narrator commentary on the meaning of events

### Style Presets

| Preset | What It Enforces |
|--------|-----------------|
| `grounded` | No purple prose, no overwrought metaphors, concrete detail preferred |
| `no-em-dashes` | Replaces em dashes with commas, periods, or restructured sentences |
| `no-purple-prose` | Blocks flowery/ornate language; targets Hemingway-level clarity |
| `dialogue-heavy` | Pushes dialogue ratio above 3.2 |
| `literary` | Higher bar for temporal complexity, moral ambiguity, and intertextual references |
| `commercial` | Tighter pacing, clearer stakes, more accessible language |
| `minimal` | Short sentences, sparse description, maximum subtext |

## Step 4 — Self-Score and Verify

After generation, the generator automatically runs the auditor to verify all 30 features:

```bash
python3 scripts/narrative_self_scorer.py \
  --input story.md \
  --blueprint blueprint.json \
  --output verification.json
```

### Verification Output

```markdown
# Narrative Quality Verification

**Genre:** brand-origin | **Length:** 3,847 words | **Blueprint Compliance:** 94%

## Dimension Scores (Target: Human Range)

| Dimension | Score | Human Range | Status |
|-----------|:-----:|:-----------:|:------:|
| Agent — Embodied Tropes | 32% | <45% | ✅ Pass |
| Agent — Character Intro | 22% ext. | <35% ext. | ✅ Pass |
| Plot — Subplots | 1 parallel | 40-55% have | ✅ Pass |
| Plot — Moral Ambiguity | 62% | >55% | ✅ Pass |
| Structure — Moralizing | 3.18 | <3.40 | ✅ Pass |
| Time — Linearity | 2.41 | >2.30 | ✅ Pass |
| Style — Dialogue Ratio | 2.98 | >2.85 | ✅ Pass |
| Setting — Weather Mirror | 3.42 | <3.70 | ✅ Pass |
| Revelation — Recontextualization | 3.21 | >3.15 | ✅ Pass |
| Perspective — Narrator Visibility | 48% | <55% | ✅ Pass |

**Overall: 28/30 features within human range (93%)**
**Residual flags:** Sensory density slightly elevated (3.71 vs target <3.75), spatial granularity slightly high (2.38 vs target <2.35)
**Verdict:** PASS — Narrative is within human structural range
```

### If Verification Fails

If any critical feature falls outside human range, the generator offers a revision pass:

```bash
python3 scripts/narrative_revision_engine.py \
  --input story.md \
  --verification verification.json \
  --fix-features "sensory_density,spatial_granularity" \
  --output story-revised.md
```

The revision engine surgically rewrites only the sections that score outside human range, preserving the plot, characters, and tone. Maximum 3 revision passes before flagging for manual review.

## Output Formats

Narrative Architect produces:

| Format | Description | Best For |
|--------|-------------|---------|
| **Fiction & Short Stories** | Multi-dimensional character arcs with temporal complexity and implicit themes | Creative writing, anthologies, portfolio pieces |
| **Brand Origin Narratives** | Founder stories with real struggles, trade-offs, and pivotal decisions — no corporate mythologizing | About pages, pitch decks, press kits |
| **Executive Case Studies** | Customer growth stories with real stakes, implementation friction, and measurable outcomes | B2B marketing, sales enablement |
| **Video & Podcast Scripts** | Scene-by-section narrative blueprints optimized for spoken delivery | YouTube, podcast intros, keynote presentations |
| **Speech & Keynote Narratives** | Personal stories designed for live delivery with natural speech rhythms | Conference talks, TED-style presentations |

## Genre-Specific Generation Patterns

### Brand Origin Stories

| Feature | Standard AI Pattern | Narrative Architect Pattern |
|---------|-------------------|---------------------------|
| Opening | "Founded in [year] with a vision to..." | Starts with a specific moment of crisis or decision |
| Struggle | Generic "challenges along the way" | Named specific failure with concrete details |
| Resolution | "Today we're proud to serve X customers" | Partial resolution with acknowledged ongoing tension |
| Theme | Stated explicitly in final paragraph | Emerges through choices and consequences |
| Founder | Flawless visionary hero | Mixed — stubborn AND insecure, brilliant AND wrong sometimes |

### Executive Case Studies

| Feature | Standard AI Pattern | Narrative Architect Pattern |
|---------|-------------------|---------------------------|
| Client intro | "Company X was facing Y challenge" | Opens with a specific moment — a bad quarter, a lost deal, a 2am call |
| Solution | "We implemented our proven methodology" | Shows implementation friction — what went wrong, what was adapted |
| Results | "200% ROI in 6 months" | Results with context — what it cost, what was sacrificed, what's still uncertain |
| Quote | "They transformed our business" | Specific, imperfect quotes — "It was messy but it worked" |
| Timeline | Linear progress | Setbacks, pivots, moments where it almost didn't work |

## Scripts

| Script | Role |
|--------|------|
| `scripts/narrative_brief_designer.py` | Takes a raw prompt and produces a structured brief with genre, length, tone, POV, and dimension defaults. |
| `scripts/blueprint_designer.py` | Designs the 10-dimension structural blueprint targeting human-range scores. |
| `scripts/narrative_generator.py` | Generates the narrative following the blueprint with all 8 transformation rules enforced. |
| `scripts/narrative_self_scorer.py` | Scores the generated narrative across all 30 features and verifies human-range compliance. |
| `scripts/narrative_revision_engine.py` | Surgical revision of specific features that fall outside human range. |

## References

- `references/storyscope_generation_patterns.md` — How each of the 30 features should be calibrated during generation (vs. during post-hoc humanization). Generation targets differ from humanization targets.
- `references/genre_blueprints.md` — Pre-designed structural blueprints for 10 genres. Each blueprint has dimension targets, subplot structures, and temporal patterns optimized for that genre.
- `references/brand_narrative_patterns.md` — Specific patterns for brand origin stories, case studies, and executive bios. Includes anti-patterns (corporate mythologizing, false humility, vague struggle narratives).
- `references/dialogue_craft_guide.md` — How to write human-sounding dialogue: fragments, interruptions, subtext, talking past each other, saying things you don't mean. Includes before/after examples for each pattern.
- `references/temporal_structure_patterns.md` — Flashback triggers, time skip techniques, frame narrative structures, in-medias-res entry patterns. How to build temporal complexity without confusing the reader.

## Configuration

| Setting | Options | Effect |
|---------|---------|--------|
| `--genre` | 10 genres | Sets dimension targets and structural patterns |
| `--length` | `flash`, `short`, `medium`, `long` | Affects subplot count, location variety, character depth |
| `--pov` | `first`, `second`, `third-limited`, `third-omniscient`, `rotating` | Narrative voice and focalization |
| `--time-structure` | `linear`, `nonlinear`, `in-medias-res`, `frame-narrative`, `episodic` | How time flows through the narrative |
| `--theme-approach` | `implicit`, `semi-explicit`, `explicit` | How the theme is delivered (implicit = human-preferred) |
| `--moral-complexity` | `high`, `medium`, `low` | How ambiguous the moral decisions are |
| `--style-presets` | `grounded`, `no-em-dashes`, `literary`, `commercial`, `minimal` | Prose style constraints |
| `--verify` | `true`/`false` | Whether to self-score after generation |
| `--auto-revise` | `true`/`false` | Whether to automatically revise features outside human range |

## Companion Skill

This skill is designed to work alongside the **[Narrative Humanizer](https://github.com/austismkeller-create/narrative-humanizer)**:

| Situation | Use |
|-----------|-----|
| Writing a new story/narrative from scratch | **Narrative Architect** (this skill) — generates structurally human text from the start |
| You have existing AI-written text that needs humanizing | **Narrative Humanizer** — detects and fixes structural AI tells in existing text |
| You want maximum quality | Generate with Narrative Architect → refine with Narrative Humanizer |

## Anti-Patterns

- **Generating without a blueprint** — Jumping straight to prose without designing the 10-dimension structure first produces the same AI patterns this skill is designed to avoid. Always blueprint first.
- **Over-controlling the story** — The blueprint is a structural skeleton, not a straitjacket. Characters should surprise you. If the blueprint says "linear" but the story demands a flashback — follow the story.
- **Corporate brand stories** — Brand origin stories should have real failure, real doubt, real trade-offs. "We saw a gap in the market and executed flawlessly" is not a story — it's a brochure.
- **Forcing all 10 dimensions equally** — Some dimensions matter more in some genres. A thriller doesn't need as much temporal complexity as literary fiction. Weight dimensions by genre.
- **Ignoring the verification step** — Always verify. Without self-scoring, you don't know if the generation actually achieved human-range scores. The whole point of this skill is measurable structural quality.
- **Making characters too ambiguous** — Moral ambiguity is human, but characters still need to be compelling. "Everyone is equally right and wrong" produces flat, unengaging narratives. Give characters strong opinions — then challenge them.

## Storage

All data is local-first:
- `~/.narrative-architect/briefs/<hash>.json` — saved narrative briefs
- `~/.narrative-architect/blueprints/<hash>.json` — saved structural blueprints
- `~/.narrative-architect/stories/<hash>.md` — generated narratives
- `~/.narrative-architect/verifications/<hash>.json` — quality verification reports

No telemetry. No cloud sync.

## Trigger Phrases

- "write a story", "generate narrative"
- "brand story", "origin story", "founder story"
- "case study narrative", "customer story"
- "write fiction", "short story"
- "narrative architect", "StoryScope generation"
- "human-grade story", "write like a human"
- "executive bio", "keynote narrative"
- "video script story", "podcast narrative"

## Dependencies

- **stdlib-only** for all 5 scripts — no `pip install` required
- **Optional**: text output via `--output` (file path) or stdout (pipe)

---

**Version:** 2.0.0
**Research Basis:** StoryScope: Investigating idiosyncrasies in AI fiction (Russell, Rajendhran, Pham, Iyyer, Wieting — COLM 2026, UMD & Google DeepMind). arXiv:2604.03136.
**Companion:** [Narrative Humanizer](https://github.com/austismkeller-create/narrative-humanizer) — for post-hoc humanization of text not generated with this skill.
**License:** MIT
