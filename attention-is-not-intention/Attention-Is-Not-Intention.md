# Attention Is Not Intention: The Algorithm's Portrait of Us

*Recommendation systems learned our impulses. Now we can tell them our intentions in plain language.*

By Sam Jafari

---

![A worn television remote resting on the arm of a grey sofa, a floor lamp on, and a television out of focus in the background showing a blurred wall of video thumbnails.](images/image-01.jpg)

*My television, most evenings. Most of what the feed knows about me, it learned from what I watched here.*

A few weeks ago I opened YouTube and realized my feed had turned to garbage.

This bothered me more than it should have, because YouTube is my television. I stopped using Facebook years ago, Instagram is off my phone, and I never picked up a TikTok habit. I pay for Premium because underneath the noise YouTube holds a lot of good material: science, engineering, psychology, business, long interviews, documentaries, and creators who can explain something hard without making it dull. Finding that material was getting harder every week.

The pattern was always the same. I would watch one video about an AI controversy and half my feed would become AI controversy. I would click a geopolitical story because something had actually happened, and YouTube would decide I wanted a week of political commentary. One interesting subject turned into twenty near-identical videos. One moment of curiosity turned into my new algorithmic identity. I pressed Not interested and removed channels. I searched deliberately for better material. The pattern kept coming back.

Then it clicked. YouTube had painted a detailed portrait of someone from what I clicked, what made me pause, and what I watched to the end. It had no idea why I did any of it, and without the why, what it held was a record of what had caught my eye.

## Attention is not intention

Everyone slows down to look at a crash on the freeway. Nobody wants a second crash. A system that learns from watch behavior alone cannot tell those two apart, because from where it sits they look identical.

Suppose I click a ridiculous political argument because I cannot believe somebody said something that stupid. The algorithm records: interested. Suppose I watch three videos about an aircraft accident because the first one made me curious about what failed. Strong interest in aviation disasters. Suppose I spend twenty minutes on some terrifying AI scenario. Likes AI risk. None of those conclusions describe what I want. I regret the twenty minutes on the political argument. I care about how aircraft are engineered, not about watching them come apart. I wanted to understand one AI risk properly, once, without turning my television into a permanent stream of dread.

![Three rows comparing what I did, what the feed concluded, and what I actually wanted: a political argument clicked in disbelief read as interest in political commentary; three aircraft-accident videos read as an interest in aviation disasters; twenty minutes on an AI scenario read as liking AI risk.](images/image-02.png)

*Three viewing patterns, three reasonable conclusions, three misses. The system sees what I watched. Unless it asks, the reason stays with me.*

To be fair to YouTube, its engineers have written about this. The system learns from clicks, watch time, likes, dislikes, shares and survey responses. It moved past raw watch time years ago because, as they put it, they "don't want viewers regretting the videos they spend time watching," and the surveys do ask why you rated a video the way you did. All of that is feedback about one video at a time, after the fact. What none of it captures is a statement about the feed as a whole: what I want my evenings to be made of, and what I do not want more of no matter how reliably it stops my thumb. The system still has to infer that from what I do, and what I do tilts toward whatever grabs.

There is evidence for that tilt, with the usual caveat that each study measures a different outcome in its own setting. Researchers who analyzed more than 370 million impressions of headline variants on Upworthy found that for an average-length headline, each additional negative word raised the click-through rate by about 2.3 percent. In a separate study of millions of Facebook and Twitter posts by news outlets and members of Congress, each additional reference to the political out-group was associated with about 67 percent higher odds of a share or retweet, and out-group language predicted sharing more strongly than ordinary negative or moral-emotional language did. Neither study looked at YouTube's recommender. The inference from them is mine: if negativity and conflict win the contest for attention, a system rewarded for attention will find them.

![Three numbers from two studies: 2.3 percent more click-through for each additional negative word in an Upworthy headline; 67 percent higher odds of a share associated with each additional reference to the political out-group in Facebook and Twitter posts; out-group language predicting sharing 4.8 times as strongly as negative emotional language.](images/image-03.png)

*Two studies, three platforms, two different outcomes. Headline clicks on Upworthy rose with each negative word, and sharing of Facebook and Twitter posts rose with references to the political out-group.*

Nobody at YouTube had to write "make people angry" into a spec. There is no button labeled activate the amygdala. When I built the vehicle data platform at Lucid, the lesson that kept repeating was that a model finds whatever the objective rewards, whether or not anyone meant it to. Fear, conflict, novelty and outrage keep winning the contest for attention, so a system trained on attention discovers them on its own. The objective does that by itself.

## The person Facebook thought I was

About eight years ago I found something inside Facebook that I have never forgotten. Facebook had built a profile of my interests, inferred from my behavior, to decide which ads to show me, and it had nothing to do with anything I had written about myself. It was buried deep enough that I had to watch a tutorial to find it, and I was not alone. A Pew survey published in early 2019 found that 74 percent of Facebook users did not know the list existed until the researchers pointed them to it, and Facebook itself acknowledged that year that its ad preference tools could still be "hard to understand and difficult to navigate."

When I finally reached the page, some of the categories made perfect sense. Some were surprising. A few were unsettling, and mostly accurate, which was the unsettling part: seeing them together made it obvious how much the platform had inferred from thousands of tiny interactions I had barely noticed myself. For the first time I was looking at Facebook's portrait of me, built to choose my ads. A feed is built on the same kind of inference, and I think every recommendation platform owes us that view of itself.

## The algorithmic mirror

Imagine opening YouTube and reading this:

> Based on your viewing over the last three months, we think you are highly interested in artificial intelligence, automotive technology, startups, health and science. Recently your viewing has shifted toward geopolitical conflict and AI-risk content, so those topics are getting more weight. You mostly watch long explanatory videos, though lately more commentary and reaction. Most of your technology viewing now comes from a small group of channels.

Then one question: is this what you want?

That is a different relationship with an algorithm. I might answer no, geopolitics matters when something important happens and I do not want daily political theater. I might say yes, I care about AI, but show me engineering, research, discovery and people building things, and cut the repetitive speculation. Or I might just say the feed has gone narrow, surprise me. I think of it as an algorithmic mirror. Before asking people what they want, show them what the system currently believes they want. I could not have described my ideal information diet from scratch. Shown the distorted version, I knew the corrections immediately, and I suspect that holds for most people.

![A mock-up of an algorithmic mirror: a card headed "Here is how we currently understand you" listing the inferred interests, the recent shift toward geopolitical and AI-risk content, the format and channel concentration, then the question "Is this what you want?" with three example answers and a box for your own words.](images/image-04.png)

*What the mirror could look like. The platform states what it has inferred, asks whether that is what you want, and takes the answer in plain language. A mock-up, not an existing feature.*

## Now I can talk back

The vocabulary we had for talking to a recommendation system was primitive. Like. Dislike. Subscribe. Not interested. Don't recommend this channel. Each one a single tiny training signal about one video, and every one of them a record of something I did rather than something I meant. Generative AI adds sentences. I can explain myself, and the system can act on the explanation.

YouTube has started here. In May 2026 it launched a custom feed, a chip beside the Home tab where you type what you want to watch and it builds a separate feed around that prompt. I do not want to give it too much credit yet. It is an experiment, US-only, one feed per account for most people, and it lives on phones and desktop. As far as I can find, nothing like it exists on the TV app, where YouTube's new Ask button lets you ask questions about the video you are watching but not shape the feed. Television is where I watch most of my YouTube, so the screen where I most need this control is the one screen without it. It also feels like a chip, a side feature, when it should be the central relationship between me and the system that picks my evening.

Still, it is a beginning, and a real one, because now I can tell the system something like this:

> Give me substantial but entertaining science, technology, psychology, health, AI, biology, space and business. Prefer people who researched, built or discovered something over people reacting to what somebody else said. Give me major geopolitical news when it matters and skip the daily theater. When an issue is contested, show me credible competing readings instead of reinforcing one. Avoid repetitive coverage, clickbait, manufactured outrage and fear-driven commentary. And now and then show me something excellent outside my interests so my world gets wider, not narrower.

Look at what that paragraph carries. Topics, yes, but also what I consider quality, how much novelty I want, how I want disagreement handled, where I want the line between information and entertainment, and which emotional tone I do not want running my living room. Most of all it carries the one signal clicks can never produce: I do not automatically want more of whatever grabbed me yesterday.

There is a catch, and it is the important part. A statement like that is worth nothing if it goes into the same pile as the clicks, as one more weak signal for an objective that still rewards attention. The crash on the freeway would win every time. It has to bind. The feed gets built around the statement, the way the custom feed already builds itself around a prompt, and the clicks adjust inside that frame instead of overriding it.

## Make it the default

A control buried in settings changes very little, because most people never find it. The Pew number shows the awareness problem: three in four did not know the list existed. So the mirror cannot be a chip that power users discover. After a platform has watched enough of me to form a model, it should say so, by default: here is how we currently understand you. Which subjects dominate the feed. Which interests are growing and which are fading. How concentrated the sources have become. Whether most of the political material is arriving from one direction. Whether the feed has drifted toward shorter, more reactive clips. Whether the same themes keep repeating. Then the question again: is this what you want?

Some pressure is arriving from outside. Article 27 of Europe's Digital Services Act already requires platforms with recommender systems to set out, in plain language, the main parameters behind recommendations and the controls on offer, and to put the switch where the feed is when more than one ranking option exists. In March 2026 a Los Angeles jury found Meta and YouTube negligent in the first of the social media addiction cases to reach a jury, and both companies said they would appeal. In August Meta agreed to pay up to 18 billion dollars to settle claims from state attorneys general that Facebook and Instagram were designed to encourage compulsive use in children, without admitting liability and pending court approval. Those cases are about kids, and I will not stretch them to every adult with a phone. But they land on the same layer as everything above: the recommendation system underneath the content debates, which decides what gets amplified, what keeps returning, what disappears, and what starts to feel important because you keep seeing it. Regulation asks for the parameters. What I want is the inference: how the system currently sees me, and a way to correct it in my own words.

## Working for us

I do not think recommendation algorithms are evil. There is more good science, music, journalism and teaching available today than any person could get through in a lifetime, and we need filters. The machine has become expert at what works on us, and we have stayed primitive at telling it what should work for us. Language can fix that part. Let the algorithm watch what I do; that signal is useful. Then show me what it concluded, let me argue with it, let me separate curiosity from preference, and let me say the disaster I watched last night mattered but I do not need twenty people yelling about it tomorrow. Then show me the mirror again in a few months, because people drift, and a passing curiosity should not quietly become a permanent identity.

We spend a lot of words on AI alignment, on making powerful systems understand and follow human intentions. The recommendation feed is the version of that problem most people actually live with. My feed knows my impulses better than I do. It has never had a sentence from me about what I want it to be, and there is still nowhere on my television to type one.

---

## Sources

1. **Robertson et al., Nature Human Behaviour, 2023.** "Negativity drives online news consumption." Roughly 105,000 headline variants tested on Upworthy, more than 370 million impressions; for an average-length headline, each additional negative word raised click-through by about 2.3 percent.
2. **Rathje, Van Bavel and van der Linden, Proceedings of the National Academy of Sciences, 2021.** "Out-group animosity drives engagement on social media." About 2.7 million Facebook and Twitter posts from news outlets and members of Congress; each additional out-group term was associated with about 67 percent higher odds of a share or retweet, and out-group language was a stronger predictor of sharing than negative or moral-emotional language.
3. **Pew Research Center, January 2019.** "Facebook Algorithms and Personal Data." Survey of 963 US adult Facebook users, fall 2018; 74 percent did not know the platform kept a list of their interests and traits until shown it.
4. **Meta Newsroom, July 2019.** "Understand Why You're Seeing Certain Ads and How You Can Adjust Your Ad Experience." Source of the "hard to understand and difficult to navigate" line.
5. **YouTube Official Blog, September 2021.** Cristos Goodrow, "On YouTube's recommendation system." The signals the system uses, the satisfaction surveys, and the move from raw watch time.
6. **YouTube Help, May and August 2026.** TeamYouTube announcements on the custom feed experiment, with coverage in Android Police and Thurrott. Eligibility, the one-feed limit, the 30-day expiry, availability on phones and desktop.
7. **YouTube Official Blog, March 2026.** "YouTube's conversational AI tool is now available on TVs."
8. **Regulation (EU) 2022/2065, the Digital Services Act.** Article 27, recommender system transparency: main parameters in plain and intelligible language, the options offered to users, and direct access to the selector where several options exist.
9. **Los Angeles County Superior Court, Judge Carolyn B. Kuhl, March 25, 2026.** Jury verdict in the first bellwether of the coordinated California social media addiction cases, finding Meta and YouTube negligent; both companies stated they would appeal. As reported by NPR, CNBC and NBC Los Angeles.
10. **Meta multistate settlement, announced August 26, 2026.** Up to 18 billion dollars with a coalition of state attorneys general, pending court approval; reported terms include default daily time limits and a chronological feed option for users under 18. As reported by CNN, The Washington Post and Poynter.
