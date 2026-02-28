# From Messy Notes to Brand Voice: The Real Challenge No One Talks About

### Before you can automate your content, you need to teach AI what makes you *you*. And that's harder than it sounds.

[Alena Gorb](https://substack.com/@savvysloth)  
Feb 24, 2026

In [Part 1](https://savvysloth.substack.com/p/building-content-automation-system), I shared why I needed to build a content creation system in the first place: new job, roughly zero free time, and a Substack I wasn't ready to give up on. The goal was clear - build something that could generate first drafts in my voice without sounding like a generic AI had vomited onto the page.

But here's the thing I realised pretty quickly: you can't automate what you haven't defined.

Before my little content creation agent could write anything that sounded like me, I needed to answer a deceptively simple question. What *is* the Savvy Sloth voice? And more importantly, how do you explain that to an AI in a way it actually understands?

That's where the real challenge began.

---

#### The Brand Guidelines Problem

Most content creators don't have brand guidelines. And honestly? That's fine when you're just writing for yourself. Your voice lives in your head, in your previous posts, in the way you naturally phrase things. You don't need to document it because you *are* the brand.

But when you want to hand that voice to an AI? You're suddenly faced with a problem. You need to externalise something that's been entirely internal. You need to take years of intuitive writing decisions - tone, humour style, technical depth, formatting preferences - and turn them into something a language model can actually use.

It took me 2 days (on and off) just thinking about my audience, goals, and voice for Savvy Sloth. Most creators never do this exercise because it feels like homework. It's boring, it's abstract, and frankly, it feels a bit silly to write down things you already know in your gut.

The irony? That homework is exactly what AI needs to replicate your voice. Without it, you're asking a model to be creative without giving it any boundaries. And that way lies generic, bland, utterly forgettable content.

---

#### What Even Goes in a Brand Guide?

When I finally sat down to document the Savvy Sloth voice, I realised I had no idea what I was doing. What *should* I include? Logo colours? Font choices?

For AI content purposes, it turns out you need something different. You need what I call "voice documentation" - not the visual stuff that designers care about, but the textual stuff that writers care about.

Here's what I ended up including:

**Voice characteristics** - How do you sound? Honest? Sarcastic? Warm? Professional? For Savvy Sloth, it's a mix of honest transparency (sharing failures alongside successes), practical focus (actionable over theoretical), accessible technical writing (explain without being condescending), and slight self-deprecation (relatable, not a know-it-all).

**Sentence and paragraph structure** - This one surprised me, but it matters enormously. Short punchy sentences for impact. Longer sentences for detail. Average 15-25 words. Never more than 35 unless rhythm demands it. Break dense technical sections into 1-2 sentence paragraphs for breathing room.

**Humour style** - When do you use it? How do you use it? What do you avoid? For me, it's self-deprecating observations, playful commentary on unexpected outcomes, and occasionally pointing out industry absurdities. What I avoid is sarcasm that might read as mean-spirited, jokes at others' expense, and humour that undermines practical value.

**Content pillars** - What topics do you actually write about? What's your angle? Savvy Sloth focuses on AI experiments (30%), workflow breakdowns (30%), tool reviews (25%), and transparency/wins/fails (15%).

**Technical depth** - How technical do you get? For Savvy Sloth, the reader is comfortable with technology but not necessarily a developer. They understand concepts like APIs and workflows but may need specific terms explained.

This took me weeks to figure out. Weeks of staring at blank documents, trying to articulate things I'd never actually articulated before. And honestly? I was getting nowhere fast.

---

#### Enter Claude (My Unexpected Branding Coach)

At some point, I realised I was spending way more time on the brand documentation than on the actual automation system I was trying to build. So I did what any reasonable person would do - I asked Claude to help.

And look, I'm not going to lie - it was weird. Having a conversation with an AI about defining *my* brand voice felt slightly absurd. Was I really going to get an AI to help me explain to other AIs what makes my writing... mine?

But it worked. Kind of.

What Claude was brilliant at was asking questions I hadn't considered. "What's something you'd *never* write?" "How would your writing sound if it was a person at a party?" "What's the difference between how you write and how a corporate blog writes?"

Those questions got me thinking in ways I hadn't. And slowly, the fuzzy concept of "my voice" started becoming something I could actually write down.

We went through maybe 4-5 rounds of refining. I'd write a draft, Claude would poke holes in it ("this sounds like every other tech blog"), I'd revise, and we'd go again. It wasn't instant magic. But it was genuinely helpful.

The end result wasn't perfect. But it was a starting point - something I could actually hand to my content creation agent and say "this is what we're aiming for."

---

#### The Problem: It Still Took Forever

Here's the thing though. Even with Claude helping, this process took time. Real time. The back-and-forth, the refining, the "actually wait, let me rethink this section" moments. It was valuable, but it wasn't fast.

And that's when I started wondering: could this be automated further?

---

#### My Solution: Gemini Gems for Brand Documentation

A few weeks later, I discovered Gemini Gems (Google's version of custom GPTs, but free). And I had a thought: what if you could skip the conversational back-and-forth entirely? What if you could feed writing samples to an AI and have it *derive* your brand guidelines automatically?

So I built a Gem to do exactly that.

The concept is simple. You give the Gem 2-3 samples of your writing (published posts, maybe a newsletter or two). You answer 4 basic questions about your goals and audience. And then the Gem analyses your writing to extract voice patterns, formatting preferences, content pillars - all the things I'd spent weeks figuring out with Claude.

I tested it with Savvy Sloth content. And honestly? It got about 70-80% of the way there. The voice characteristics were surprisingly accurate. The sentence structure analysis was spot on. The content pillar breakdown made me nod along.

What it missed were the nuances - the specific jokes I make, the particular phrases I gravitate toward, the inside jokes with my audience. Those things are harder to extract algorithmically because they're not consistent across posts. They're the flourishes, not the foundation.

But here's the thing: that 70-80% is a *massive* head start. It took me 20 minutes with the Gem versus the hours (okay, fine, it was probably closer to 15 hours total) I'd spent manually documenting Savvy Sloth's voice.

---

#### Why This Matters for Your Content Automation

Here's the honest truth: if you want to build a content creation system that sounds like you, you need brand documentation. Not because AI can't write - it absolutely can - but because generic AI writing is boring and forgettable and exactly like everyone else's generic AI writing.

Your voice is your competitive advantage. And your voice needs to be defined before it can be replicated.

The traditional way to do this is painful. It's sitting down on a Sunday afternoon, forcing yourself to answer questions you'd rather just *feel* than articulate. It's weeks of iterative refinement. It's honestly kind of miserable.

The AI-assisted way (whether that's Claude helping you brainstorm or a Gem extracting patterns from your existing writing) is faster. Not perfect, but fast. And fast matters when you're trying to build something alongside a full-time job and a life.

In next week's part, I'll walk you through exactly what I included in the Savvy Sloth brand guide and show you the actual documents I use to keep my content creation agent honest. We'll also get into the technical architecture - how OpenCode and Claude work together to turn rough notes into first drafts.

Until then, if you've been putting off documenting your brand because it feels like homework... maybe AI can do your homework for you. At least the first draft of it.

---

If you want to follow along (and learn what actually works in AI automation), subscribe below and share with friends and colleagues who might enjoy this experiment.

[Share](https://savvysloth.substack.com/p/challenges-of-defining-brand-for-ai)

And if you have automation challenges you'd like to see me tackle, reply to this email, drop a comment, or join my subscriber chat and let me know.

[**Join Alena Gorb's subscriber chat**](https://open.substack.com/pub/savvysloth/chat?utm_source=chat_embed)

[Available on the Substack app and on web](https://open.substack.com/pub/savvysloth/chat?utm_source=chat_embed)

Follow me on [**LinkedIn**](https://www.linkedin.com/in/alena-gorb/), where I'll also be posting interesting and fun tidbits.
