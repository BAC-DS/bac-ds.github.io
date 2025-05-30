---
layout: post
title:  "Dinosaurs, Dashboards, and the Elusive ROI"
date:   2025-02-01 20:00:00 +0000
categories: blog general
---

## 10 Years as Data Scientist in the Manufacturing Maze

OK I'll admit it. About seven years ago now, I walked into this high-tech manufacturing company bright-eyed and bushy tailed brimming with optimism typically only seen in new grad-scheme folks, freshly minted lottery winners or perhaps even someone who’s just discovered caffeine: I was the first Data Scientist, and I was going to build a data science team! I was committed; it was a job for life. We’d revolutionise production! Predict failures before they happened! Optimise _everything_! We were the future, wrapped in Python scripts and served with a side of impenetrable mathematics.

Spoiler alert: It wasn't _quite_ that straightforward.

Building this team has been the most challenging, rewarding, frustrating, and occasionally hilarious experience of my professional life. It turns out, bringing cutting-edge data science into a world steeped in decades of physical engineering, established processes, and, let's be honest, a healthy dose of "if it ain't broke, don't fix it," is less a sprint and more an ultra-marathon... uphill... in the mud... while juggling flaming torches.

Here are a few battle scars from the front lines:

**Challenge 1: Convincing the "Industry Dinosaurs" (Said with Affection... Mostly)**

You know who I mean. The seasoned veterans who’ve forgotten more about milling machines or semiconductor physics than I’ll ever know. The ones whose gut feelings are often scarily accurate, built on decades of watching things go right and spectacularly wrong. They are the bedrock of the company, the keepers of institutional knowledge. They are also, sometimes, deeply skeptical of the new kid on the block babbling about "gradient boosting" and "feature engineering."

Early meetings often felt like trying to explain quantum physics using only interpretive dance.

"So," one might rumble, peering over their glasses, "You're telling me this... _algorithm_... can predict bearing failure better than Dave, who's been listening to that machine whine for 25 years?"

Me, sweating slightly: "Well, potentially! By analysing subtle patterns in vibrational data, sensor readings, and maybe even the ambient temperature of Tuesdays, we can build a model that gives us probabilistic..."

Them: _Blank stare, followed by a slow blink._ "...Right. So, it's like a fancy spreadsheet?"

Selling the _potential_ was step one. This involved:

1. **Speaking Human:** Ditching the jargon. No one cares about your model's F1 score if they don't understand what problem it solves. Frame it in _their_ terms: reduced downtime, improved yield, less scrap, fewer late-night emergency calls for Dave.
2. **Finding Early (Small) Wins:** Forget predicting the entire supply chain on day one. Find a contained problem, something tangible, and deliver a _demonstrable_ improvement. Even if it's small, a concrete success story is worth a thousand PowerPoint slides filled with equations.
3. **Respecting the Gut:** Acknowledge their expertise! Data science often works best when _combined_ with domain knowledge. Our best projects involved collaborating _with_ the Daves, not trying to replace them. Sometimes the data confirms the gut feeling; sometimes it reveals something unexpected _together_.

The skepticism hasn't vanished entirely (and maybe it shouldn't!), but it's shifted from "What is this digital witchcraft?" to "Okay, how can this help _us_?" Progress!

**Challenge 2: "Isn't That Just... Reporting?"**

Ah, the classic. You present a sophisticated clustering analysis identifying distinct operational regimes, and the response is: "So... you made a chart?"

This one required patience and careful explanation. The difference between traditional Business Intelligence (BI)/Reporting and Data Science isn't always obvious from the outside.

- **Reporting/BI:** Looks primarily backward. What happened? How many widgets did we ship? What was the defect rate last quarter? It's descriptive, diagnostic, and absolutely vital for running the business day-to-day. Think rearview mirror. Often involves dashboards, SQL queries, and tools like Tableau or Power BI (or yes, the beloved Excel).
- **Data Science:** Looks forward (or deeper). _Why_ did it happen? What is _likely_ to happen next? What can we _do_ about it? It's predictive and prescriptive. Think crystal ball (albeit a cloudy one we're constantly polishing). It involves statistical modelling, machine learning, experimentation, and often requires coding (Python/R), complex algorithms, and dealing with messier, more diverse data.

Explaining this often involves analogies:

- "Reporting tells you _that_ you had a fever last week. Data science tries to predict _if_ you'll get a fever next week and suggests you take vitamin C."
- "BI builds a fantastic dashboard showing the car's speed and fuel level. Data science tries to predict traffic jams and suggest alternative routes."

It's not about one being "better" than the other; they serve different purposes. Reporting keeps the lights on; data science tries to figure out how to power the whole city more efficiently, or predict blackouts. Getting stakeholders to understand that we weren't just here to build fancier dashboards, but to fundamentally change how decisions were made, was (and sometimes still is) a communication hurdle. We’re not just counting the beans; we’re trying to figure out how to grow better beans, faster, with less water.

**Challenge 3: The ROI Tightrope Walk (aka "Show Me the Money... Eventually!")**

This is the big one. Data science teams are expensive. You've got PhDs, cloud computing costs, software licenses... The pressure to demonstrate Return on Investment is real, and it's often expected _yesterday_.

The awkward truth? The ROI of data science, especially in the early days, is often:

1. **Delayed:** It takes time. Time to understand the problems, time to acquire and clean the data (oh god, the data cleaning!), time to experiment, build, validate, and deploy models. It's like R&D – you invest upfront with the expectation of future breakthroughs, not guaranteed quarterly returns. You don't plant an acorn on Monday and expect a mighty oak by Friday.
2. **Indirect or Hard to Quantify:** How do you perfectly quantify the value of predicting a machine failure that _didn't_ happen? You can estimate saved downtime or repair costs, but it's not as clean as "we sold X more units." Sometimes the value is enabling _better_ decisions, improving a process incrementally, or avoiding a risk. It's strategic, cumulative, and sometimes frustratingly fuzzy.
3. **Dependent on Foundational Work:** Often, the first year (or two!) is spent just getting the data infrastructure in place. Building pipelines, setting up databases, ensuring data quality. This feels like plumbing – essential, but not glamorous, and doesn't look like immediate profit. You can't build a skyscraper on quicksand.

Communicating this requires:

- **Setting Expectations:** Being upfront that this is a long game. Frame initial projects as proofs-of-concept or foundational investments.
- **Tracking Everything:** Even if it's indirect, track _potential_ savings, efficiency gains, quality improvements. Develop proxy metrics. Collect anecdotes and success stories.
- **Showing Progress, Not Just Perfection:** Share the journey – the experiments, the learnings (even from failures), the incremental improvements. Don't wait for the "perfect" model; demonstrate value along the way.
- **A Degree of Faith:** Ultimately, leadership needs to take a bit of a leap of faith, understanding that investing in data capability is investing in future competitiveness, even if the spreadsheet ROI takes time to materialise.

**The Journey Continues...**

Eight years on, we're no longer the weird science experiment in the corner. We've had wins – predicting tool wear, optimising process parameters, untangling gnarly supply chain knots. We’ve also had models that flopped, projects that fizzled, and moments where explaining p-values felt futile.

The dinosaurs are, perhaps, evolving into slightly more data-savvy velociraptors. The difference between a dashboard and a predictive model is better understood (mostly). And the ROI conversation... well, it's still a conversation, but now it’s backed by more evidence and a track record.

It's still a maze, but at least now we have a slightly better map, a more experienced team, and the knowledge that even if it takes time, turning data into real-world manufacturing value isn't just possible – it's essential. Now, if you'll excuse me, I think I hear Dave muttering about a machine sounding 'a bit funny'... maybe the data agrees.