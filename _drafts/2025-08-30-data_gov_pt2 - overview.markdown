---
layout: post
title:  "Data Governance Pt2: Why you should care about Data Governance"
date:   2025-08-26 07:00:00 +0100
categories: blog general
---

In my [last post](https://bac-ds.github.io/blog/general/2025/07/26/data_gov_pt1.html) I gave a tongue-in-cheek story about two (VERY fictional!) semiconductor manufacturing companies, exhibiting very different approaches towards and appetites for data governance, culminating in, well.... quite different results when auditors came knocking.

Frankly, passing an audit is barely even a side-benefit (admittedly it might be the ROI your SLT/CXOs are interested in!) but the day-to-day wins of a well executed and maintained data infrastructure, with ownership, documentation, versioning, quality, visibility provide extensive value for pretty much every facet of the business.

### Purpose of a Data Governance Strategy

Basically, the whole point is to build a system, or set of policies/frameworks/tools/widgets/*insert your internal corporate vernacular here*, that ensures data across the organisation is

- accurate
- secure
- accessible 
- used responsibly

#### 'If this was solved tomorrow, what would it look like?'

Let's do it this way - read the below and see if it sounds like some sort of utopia because, and I don't say this lightly, getting DG right will make __pretty much everything__ easier - for example:

<figure style="float: right; max-width: 40%; margin: 20 auto;">
  <img src="/assets/images/posts/No_DG_CXO.png" alt="Cartoon for poor vs good data governance" style="width: 100%; height: auto; display: block;"/>
  <figcaption style="font-size: 0.9em; text-align: center; color: #666;">Time for a bit of a rethink, and some data governance</figcaption>
</figure>

- knowing what data exists and who to ask about it
- secure access to that data
- analysis of data
- having confidence in the data and derived metrics
- visibility and clarity around metrics and KPIs
- understanding the reporting of metrics and KPIs

Which will all enable:
- appropriate and a considered democratisation of data
- tracking, visibility and optimisation of utilisation and performance of equipment
- tracability, testing and monitoring of products or parts
- generation, visibility, and - __ultimately__ - control of costings
- ability to make decisions on hiring, production, alterations, optimisation of systems... based on data
- you can finally call your company **data-driven**

But be aware - for any business, in any industry, at any scale, __data governance takes effort__. 
It's like exercise and getting in-shape and _staying healthy_ -- it's a way of life. 
Data governance isn't a data product that some day will just 'exist'.

So let's take a look at the key pillars of DG, and start to understand what they mean, and how to implement.

### **Key Pillars of a Data Governance Strategy**

#### Data Governance Committee

Who doesn't like a steering committee eh? What better way to make sure progress grinds to a halt 🛑 than to get a commitee put into place. Who hasn't got a couple of hours a week to waste in meetings? 🕣 🕐

__BUT...__

_This is going to matter. Data governance is a long-term project, and needs to be built to be robust, scalable, and coordinated_.

So actually, __YES - a steering committee__ (or other form of council) is not only a good shout, but actually necessary. A cross-functional team that oversees strategy, defines structure & policies, enforces compliance, resolves disputes... Yes.

Sorry (not at all sorry).

Additionally, they will be integral to the assigning and developing of the next pillars...

#### Data Policies & Frameworks, Privacy & Security

It might sound like a bunch of bureaucracy and red-tape-esque nonsense, but it really is crucial. Sometime soon three (ha! try 33) people are going to have the same question about some data, or will share the wrong thing, or want access to something they don't need or shouldn't be able to, or will fall foul of some legislation, or will flag an issue ... and on and on and ariston.

So, a key output that the DG Steering committee needs to yield is a set of policies and governing frameworks, to ensure that all of that "steering" is effectively logged, communicated and thus can be understood and acted upon.

It needs to cover:

- Ensuring compliance with regulations (GDPR, HIPAA, etc.)

- Defining rules for data classification, access control, encryption, and audit logging.

- Development of enterprise-wide policies (e.g. naming conventions, data retention).

- Defining of escalation paths when data issues arise.

__And a little more detail as to what that actually looks like...__

#### Data Management

From a __quality__ aspect, there need to be standards defined for what *makes data “good”* (e.g. accuracy, completeness, timeliness). This needs to be documented and applied across all systems for consistency, and could also include routines for profiling, validation, cleansing, and monitoring, so as much as possible is automatic, or at least second-nature.

Similarly, to allow for avoidance of duplication or ambiguity, __master and reference control__ needs to be considered, so that there are consistent definitions for core entities (e.g. customers, products).

Establishing a _data catalogue or glossary_ will help users understand the __Metadata__, or at least know where to look for definitions, lineage, usage, owners... . This will build on these quality and reference control pieces discussed just above, and can also help communicate and store information pertaining to the __lifecycle__ of the data (retention period, freshness, archival info).

__And who can support and actually drive this data management?...__

#### Data Ownership & Stewardship

Any of this sound familiar?

> "Hey who knows what this KPI means? Is it needed? How's it even derived?"

> "Why are all these negatives in here? This sensor literally CAN'T report a negative."

> "Yeah let me give you the connection string - password is just c0mp4ny_db_p4$$w0rd -- whatever you do don't alter anything..!"

A proper DG implementation would outline data owners and stewards immediately, and once in place, they would either quickly answer any of the questions above, or - more likely - mitigate them ever being asked.

A __data owner__ is accountable for the data, in the same way a landlord is accountable for their property; they decide what happens to it, approve changes, state who can access it... but they don't perform the maintenance or gardening or anything. Their chief concern is if and how the data is serving the business.

The __data steward__ is like the caretaker for the above landlord's property; they make sure it's clean, safe, running smoothly. Their main concern is whether the data is accurate and understandable.

This should be part of their job description; possibly you'll have seen items in job posts "XYZ will be responsible for the in-house downtime KPIs and reporting"... Which is fair - somebody has to own it.

__They can be supported with...__

#### Tools & Technology

Various software platforms exist to help with the above concerns, such as DataEdo, DataHub, dbt, Informatica... but not having the right tool shouldn't stop you from starting out. 

It can be done, initially, with Sharepoint, Excel, or some other ease-of-access tools (although it really needs to be moved to a fit-for-purpose platform ASAP!!!) - so long as the mindset is correct, and the team is determined.

And once these systems are being populated and deployed, and become part of the ecosystem, you can start looking at...

#### Measurement and Continuous Improvement

You can't improve what you can't measure, and no system is perfect; so by that logic your data governance _can_ be improved, if you:

- Define some metrics (e.g. % of critical data sets with stewards assigned, quality scores)
- Review and refine the strategy.


## Final Thoughts


In the final season of the West Wing, CJ Cregg is offered a few billion dollars to go and fix Africa. Hollis (the billionaire philanthropist) doesn't know how to spend it. CJ comments that it's highways and roads that are the issue; not sexy at all - but so many AIDS projects don't get off the ground because the medicine and resources can't get where it's needed.

Infrastructure is the issue.

Data Governance is kind of like this. It's not sexy like ML models that promise to optimise sales using customer segmentation, or some beautiful dashboard with high resolution interactive drill-downs, update to the minute. It's not about LLMs offering to answer all customer-facing questions, being fed from some RAG-interface which has ingested every internal document.

None of that can be done without strong under-pinning data infrastructure, and data governance to guide it.