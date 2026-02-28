# Raw Notes

Drop your unstructured automation notes, brain dumps, tool discoveries, experiment observations, and random ideas here. No structure required.

The agent reads this file and transforms it using `skills/ideas-transformer/SKILL.md`.

---

## How to Use

Just write. Paste. Dump. The messier the better.

**Useful habits (optional):**
- Date-stamp each session with a `---` divider
- Note if something is unverified: "haven't tested this yet"
- Include real numbers when you have them: hours, costs, savings
- Capture the emotion: frustrated, surprised, vindicated, confused

---

## Archive

Processed notes are NOT deleted from this file. They're marked with a `✅ Processed: [DATE]` stamp at the top of each block. This lets you reference what was captured and when.

---

<!-- Add your notes below this line -->
# Raw Notes

## 2026-02-17: Building the Content Creation Agent
-I've recently got a new job as a Systems Consultant at an AI-powered data mangement and automation start-up but it means I have much less time for Substack (but I don't want to give up on it)
-so the goal of this project is to build me a system which can generate the first draft of my posts from my messing notes but in Savvy Sloth style and language, so I don't have to do so much editing on it to make it sound like "me" that I end up rewriting the whole thing anyway. I don't have time for this
-the budget is ideally zero for this project. the time: well I need this ASAP, otherwise, I'll be out of content (crying face), and quality I want decent so I don't have to rewrite the whole thing: just add my jokes and random side thoughts at the end and not spend more than 30 mins-1 hour on the review
---
- spent the last 3 days building out a complete content creation system with Claude in VSCode and OpenCode 
- started wanting to automate Notion → content generation, but my Notion was too messy for any reasonable data extraction: just endless wall of text ideas but not much structure
- tried using Manus agent to organise my messing Notion: asked it to orgnise pages without deleting anything, but guess what? It deleted half of my pages. Thank the coding gods for restore functionality
- also realised that I actually something that takes my messy automation notes and turns them into proper 
content briefs. the notes i capture after experiments are always chaotic - half-formed 
thoughts, numbers scattered everywhere, emotional reactions mixed with technical details
- also not sure how after the Notion + Manus fiasco, I feel about giving agents access to my API keys etc. let's stick with MD files for the time being
- but despite all that mess, Manus actually managed to build me a Content Strategy for Savvy Sloth doc based on the info in my Notion which was pretty good starting point. I used this later as part of the inputs to Claude which generated the 3 brand doc files for me.
---
-built a custom skill with Cluade called ideas-transformer that reads my brand guidelines, content 
pillars (AI Experiments 30%, Workflow Breakdowns 30%, Tool Reviews 25%, Transparency 15%), 
and SEO strategy, then transforms raw notes into structured briefs with:
- 3 title options ranked by SEO + voice fit
- opening hooks written in my actual voice
- linkedin angles that aren't just summaries
- substack notes that are casual/vulnerable
- pillar classification and series vs standalone decisions

---
the whole system now lives in vscode with opencode. 3 core prompts:
1. transform raw notes → structured briefs
2. generate substack post from brief  
3. generate linkedin + notes from brief

-realised halfway through that i was overcomplicating the analytics side. I was considering using LinkedIn API but then considering notorious complexities with accessing LinkedIn via external tools, I decided manual export is easier for now.
-was considering using substack-api library in TypeScript (unofficial API as I understand since Substack doesn't have an official one yet?), so again decided to just manually export substack csvs weekly rather than fight with the unofficial api. sometimes the low-tech solution is 
the right intermediary solution which you can build on later on - no need to overcomplicated at this stage

---

- also discovered gemini gems can be used to create or even come up with brand guides and documentation. I used Claude to generate my brand docs through a long chat, but so that other people can also simulate this process and I can share it easily packaging into Gems seemed like a good option (Custom GPT might've been better, but you have to pay for OpenAI subscription which I don't have) 
- built a complete system that analyses writing samples and derives voice patterns, formatting preferences, content pillars, everything. takes like 20 minutes vs the usual 20 hours of documenting 
your brand. created 5 knowledge files (well Claude created these, and I just edited those slightly) that help users who don't have strategies:
- content strategy framework
- voice development guide  
- platform best practices (2024-2026 algorithm insights)
- seo & keyword research
- audience analysis framework

-the gem asks for 2-3 writing samples and 4 basic questions (brand name, platforms, goals, 
audience) then intelligently derives everything else. pulls from the knowledge files only 
when there are gaps. produces product-marketing-context.md, brand-guidelines.md, and 
seo-best-practices.md - the exact three files the content agent needs
- note to self (and users): don't use Deep research or Thinking setting for models - they start overcomlicating the process and the briefs; just use the defaul and fast model and you should get a good starting point

-could see this being useful for other people setting up ai-powered content systems. most 
guides assume you already have brand docs that also work as an input for agents. but it's all the context that you need to provide that is really the messy and time-consuming part because you need to actually sit down and think about your brand
- I've done this exercise for Savvy Sloth which now has those brand docs, but it took a while (maybe 2 days on and off) just thinking about my audience, goals etc.

---

interesting meta observation: i'm now using ai to help people use ai to create content 
about using ai. does look like we're getting lost in this AI matrix but also it's 
genuinely solving a real problem - most creators have their voice in their writing, not 
in documented guidelines. extracting that voice automatically is valuable

---

folder structure ended up clean:
- ideas/ (raw-notes.md → content-ideas.md)
- outputs/ (substack-drafts/, linkedin-posts/, substack-notes/)
- skills/ (just ideas-transformer, deleted the redundant ones)
- prompts/ (transform-ideas.md, weekly-batch.md)
- brand files at root

-realised i had duplicate skills doing similar things (social-content, content-repurposing, 
copywriting all overlapping - I wanted to try out pulling skills from Vercel's skills.sh website in the first stance to test those out). Claude instead created ideas-transformer to consolidate all of them. one skill to rule them all

---
- I was debating which software to use for agents: most people seem to really like Claude Code, but you don't get a free tier and have to pay. I'm not ready to commit. OpenClaw is just scary from the security point of view so I didn't even touch that. Codex you also gotta pay. OpenCode seemed like the best free alternative (although some people on Reddit didn't like that it doesn't constantly ask for permissions - not sure how true this is though)
- I'm using the free models OpenCode offers for now. Might try a local Ollama model for an experiment to avoid paying but potentially have better outputs
---

## 2026-02-24: Building the Content Creation Agent
- The first part draft was OK, the agent got the basic language, spelling, and punctuation pretty spot on. The homour part was surprising good actually - I really loled when it said that AI writing has the "personality of terms and conditions document" that is something I'll say for sure.
- The content itself though needs a bit more work: the writing is a bit too assertive at times, whereas with me being a scientist, I like to stay a bit more on cautious side when it comes to making statements. Might be something worth tweaking or implementing the review cycle as well.  

---
- Also I realised I didn't even quite understand what AI agents are properly and especially how they work in OpenCode. OpenCode docs really helped: turns out there are two built-in agents "Build" and "Plan" that are pretty general purpose, but you can add custom agents too. Pretty handy knowledge. 

---
- Thinking about the series structure it could follow something like:
    - Part 1: project goals and objectives + tools
    - Part 2: developing your brand guide (that's where I can talk about how I used Claude to help me but created a Gemini Gem so my readers can try to replicate this process as well) 
    - Part 3: not sure on that one yet, but probably the first iteration of my agent with the brand docs from part 2; no reviews or analytics just yet, only the writing samples and brand docs really. I can include my story with Manus and why I'm reluctant to allow agents assess to my Notion (because Manus deleted half of the files even when I explicitly told it not to)
    - Part 4: the results of using the first basic version of the agent, learnings, and potential improvements
    - Part 5 (paid): step-by-step setup of more advanced content writing agent - I still need to build this, but maybe some Notion integrations and some analytics + review cycle for constant improvements? TBC for now I guess 

---
- When I was creating my brand guideline documents for Savvy Sloth, I actually went back and forth with Claude on these (I provided Claude with writing samples and Savvy Sloth context).The idea for the three files came from the social-content skill that I originally downloaded from Vercel skills portal but didn't end up using because Claude generated a custom skill for me instead. I downloaded the files Claude generated and edited them directly myself. This was the most time consuming part because it really made me thinking about what actually makes Savvy Sloth, well Savvy Sloth, what I want to achieve, and how my writing differentiated from the rest. It was quite a fun exercise actually, and the review was the most important part because everything else was pretty much done by Claude.