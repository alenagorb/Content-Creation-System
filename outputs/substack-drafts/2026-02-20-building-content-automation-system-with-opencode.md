# From Notes to Posts: Building My Content Automation System

### How I built a system that writes first drafts in my voice (so I don't have to give up Substack).

[Alena Gorb](https://substack.com/@savvysloth)  
Feb 17, 2026  
![A cartoon sloth sitting at a laptop, looking thoughtful, with coffee beside it. The screen shows a document with text and a lightbulb icon, suggesting content creation. Generated using Pollinations.ai](/)

---

Hello, hello, beautiful people, and welcome to Part 1 of my latest automation experiment: building a content creation assistant that captures my actual voice 🦥.

Yes, we're doing another automation series. No, I'm not satisfied with just automating external processes. This time, I'm automating my own content creation. Because apparently, I'm exactly the kind of person who builds a complex system to solve a problem they could have just... solved differently.

But here's the thing: I've got a new job that leaves me with roughly zero time for Substack. That's a problem because I didn't want to give it up. So I did what any automation-obsessed person would do: I built a system to write my posts for me.

The catch? It needed to sound like me. Not some generic AI. My actual voice with all the sarcasm and random side thoughts.

If you've ever tried to get an AI to replicate your writing style, you'll know this is harder than it sounds. The first few attempts were... rough. Very rough.

But I'm getting ahead of myself. Let's start from the beginning.

---

#### The "WHY": Project Goals & Objectives

Three months ago, I started a new role as a Systems Consultant at an AI-powered data management and automation start-up. It's brilliant. I get to work with automation tools all day, learn new things constantly, and honestly, I'm genuinely excited about the work.

The trade-off? My free time evaporated.

Before the new job, I was spending roughly 4 hours per Substack post. That included drafting, editing, adding my jokes and random side thoughts, formatting, and scheduling. It was a solid chunk of my weekend, but it was my creative outlet. I loved it.

Now? By the time I finish work, cook dinner, and do all the mundane life admin that piles up, I'm left with maybe 30 minutes before I need to crash. Not exactly enough time for thoughtful content creation.

I faced a simple choice: either cut back on Substack (maybe to one post a month, or stop entirely), or find a way to work smarter.

I'm not great at working smarter. I'm much better at working harder. But this time, even I had to admit that approach wasn't going to scale.

So I started thinking about automation.

Here's what I wanted from this project:

- A system that could take my rough notes and turn them into a first draft that captured my actual voice
- Something I could review in 30-60 minutes, add my specific jokes and tangents to, and hit publish
- Zero budget (because I'm a Systems Consultant now, not a millionaire)
- A first draft that was at least 80% of the way to being publishable

I also had a secondary goal: document the entire process so you could replicate it if you wanted to. Because that's kind of what I do here.

---

#### The "WHAT": System Design & Overview

Let me be clear about what I was and wasn't looking for.

I didn't want a content generator that spat out generic AI waffle. I didn't want something that would make me spend hours rewriting from scratch. The whole point was to save time, not create more work.

What I needed was this: a system that could read my rough notes and transform them into a post that sounds like me.

Here's what the high-level flow looks like:

**Rough Notes → Read & Understand → Transform to Draft → Format for Platforms → Review & Publish**

Simple, right?

The challenge was making the "transform to draft" step actually sound like me. That's where the real work happened.

---

#### The "HOW": Tool Selection Decision-Making

Here's what I've learned from years of building automation systems: the more complex you make something, the more likely it is to break in ways you don't expect.

My first instinct was to build something elaborate. Connect my notes to an API, set up vector embeddings for semantic search, create a multi-stage pipeline with separate nodes for research, drafting, editing, and formatting. You know, proper engineering.

But I kept coming back to a simpler question: what actually needs to happen for me to have a usable first draft?

The answer was surprisingly straightforward. I write rough notes in various places (Notion, Apple Notes, sometimes just a text file when I'm being particularly disorganised). Those notes contain the core ideas, some links, maybe a few half-formed thoughts. What I need is for someone (or something) to read those notes and transform them into a post that sounds like me.

So I stopped trying to over-engineer it and focused on three core functions:

1. Reading and understanding my notes
2. Transforming them into a structured draft
3. Formatting for my specific platforms

For this project, I used the following tools:

**🤖 For AI Processing:**

- OpenCode (free tier) as my automation environment
- Claude as the AI model for generation and conversation

**📝 For Note-Taking:**

- Notion for structured notes
- Apple Notes for quick captures
- Text files for random thoughts

**📄 For Draft Management:**

- Markdown files for version control
- Git for tracking changes

The key constraint here was budget: zero. I'm a Systems Consultant now, but I'm not made of money. And honestly, if I'm going to pay for something, I'd rather pay for a subscription that gives me the exact output I need rather than building my own from scratch.

But I'm also the person who spent an entire weekend building a custom Notion dashboard for tracking coffee shop inventory. When the mood takes me, I enjoy this kind of thing. So building it myself was partly about cost savings and partly about curiosity.

---

#### The "HOW": Ideal Tools Stack

Based on my requirements and after some experimentation, here's what I settled on:

| Tool | Purpose | Cost |
|------|---------|------|
| OpenCode | Automation environment | Free |
| Claude | AI generation | Free tier |
| Notion | Note storage | Free |
| Apple Notes | Quick captures | Free |
| Text files | Random thoughts | Free |

Total cost: £0

As you can see, the minimal version of this workflow costs nothing to set up. That's important to me because I wanted to prove the concept before investing in any paid tools.

The free tier of Claude (via OpenCode) gave me enough to test the approach. And honestly, the constraints pushed me toward simpler solutions that turned out to work better anyway.

---

#### The Real Challenge: Capturing My Voice

Now here's where things got interesting. And by interesting, I mean frustrating.

The first time I ran my notes through the system, the output was technically correct. It had the right structure. It covered the key points. It even used some of my phrases.

But it read like... AI. You know the type. Clean, polished, utterly soulless. The kind of writing that's technically proficient but has all the personality of a terms and conditions document.

This was the moment I realised I'd underestimated the problem. Getting an AI to sound like a generic content writer is easy. Getting it to sound like me specifically? That's much harder.

My writing has a specific voice. It's honest, sometimes self-deprecating, occasionally sarcastic, and I like to think it's practical rather than theoretical. I make jokes that probably aren't funny. I go on tangents. I use parenthetical asides (like this one) to add colour rather than just information.

None of that comes naturally to an AI. It's trained on the internet, which means it's trained on "professional" writing. The exact opposite of my chaotic, conversational style.

I needed to teach it. And that meant figuring out how to capture what makes my voice... mine.

---

#### The "HOW": Initial Setup Checklist

In the final part of this post, I'll briefly go over the initial setup steps so you can follow along if you want to replicate this:

✅ **Set up your OpenCode account** (it's free).

✅ **Get your Claude API access** through OpenCode's integration.

✅ **Create a notes system.** I use Notion, but you could use Apple Notes, a folder of text files, or whatever works for you. The key is consistency: always capture ideas in the same place.

✅ **Gather writing samples.** Collect 5-10 posts that represent your voice well. These will be used to train the system on your style.

✅ **Define your content pillars.** Know what topics you cover and in what proportions. This helps the system understand context.

Next week, I'll walk through exactly how I built the voice prompt system that makes the AI sound like me. That's where the real magic (and frustration) happened.

---

If you want to follow along (and learn what actually works in AI automation), subscribe below and share with friends and colleagues who might enjoy this experiment.

[Subscribe button]
[Share button]

And if you have automation challenges you'd like to see me tackle, reply to this email, drop a comment, or join my subscriber chat and let me know.

[Subscriber chat embed]

Follow me on LinkedIn, where I'll also be posting interesting and fun tidbits.
