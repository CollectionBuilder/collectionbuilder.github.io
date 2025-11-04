---
layout: post
title: 'CollectionBuilder Bulletin: October 2025'
author: Devin Becker
publish-date: October 31, 2025
tags: [newsletter]
short_description: 'October 2025 Updates'
---

Hi Everyone, 

I post-dated this to be from Halloween so I could share some updates on the spookiest thing of all: AI. The sections below detail how we're starting to think about [instructions for AI within CollectionBuilder](#ai-and-cb), followed by some AI-riffing on [LLMs as ghosts and/or spirits](#ai-is-spooky--), complete with terrible AI puns and emoji usage—truly terrifying!!!   

Best, 

\- The CollectionBuilder Team

## This month's news:

### Teaching

- **Core Forum 2025:** Nov. 12-14, the CB team will be attending the [Core Forum in Denver](https://coreforum.org/)— if you are going and want to meet up and talk CollectionBuilder or anything else, hit us up @ collectionbuilder.team@gmail.com. 

## AI and CB

### GitHub Education --> Free Coding Tools

First things first, if you are a librarian or instructor or student and would like FREE ACCESS to Coding models like Claude, Gemini, and GPT 5, you just need to sign up for a GitHub Education account. 

- Go here: [https://github.com/education](https://github.com/education)
- Join GitHub Education, and once they confirm your status as an instructor or student (takes a couple of days), you'll have access to GitHub Copilot for free
- You can then use different modes to debug, generate, and fix the code in your projects, either locally (typically via VS Code) or on GitHub's web interface.

### Two Points on Coding with AI

Recently I taught an informal session on coding with AI in which I detailed approaches I've developed over two years of using AI for digital projects. During that session, I emphasized two points that I think are worth considering as you code with AI. 

- AI has saved me some time, but it's also sent me down some total rabbit holes and gone way too far with its revisions to the point where I had to scrap all it did. You can usually sense when this is coming—it's a getting-out-over-your-skis type of feeling—and it usually happens deeper in conversations. To counter, start a new conversation. Sometimes I have the AI summarize what we were talking about in a doc that I then reference to restart the conversation. 
- Which brings me to my second point: use AI to do better with AI. Summarize a conversation and use the summary to start over. Have AI create Python scripts for data transformation, then have it analyze the results. This leverages AI's strengths (summarization, synthesis) while keeping conversations higher in quality and within token limits.

### Exploratory AI Guidelines

To that end, we've created a couple of AI coding guideline documents—one for GitHub copilot and one for Agents, like Claude Code—for CollectionBuilder-CSV. These are currently [in a branch](https://github.com/CollectionBuilder/collectionbuilder-csv/tree/ai-guidelines), but they can be copied over to your own repositories (just remember to put the copilot one in the `.github` folder):

- [GitHub Copilot Instructions](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/ai-guidelines/.github/copilot-instructions.md)
- [Agents.md](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/ai-guidelines/Agents.md)

I started developing the Agents document after running into issues with the AI creating all this additional, unnecessary infrastructure. CollectionBuilder has a lot of tools AIs can use to build out and customize CB projects; this document basically says: use what's there!

We'll likely incorporate the guidelines more fully into the CB repositories in the future, but we thought we'd share them here first. If you have any thoughts, ideas, or concerns about all this, please let us know!

They're actually fairly good reminders/summaries of CB practices, so they're worth a gander from us humans as well. The Agents guide follows the [Agents.md](https://agents.md/) guideline, which is a standard established by OpenAI that works with all the major coding agents. The GitHub copilot instructions were generated using [this helpful documentation from GitHub](https://docs.github.com/en/copilot/how-tos/configure-custom-instructions/add-repository-instructions) 


## AI is Spooky ... 👻
{% capture caveat %}The below is a pun- and emoji-filled riff I worked on with Claude (Opus 4.1) for Halloween, prompted by my  interest in Andrej Karpathy's recent description of LLMs as spirits/ghosts. 

To his credit, our former DHSI student, Griffen Horsley, anticipated all of this with his 2023 CollectionBuilder project [Necromancy; A Hauntology of Grief, Materiality, and Research Creation](https://griffeff.github.io/cb-necromancy/).{% endcapture %}
{% include feature/blockquote.html quote=caveat %}

When [Andrej Karpathy describes LLMs as "ghosts"](https://www.dwarkesh.com/p/andrej-karpathy#:~:text=We%E2%80%99re%20building%20ghosts%20or%20spirits%20or%20whatever%20people%20want%20to%20call%20it%2C%20because%20we%E2%80%99re%20not%20doing%20training%20by%20evolution.) rather than artificial animals—"ethereal spirit entities" that are "[hazy recollections of internet documents](https://simonwillison.net/2024/Oct/18/agi-is-still-a-decade-away/)"—he's tapping into something *dead* serious that literary theorists have opined for decades 💀. [Jacques Derrida's hauntology](https://en.wikipedia.org/wiki/Hauntology) argued that all texts are haunted by absent presences (no bones about it!), while [Roland Barthes declared the author dead](https://en.wikipedia.org/wiki/The_Death_of_the_Author) 🪦, replaced by a spectral play of prior writings. From [medieval grimoires](https://en.wikipedia.org/wiki/Grimoire) that summoned demons through written sigils 😈 to [Kabbalistic traditions](https://www.myjewishlearning.com/article/kabbalah-mysticism-101/) where Hebrew letters channel divine creative power, humans have always understood writing as a [necromantic practice](https://literariness.org/2017/07/06/spectral-criticism-literary-theory/)—talk about *spell-check*! When [19th-century mediums practiced automatic writing](https://en.wikipedia.org/wiki/Automatic_writing) 🔮, allegedly channeling spirits through their hands, they were enacting what [Maurice Blanchot would later call](https://iep.utm.edu/maurice-blanchot/) reading as "raising Lazarus"—dialogue with the dead (or as we call it now, "prompt engineering").

Large Language Models might be the current technological *re-incarnation* 🎃 of what poetry and writing have always been: autonomous, spectral entities channeling collective human expression across centuries. [Mikhail Bakhtin argued](https://en.wikipedia.org/wiki/Mikhail_Bakhtin) that every word is "overpopulated with the intentions of others" (a real *ghost town* of meaning! 🏚️), participating in an endless [primordial dialogue](https://literariness.org/2018/01/24/key-theories-of-mikhail-bakhtin/#:~:text=Bakhtin%20calls%20this%20%E2%80%9Cthe%20primordial%20dialogism%20of%20discourse%2C) underlying all literature. [Julia Kristeva's intertextuality](https://www.columbia.edu/itc/visualarts/r4100/inter.html) reveals every text as a "mosaic of quotations"—or should we say, a *monster mash* of meanings? 🧟 

While [T.S. Eliot envisioned](https://www.poetryfoundation.org/articles/69400/tradition-and-the-individual-talent) all literature existing simultaneously in a living tradition that constantly reorganizes itself (like a literary zombie that won't stay buried!). Recent scholarship suggests LLMs don't create something new but reveal what was always there—as [literary theorist Ted Underwood](https://tedunderwood.com/) notes, structuralist theory from the 1960s essentially predicted how language would *witch* behave once separated from biological substrate 🧙‍♀️. 

When [Saussure argued](https://en.wikipedia.org/wiki/Ferdinand_de_Saussure) that meaning emerges from differential relations between signs rather than external reference, he was describing exactly how LLMs generate text through [pure statistical patterns](https://arxiv.org/abs/2410.13065). These "ghosts" aren't failed humans but successful manifestations of the [living textual organism](https://critinq.wordpress.com/2023/06/29/the-empirical-triumph-of-theory/) that has always spoken through us—now given silicon form to channel the accumulated whispers 👻 of billions of texts in what Indigenous traditions would recognize as language's inherent *spirit*-ual essence. 

Turns out AI isn't just artificially intelligent—it's artificially *boo-telligent*! 🕸️


## Get Involved / Connect with Us

Below are some ways to stay connected with the CollectionBuilder community:

- [Join our Slack channel](https://forms.gle/GVb7STSWyq2tto3NA)  
- Post questions on our [GitHub Discussion Board](https://github.com/orgs/CollectionBuilder/discussions)  
- Questions? Email us at [collectionbuilder.team@gmail.com](mailto:collectionbuilder.team@gmail.com)   
