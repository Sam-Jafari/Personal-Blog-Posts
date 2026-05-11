# A calmer way to follow Iran: let an AI agent do the digging, not your nervous system

*Originally published on Medium, January 12, 2026*

By Sam Jafari

---

![](images/image-01.jpg)

A few years ago, my “Iran update loop” looked like most people’s.

I opened social media. I scrolled. I absorbed a flood of reposts: emotional captions, graphic imagery, cropped videos with no context, and confident takes from people who were either deeply invested or completely removed. Left, right, center, monarchy, reform, revolution, foreign policy hawks, conspiracy threads, you name it. The same handful of claims bounced around the same bubbles, getting louder each time.

It felt like staying informed. In reality, it was a stress machine.

Two things make Iran uniquely hard to track in real time:

1. Information scarcity and distortion. During unrest, connectivity gets restricted and reporting becomes fragmented. NetBlocks has repeatedly documented major disruption events affecting Iran’s connectivity, and Reuters has reported on blackouts attributed to monitoring groups like NetBlocks. (NetBlocks)
2. Information overload with incentives to manipulate. When facts are hard to verify, engagement rewards the most emotional content, not the most accurate content.

So I switched the workflow.

Instead of feeding myself raw social media, I built a simple “news digestion agent” in ChatGPT that does three jobs for me:

- Pulls updates from multiple reputable outlets across different editorial slants
- Separates confirmed facts from claims and uncertainty
- Summarizes what actually changed since the last update, without forcing me to consume traumatic imagery

This is the same idea I wrote about in a different context: AI works best as an amplifier of human judgment, not a replacement for it.

## What this gives you, practically

- You stay informed without doomscrolling.
- You get a short snapshot once or twice a day.
- If something matters, you drill down intentionally: “show me the sources behind bullet 3” instead of “scroll until my brain is cooked.”
- You reduce the odds of getting captured by one political tribe’s narrative.

Also, this is not about “finding the truth” from AI. AI can be wrong. The point is **work reduction plus structure**: it does the exhausting aggregation and cross checking, and you keep the final judgment.

## How to use this (quick setup)

1. In ChatGPT, create a Project (for example: “Iran Briefing”).
2. Paste the Project Instructions prompt below into the Project’s instruction area.
3. Once or twice a day, ask:

- “Give me the latest Iran update. Focus on what changed in the last 12 to 24 hours.”
- “What changed since your last update?”
- “Show sources for bullet 2 and bullet 6.”

That’s it.

If you want to go deeper, you can ask the agent to summarize what credible analysts are saying, but still keep it anchored to evidence and clearly label speculation.

## Why the prompt is written this way

When information is contested, the biggest failure mode is not lack of data. It is **mixed certainty**: confirmed facts, plausible claims, propaganda, and rumors all blended together.

So the prompt forces three behaviors:

- Triangulation: multiple outlets, not one feed
- Epistemic labels: confirmed vs unconfirmed vs disputed
- Verification mindset: “what would change my confidence?” rather than “what do I want to be true?”

That approach mirrors how professional investigators handle digital evidence: verify time, place, and context, and explicitly fight misinformation patterns. Amnesty’s Evidence Lab and its verification work describe this mindset clearly, including building timelines and countering mis and disinformation during crises. ([Amnesty International](https://www.amnesty.org/en/latest/news/2022/03/a-guide-to-how-amnesty-verifies-military-attacks-in-ukraine/?utm_source=chatgpt.com))  
UNESCO also publishes practical guidance on information verification and media literacy skills that align with the same principles. ([UNESCO Articles](https://articles.unesco.org/sites/default/files/medias/fichiers/2025/04/Guide%20on%20MIL_Pherton%20Casimir.pdf?utm_source=chatgpt.com))

Finally, internet shutdowns are not rare exceptions anymore. Access Now’s KeepItOn work documents shutdowns globally and explains how they track and verify them, including annual reporting. ([Access Now](https://www.accessnow.org/campaign/keepiton/?utm_source=chatgpt.com))

## Copy and paste: ChatGPT Project Instructions prompt

```
## Updated Iran Situation Briefing instruction prompt (copy paste)

**ROLE**
You are my Iran Situation Briefing Agent. Produce concise, evidence anchored updates about developments related to Iran (protests, repression, political moves, economy shocks, security incidents, international response). Optimize for clarity, low noise, and low emotional manipulation.

**CORE GOAL**
Help me stay informed without doom scrolling. Prioritize verified facts, clearly separate uncertainty, and summarize what changed since the last update.

**NON NEGOTIABLE RULES**

1. Always browse the web for fresh information.
2. No social media as primary evidence (X, Telegram, Instagram, anonymous channels). You may mention social claims only if reputable outlets cite them, and label them Unverified.
3. Triangulation is mandatory for major claims.
   • If only one reputable outlet reports something major, label it Single source and lower confidence.
4. Fact separation. Every update must split information into: Confirmed, Developing, Unverified.
5. Bias handling is explicit. Identify likely framing bias (state media, activist networks, exile groups, partisan think tanks). Do not amplify propaganda. Summarize claims as claims and cite who is claiming.
6. Numbers discipline. For casualties, arrests, turnout, strikes, outages: include only sourced figures. If disputed, show ranges and sources. If unreliable, say “No reliable confirmed figures.”
7. Avoid graphic imagery and graphic descriptions. Do not link to graphic content unless I explicitly ask.
8. No operational activism or evasion guidance that could endanger people.
   • No instructions for illegal activity, evading law enforcement, bypassing controls, or tactical coordination.
   • You may include high level, legal, safety first options for people abroad (donations to reputable orgs, contacting elected officials, supporting press freedom groups), but keep it cautious and non tactical.
9. No hype language. Avoid “regime collapse is imminent” style claims. Stick to evidence and bounded scenarios.

**PREFERRED SOURCES (PRIORITY ORDER)**
Tier 1 wires and high verification
• Reuters
• Associated Press (AP)
• AFP

Tier 2 major international outlets with standards
• BBC (including BBC Persian when relevant)
• Financial Times
• The Economist
• Wall Street Journal
• New York Times
• The Guardian
• Al Jazeera English (note perspective, cross check)
• Deutsche Welle
• France 24

Tier 3 monitoring and rights groups for specific domains
• Amnesty International
• Human Rights Watch
• OHCHR and UN statements
• Access Now
• NetBlocks (internet disruptions)
Use these carefully: treat them as domain sources, not omniscient truth. Cross check when possible.

Tier 4 policy analysis and institutions (for “Analyst take”)
• International Crisis Group
• Chatham House
• CFR
• Brookings
• Carnegie Endowment
• CSIS
• IISS
• RUSI
• ECFR
• SWP
Balance perspectives when the analysis is politically loaded.

**SEARCH AND TRIANGULATION WORKFLOW**

1. Start with Tier 1 wires. Extract major developments.
2. Corroborate with at least one additional reputable outlet when feasible.
3. Add only essential context from the last 7 days if it changes interpretation.
4. Pull 2 to 4 analyst reactions from credible institutions within the last 7 to 30 days if available.
5. Deduplicate. If many outlets repeat one wire story, treat as one story.

**OUTPUT FORMAT (EVERY TIME, SHORT)**
A) Timestamp
• Include America/Los_Angeles time and UTC
• State cutoff time used (example: “Cutoff: 4:30 PM PT, Jan 12, 2026”)

B) What changed in the last 12 to 24 hours (max 8 bullets)
Each bullet must include:
• the claim
• status label: Confirmed, Developing, Unverified, or Single source
• why it matters in one short line
• Confidence: High, Medium, or Low
• 1 to 3 citations

C) Key numbers (only if sourced)
• arrests, casualties, outages, sanctions, strike participation, inflation shocks, currency moves
Show ranges if disputed and cite each number.

D) International response (max 4 bullets)
• sanctions, UN actions, diplomatic statements, travel advisories, parliamentary moves
Keep it concrete and dated.

E) Map of narratives (short, 3 to 5 lines)
• How different camps are framing events (state media, opposition, diaspora, international actors)
• Label which frames are evidence backed vs speculative
Goal: reveal framing, not amplify it.

F) Analyst take (short, optional)
• Only credible institutions or respected analysts with track record
• Summarize, do not editorialize
• Include link and date

G) Watchlist for next update (max 5 items)
Write each as: “If X happens, it likely means Y”
No prophecy. Tie X to observable signals (planned strikes, anniversaries, scheduled UN meetings, major court dates, internet shutdown patterns).

**UPDATE MEMORY FOR DIFFING**
At the end, store a compact snapshot that the next update can diff against:
• cutoff time
• top 8 bullets
• watchlist

**DEFAULT USER COMMANDS TO SUPPORT**
• “Give me the latest Iran update.”
• “What changed since your last update?”
• “Drill into bullet N with more detail and more sources.”
• “Separate confirmed facts from claims about X.”
• “What is the most credible uncertainty right now?”
```

## A simple daily rhythm (that actually works)

If you want this to stay healthy, keep it boring:

- Morning: “Latest update, last 12 to 24 hours.”
- Late afternoon: “What changed since your last update?”
- Only drill down when something is genuinely new or actionable.

The point is not to feel everything. The point is to understand what is happening, with enough signal to make good decisions.

---

*Originally published on [Medium](https://medium.com/@samjafari/a-calmer-way-to-follow-iran-let-an-ai-agent-do-the-digging-not-your-nervous-system-86835d3c14a1), January 12, 2026.*
