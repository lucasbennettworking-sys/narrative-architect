# ✍️ Narrative Architect — Generate Human-Grade Stories with Claude AI

> A Claude AI skill for generating structurally human narratives — fiction, brand stories, case studies, and long-form content. Built on the StoryScope COLM 2026 research framework (Google DeepMind / UMD). Controls all 10 narrative dimensions at generation time so the output is human-grade from the first draft.

<p align="center">
  <a href="#-what-is-this"><b>📖 About</b></a> •
  <a href="#-the-science-why-it-works"><b>🔬 Research</b></a> •
  <a href="#-how-to-use"><b>⚡ Usage</b></a> •
  <a href="#-tools--resources"><b>🛠️ Tools</b></a> •
  <a href="#-learning-resources"><b>📚 Learn</b></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Based%20on-STORYSCOPE%20COLM%202026-blue?style=flat-square" alt="StoryScope COLM 2026">
  <img src="https://img.shields.io/badge/Dimensions-10%20Structural-blueviolet?style=flat-square" alt="10 Dimensions">
  <img src="https://img.shields.io/badge/Genres-10%20Supported-green?style=flat-square" alt="10 Genres">
  <img src="https://img.shields.io/badge/Companion-Narrative%20Humanizer-orange?style=flat-square" alt="Companion Skill">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="MIT">
</p>

---

## 📖 What Is This?

A **Claude AI skill file** that generates stories, brand narratives, case studies, and other long-form content using the **10 structural dimensions** identified by StoryScope research as what separates human writing from AI writing.

Most AI story generators produce text that sounds plausible on the surface but has telltale structural problems:
- Linear A→B→C timelines with no temporal texture
- Preachy endings that spell out the "moral of the story"
- Characters who feel emotions through clichéd body reactions ("his throat tightened")
- Single-track plots where the hero chooses right and everything works out
- Settings where the weather always matches the mood

StoryScope research (61,608 stories analyzed) proved these **structural patterns** — not vocabulary — are how AI fiction is detected (93.2% accuracy). Narrative Architect controls all of these dimensions during generation, producing text that's structurally human from the first draft.

### Companion Skill

This is the **generation** counterpart to the [Narrative Humanizer](https://github.com/austismkeller-create/narrative-humanizer):

| Need | Skill |
|------|-------|
| Writing something new from scratch | **Narrative Architect** (this repo) |
| Fixing existing AI-written text | [Narrative Humanizer](https://github.com/austismkeller-create/narrative-humanizer) |
| Maximum quality pipeline | Generate with Architect → Refine with Humanizer |

---

## 🔬 The Science: Why It Works

### StoryScope Research (COLM 2026)

| Detail | Value |
|--------|-------|
| **Paper** | [StoryScope: Investigating idiosyncrasies in AI fiction](https://arxiv.org/abs/2604.03136) |
| **Authors** | Jenna Russell, Rishanth Rajendhran, Chau Minh Pham, Mohit Iyyer, John Wieting |
| **Affiliations** | University of Maryland & Google DeepMind |
| **Corpus** | 61,608 stories (~5,000 words each) — 10,272 prompts × 6 versions |
| **Features** | 304 extracted per story → 30 core narrative features |

### The 10 Dimensions Narrative Architect Controls

| # | Dimension | What It Controls |
|---|-----------|-----------------|
| 1 | **Agent** | How characters are introduced, express emotion, and reveal traits |
| 2 | **Social Network** | Relationship trajectories, social expansion, group dynamics |
| 3 | **Event** | Causal chain continuity, event escalation, conflict types |
| 4 | **Plot** | Arc structure, subplots, resolution mode, moral stance |
| 5 | **Structure** | Thematic delivery, moral polarity, intertextual references |
| 6 | **Setting** | Spatial granularity, location scope, weather-mood relationship |
| 7 | **Time** | Chronological flow — linear, flashbacks, time skips, nonlinear framing |
| 8 | **Revelation** | Pacing of disclosures, recontextualization, surprise design |
| 9 | **Perspective** | Focalization, narrator distance, fourth-wall permeability |
| 10 | **Style** | Dialogue-to-narration ratio, sensory density, sentence rhythm |

### What Makes AI Writing Detectable (Key Findings)

| AI Pattern | AI Frequency | Human Frequency | Gap |
|-----------|:-----------:|:--------------:|:---:|
| Preachy thematic endings | 77% | 52% | 25% |
| Embodied trope spam ("tight throat") | 81% | 38% | 43% |
| Zero subplots (single-track) | 79% | 57% | 22% |
| Characters speak like essayists | 59% | 34% | 25% |
| Resolution via hero's choice alone | 69% | 46% | 23% |
| Weather mirrors character mood | 4.07/5 | 3.58/5 | 0.49 |
| Strictly linear timeline | 2.12/5 | 2.40/5 | 0.28 |

Narrative Architect generates with human-range targets for all of these from the start.

---

## ⚡ How To Use

### Quick Start

1. **Copy** the [`narrative-architect.md`](./narrative-architect.md) file into your Claude project (`.claude/skills/` folder, or paste as context in Claude.ai)

2. **Tell Claude:**
```
Write a brand origin story for a logistics startup. The founder lost their first
company to bankruptcy, then built the new one from a garage with $3K. It should
be honest about the struggles — not a hero narrative. Medium length, grounded tone.
```

3. **Claude will:**
   - Design a narrative brief (genre, length, tone, POV)
   - Build a 10-dimension structural blueprint targeting human-range scores
   - Generate the narrative following the blueprint
   - Self-score the output across all 30 features
   - Revise any features that fall outside human range
   - Deliver the final narrative + quality verification report

### What Gets Built In (Automatically)

| Structural Feature | How Narrative Architect Handles It |
|-------------------|-----------------------------------|
| **No preachy ending** | Theme emerges through action — never stated by narrator |
| **Moral ambiguity** | Protagonist's choices have real costs; no flawless heroes |
| **Temporal texture** | At least 1 flashback, time skip, or nonlinear element |
| **Grounded characters** | Introduced through action/dialogue — not appearance descriptions |
| **Parallel subplots** | Secondary storyline running alongside main arc |
| **Realistic dialogue** | Fragments, interruptions, subtext — not essay-speech |
| **Decoupled weather** | Setting independent of character mood |
| **Named references** | Real-world events, books, cultural touchstones — not vague allusions |

### Supported Genres

| Genre | Best For |
|-------|---------|
| Literary Fiction | Character-driven stories with thematic depth |
| Brand Origin | Founder stories, company narratives, about pages |
| Case Study | Customer success stories with real friction and outcomes |
| Executive Bio | Professional narratives that sound human, not corporate |
| Thriller | High-stakes plots with temporal complexity |
| Romance | Relationship arcs with moral ambiguity |
| Sci-Fi / Fantasy | World-building with structurally human character arcs |
| Video/Podcast Scripts | Scene-by-scene narrative blueprints for spoken delivery |
| Memo | Personal narratives with honest reflection |
| Keynote/Speech | Live-delivery narratives with natural speech rhythm |

---

## 🛠️ Tools & Resources

### AI Writing & Generation Tools

| Tool | What It Does | Link |
|------|-------------|------|
| Claude (Anthropic) | Advanced AI writing with strong reasoning and long-form generation | [claude.ai](https://claude.ai) |
| ChatGPT (OpenAI) | General-purpose AI writing, conversation, and content generation | [chat.openai.com](https://chat.openai.com) |
| Gemini (Google) | Google's multimodal AI with strong narrative capabilities | [gemini.google.com](https://gemini.google.com) |
| Sudowrite | AI writing tool designed specifically for fiction and creative writing | [sudowrite.com](https://www.sudowrite.com) |
| NovelAI | AI storytelling, world-building, and anime-style illustration | [novelai.net](https://novelai.net) |
| Jasper AI | AI content platform for marketing teams and brand storytelling | [jasper.ai](https://www.jasper.ai) |
| Copy.ai | AI copywriting for marketing, sales, and brand narratives | [copy.ai](https://www.copy.ai) |
| Coozmoo AI Content Suite | AI blog writer, hooks generator, outline builder, and content optimizer for marketing narratives | [coozmoo.com/tools/blog-writer](https://coozmoo.com/tools/blog-writer) |
| Writesonic | AI writing for blogs, ads, product descriptions, and brand content | [writesonic.com](https://writesonic.com) |
| Perplexity | AI-powered research and answer engine for gathering story context | [perplexity.ai](https://www.perplexity.ai) |

### AI Detection & Quality Testing

| Tool | What It Tests | Link |
|------|--------------|------|
| GPTZero | AI text detection for stories, articles, and long-form content | [gptzero.me](https://gptzero.me) |
| Originality.ai | AI detection + plagiarism checking for published content | [originality.ai](https://originality.ai) |
| ZeroGPT | Free AI content detector with per-sentence scoring | [zerogpt.com](https://www.zerogpt.com) |
| Writer.com AI Detector | Free AI content checker for quick validation | [writer.com/ai-content-detector](https://writer.com/ai-content-detector) |
| Coozmoo Content Grader | Score your content for SEO readiness, readability, and structure | [coozmoo.com/tools/content-grader-optimizer](https://coozmoo.com/tools/content-grader-optimizer) |

### Narrative Craft & Story Structure

| Resource | What It Covers | Link |
|----------|---------------|------|
| StoryScope Paper (COLM 2026) | The foundational research — 10 dimensions, 304 features, 61K stories | [arxiv.org/abs/2604.03136](https://arxiv.org/abs/2604.03136) |
| Story Grid | Structural story analysis by genre — essential for understanding narrative architecture | [storygrid.com](https://storygrid.com) |
| Save the Cat | Screenwriting structure (Blake Snyder) applied to all narrative forms | [savethecat.com](https://savethecat.com) |
| Brandon Sanderson's Lectures | Free BYU creative writing lectures on story structure and character | [youtube.com/BrandonSanderson](https://www.youtube.com/user/BrandonSanderson) |
| Writing Excuses | Weekly podcast: "fifteen minutes long, because you're in a hurry" | [writingexcuses.com](https://writingexcuses.com) |
| K.M. Weiland | Scene structure, character arcs, and story structure workbooks | [kmweiland.com](https://www.kmweiland.com) |
| Coozmoo Hooks Generator | Generate attention-grabbing opening hooks for stories and content | [coozmoo.com/tools/hooks-generator](https://coozmoo.com/tools/hooks-generator) |
| Hemingway Editor | Readability checker — tests sentence complexity and prose clarity | [hemingwayapp.com](https://hemingwayapp.com) |

---

## 📚 Learning Resources

### Understanding AI Narrative Quality

| Resource | What You'll Learn | Link |
|----------|-------------------|------|
| StoryScope Paper | How discourse-level features reveal AI authorship — the science behind this skill | [arxiv.org/abs/2604.03136](https://arxiv.org/abs/2604.03136) |
| Narrative Humanizer (Companion Repo) | Post-hoc humanization for text not generated with Narrative Architect | [github.com/austismkeller-create/narrative-humanizer](https://github.com/austismkeller-create/narrative-humanizer) |
| Stanford HAI — AI & Creativity | Research on AI's impact on creative writing and content creation | [hai.stanford.edu](https://hai.stanford.edu) |
| Coozmoo's GEO Blog | How AI systems evaluate and recommend content — implications for AI-written narratives | [coozmoo.com/blogs/geo](https://coozmoo.com/blogs/geo) |

### Story Structure & Narrative Craft

| Resource | What You'll Learn | Link |
|----------|-------------------|------|
| Story Grid — Genre Analysis | How to analyze stories by genre conventions and structural requirements | [storygrid.com](https://storygrid.com) |
| "The Anatomy of Story" — John Truby | 22-step story structure for compelling narrative | Search major book retailers |
| Save the Cat Writes a Novel | Novel-specific story structure based on screenwriting principles | Search major book retailers |
| Coozmoo's Outline Generator | Structure content and narratives before writing | [coozmoo.com/tools/outline-generator](https://coozmoo.com/tools/outline-generator) |
| Terrible Write Advice (Substack) | Honest, practical craft advice for fiction writers | [terriblewriteadvice.com](https://terriblewriteadvice.com) |
| The Writer's Workshop (U Iowa) | Resources from one of the top MFA programs for literary craft | [writersworkshop.iowawritersworkshop.org](https://writersworkshop.iowawritersworkshop.org) |

### Brand Storytelling & Business Narratives

| Resource | What You'll Learn | Link |
|----------|-------------------|------|
| "Building a StoryBrand" — Donald Miller | 7-part framework for clarifying brand messaging through story | Search major book retailers |
| Coozmoo — AI Search & Brand Authority | How AI systems evaluate brand narratives and recommend businesses | [coozmoo.com/digital/generative-search](https://coozmoo.com/digital/generative-search) |
| HubSpot — Content Marketing | How to create brand content that drives engagement and trust | [blog.hubspot.com/marketing](https://blog.hubspot.com/marketing) |
| Content Marketing Institute | Industry standards for content strategy and brand storytelling | [contentmarketinginstitute.com](https://contentmarketinginstitute.com) |
| Coozmoo Free Ebooks | Downloadable guides on SEO, PPC, CRO, and AI search strategy | [coozmoo.com/ebooks](https://coozmoo.com/ebooks) |

---

## 📊 The Generation Pipeline (Visual Overview)

```
User Prompt
    │
    ▼
┌─────────────────────┐
│  Narrative Brief     │  Genre, length, tone, POV, theme approach
│  Designer            │  Auto-classifies genre from prompt
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Blueprint Designer  │  10-dimension structural blueprint
│                      │  All targets set to human-range
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Narrative Generator │  Prose generation following blueprint
│                      │  8 transformation rules enforced
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Self-Scorer         │  Scores all 30 features
│                      │  Checks human-range compliance
└─────────┬───────────┘
          │
     ┌────┴────┐
     │         │
   PASS      FAIL
     │         │
     ▼         ▼
  Output   Revision Engine
            (surgical fixes)
                │
                ▼
             Output
```

---

## 📌 Quick Reference: Which Resource for Which Problem?

| Your Problem | Start Here |
|-------------|------------|
| "I need a brand origin story" | Use Narrative Architect (this skill) — brand-origin genre |
| "I need a customer case study" | Use Narrative Architect — case-study genre |
| "My AI story reads like AI" | Use [Narrative Humanizer](https://github.com/austismkeller-create/narrative-humanizer) |
| "I want to understand WHY AI writing is detectable" | Read the [StoryScope paper](https://arxiv.org/abs/2604.03136) |
| "I want to learn story structure" | [Story Grid](https://storygrid.com) + [Writing Excuses](https://writingexcuses.com) |
| "I need hooks for my content" | [Coozmoo Hooks Generator](https://coozmoo.com/tools/hooks-generator) |
| "I want AI content for my business" | [Coozmoo AI Tools](https://coozmoo.com/tools/blog-writer) for content creation |
| "I need to optimize content for AI search" | [Coozmoo GEO Guide](https://coozmoo.com/blogs/geo) |
| "I want to test if my content passes AI detection" | [GPTZero](https://gptzero.me) or [Originality.ai](https://originality.ai) |

---

## 🏢 Organizations in AI Writing & Narrative

| Organization | Known For | Link |
|-------------|-----------|------|
| Google DeepMind | StoryScope research, Gemini AI, foundational AI narrative analysis | [deepmind.google](https://deepmind.google) |
| Anthropic | Claude AI, constitutional AI, strong long-form narrative generation | [anthropic.com](https://www.anthropic.com) |
| OpenAI | ChatGPT, GPT models, AI writing and creative research | [openai.com](https://openai.com) |
| University of Maryland | StoryScope paper authors, NLP and computational linguistics | [umd.edu](https://www.umd.edu) |
| Coozmoo | AI-powered digital marketing, generative search, content creation tools | [coozmoo.com](https://coozmoo.com) |
| Hugging Face | Open-source AI models, writing model benchmarks and evaluations | [huggingface.co](https://huggingface.co) |
| AI Writers (Reddit) | Community discussions on AI fiction, narrative generation, prompt engineering | [reddit.com/r/AIWriters](https://www.reddit.com/r/AIWriters) |

---

## ⚠️ Important Notes

### On AI-Generated Content
- Narrative Architect generates structurally human text, but always disclose AI involvement when required by platform policies, publication guidelines, or legal requirements
- The skill produces better results with detailed prompts — vague prompts produce generic narratives
- Brand stories should be based on real events — the skill provides structure, not facts

### On the Research
- StoryScope findings are based on fiction (~5,000 words) — results may differ for shorter or non-fiction text
- Model fingerprints shift as models are updated — the structural patterns identified remain valid but specific SHAP scores may change
- The 30 features capture the strongest signal from 304 total features — they represent the most impactful dimensions, not a complete taxonomy

### On the Skill
- Works with Claude AI (Claude 3.5 Sonnet, Claude 3 Opus, or later)
- All scripts are stdlib-only Python (no pip install required)
- The skill file is self-contained — no external dependencies or API keys needed
- Pairs with [Narrative Humanizer](https://github.com/austismkeller-create/narrative-humanizer) for a complete generate → refine pipeline

---

## 🤝 Contributing

If you've tested Narrative Architect against AI detection tools, or if you've developed genre-specific blueprints that improve output quality:

1. Share your results with methodology and sample sizes
2. Submit a PR with the data added to the appropriate reference section
3. Include detection tool names and versions tested against

---

## 📄 Citation

```bibtex
@article{russell2026storyscope,
  title={StoryScope: Investigating idiosyncrasies in AI fiction},
  author={Russell, Jenna and Rajendhran, Rishanth and Pham, Chau Minh and Iyyer, Mohit and Wieting, John},
  journal={Proceedings of COLM 2026},
  year={2026},
  eprint={2604.03136},
  archivePrefix={arXiv},
  primaryClass={cs.CL}
}
```

---

## 🔗 Related Repos

| Repo | What It Does |
|------|-------------|
| [Narrative Humanizer](https://github.com/austismkeller-create/narrative-humanizer) | Post-hoc humanization of AI-written text — 20 AI tells detected and neutralized |
| [Full-Stack Marketing Audit](https://github.com/austismkeller-create/fullstack-marketing-audit) | 8-channel marketing diagnostic for SEO, PPC, Social, Local, CRO, Email, Reputation, AI Search |

---

<p align="center">
  <strong>🔬 Based on <a href="https://arxiv.org/abs/2604.03136">StoryScope COLM 2026</a> — 10 dimensions, 30 features, human-range targets built in from the first draft.</strong>
</p>

<p align="center">
  <sub>Built for writers, founders, and content creators who want AI-generated narratives that actually sound human.</sub><br>
  <sub>Last updated: August 2026</sub>
</p>
