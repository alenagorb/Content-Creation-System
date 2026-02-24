# Transform Ideas Prompt

## When to Use This Prompt

Run this whenever you have a batch of raw notes, brain dumps, or unstructured observations from your automation experiments. It transforms them into structured content briefs ready for scheduling.

---

## How to Run

### Option A: Notes in a file
Place your raw notes in `ideas/raw-notes.md` (one dump per session is fine, date-stamped). Then use this prompt:

```
Read skills/ideas-transformer/SKILL.md carefully.

Then read these context files in order:
- product-marketing-context.md
- brand-guidelines.md
- seo-best-practices.md
- ideas/content-ideas.md (to check for duplicate topics)

Then read ideas/raw-notes.md.

Transform the raw notes into structured content briefs following the SKILL.md instructions exactly. Save the output to ideas/content-ideas.md, appending to any existing content rather than overwriting it.
```

### Option B: Notes pasted directly
If you want to paste your notes inline without saving a file first:

```
Read skills/ideas-transformer/SKILL.md carefully.

Then read these context files in order:
- product-marketing-context.md
- brand-guidelines.md
- seo-best-practices.md
- ideas/content-ideas.md (to check for duplicate topics)

Here are my raw notes:

[PASTE YOUR NOTES HERE]

Transform them into structured content briefs following the SKILL.md instructions. Save the output to ideas/content-ideas.md, appending rather than overwriting.
```

---

## What the Agent Will Do

1. Read the SKILL.md to understand the transformation rules
2. Load your brand context (voice, pillars, SEO rules)
3. Check existing content-ideas.md to avoid duplicates
4. Extract every distinct idea from your raw notes (nothing gets discarded silently)
5. For each idea, produce:
   - Content pillar classification
   - Series vs standalone decision
   - 3 title options (SEO-optimised, ranked)
   - Subtitle (120-160 chars)
   - Opening hook (written in your voice)
   - 2-3 LinkedIn post angles (not summaries — distinct value moments)
   - 3-5 Substack Notes angles (casual/vulnerable tone)
   - SEO keywords and search intent
6. Produce an end-of-output summary with:
   - Pillar balance check
   - Scheduling estimate
   - Priority order recommendation
   - Gaps and suggestions for next capture session

---

## Tips for Better Raw Notes

The messier your notes, the better this works — it's designed for that. But a few habits make the output stronger:

**Include real numbers when you have them**
"took about 3 hours" → "took exactly 2h45"
"saves me time" → "saves me ~45 minutes per debugging session"
"costs something" → "costs $12/month"

The hook-writing step pulls directly from these details. Vague notes produce vague hooks.

**Capture the emotion**
"fixed the bug" vs "spent three hours on it then felt vindicated when the one-line fix worked"
The emotional arc is what makes Savvy Sloth posts feel real. If you felt frustrated, curious, surprised, or delighted — write that down.

**Don't worry about structure**
You can mix completely different topics in one note dump. The agent separates them. Date-stamping each block helps but isn't required.

**Mark things as unverified if they are**
"this is a hunch" or "haven't tested this yet" — the agent will flag these correctly rather than turning guesses into advice posts. This is important for brand integrity.

---

## Example Raw Note Formats That All Work

**Diary-style:**
```
Wednesday was annoying. Spent most of the evening fighting with the notion api
which apparently doesn't support nested database properties in zapier. had to
switch to make. feels like a step backward but actually make's notion integration
is much cleaner. might do a post on this.
```

**Bullet dump:**
```
- firecrawl: free apify alternative, better markdown output, rate limits on free tier
- n8n merge node: use before any shared action node in parallel branches
- make pricing: $29/mo starter, n8n community free — which is actually better for beginners??
```

**Tool discovery note:**
```
found perplexity api yesterday. tried it for the news tracker. much better than
google news scraping — structured results, no HTML parsing needed, $5 for 1000
queries. probably a better tool for the pharma news project than jina ai.
```

**Philosophical observation:**
```
keeps coming up in comments: "will AI take my job". i think people are asking
the wrong question. the real question is whether the people in their industry
learn to use it first. not sure if this is a substack post or just a note.
```

All of these will produce properly structured briefs.

---

## What to Do With the Output

Once the structured briefs are saved to `content-ideas.md`, you have several options:

**Schedule immediately:**
```
Read ideas/content-ideas.md and create a 4-week content calendar in 
ideas/weekly-schedule.md that follows the publication cadence in 
product-marketing-context.md. Use the priority order from the summary section.
```

**Generate the actual content:**
```
Read ideas/content-ideas.md and write the full Substack post for [IDEA NAME]. 
Use the opening hook from the brief, follow brand-guidelines.md for voice 
and formatting, and save to outputs/substack-drafts/[date]-[slug].md.
```

**Generate LinkedIn posts from briefs:**
```
Read ideas/content-ideas.md and write the full LinkedIn post for Angle 1 
from [IDEA NAME]. Follow brand-guidelines.md. Save to 
outputs/linkedin-posts/[date]-[slug].md.
```

**Review and select:**
Just read `content-ideas.md` yourself, pick the ideas you want to develop, 
and feed them to the content generation prompts individually.
