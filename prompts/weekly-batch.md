# Weekly Content Batch Generation

## Step 1: Analysis
- Read `.agents/performance-data/substack-analytics.csv`
- Identify top-performing content pillars from last month
- Check `.agents/ideas/content-ideas.md` for queued topics

## Step 2: Topic Selection
- Propose 2 topics for this week
- Ensure content pillar balance
- Verify alignment with `.agents/product-marketing-context.md`

## Step 3: Content Creation
For each topic:

### Substack Post
- Length: As described in `.agents/brand-guidelines.md`
- Structure: As described in `.agents/brand-guidelines.md`
- SEO: Apply `.agents/seo-best-practices.md`
- Voice: Match `.agents/writing-samples/`

### LinkedIn Sequence
- Post 1: Announcement (day of publication)
- Post 2: Key framework (2 days later)
- Post 3: Data insight (4 days later)  
- Post 4: Personal lesson (7 days later)

### Substack Notes
- 5 variations (teaser, data, question, quote, insight)

## Step 4: Save & Organise
- Substack: `output/substack-drafts/YYYY-MM-DD-[slug].md`
- LinkedIn: `output/linkedin-posts/YYYY-MM-DD-[topic]-[variant].md`
- Notes: `output/substack-notes/YYYY-MM-DD-[topic]-note-[1-5].md`

## Step 5: Update Tracking
- Update `ideas/content-ideas.md` (mark completed, add new ideas)