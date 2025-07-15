---
layout: post
title:  "Maximising the Efficacy of Your Data Team: Pt 1"
date:   2025-06-27 13:00:15 +0100
categories: blog general
---

# Defining a Data Team

I've asked these questions and seen them asked on Reddit numerous times.

At networking events, or when I've worked with contacts across dozens of companies, I've probed a bit and dug around to try to understand how it's handled there.

Moreover, I'm centrally involved in navigating this within my current company, as we grow and expand and the company and its data requirements evolve.

__What roles make up your data team?__

__What is the optimal structure of your data team?__

__Where do your data/data science team(s) sit within your company?__


We live in a time when using data to drive decision-making is critical, and not maximising its impact is basically leaving money on the table. As such, how you structure and position your data capability can make a significant difference!

Over the next couple of posts I'll outline what I've learned from reading around and talking with connections; but - as you will probably already know - there is no single answer that will definitively work. Multiple factors come into play, from type of business, stage of business growth, size of business, and maybe a couple more.

I share my thoughts below, by first addressing a core question ...

# What does a data team do?

The number of potential answers here scales approximately as:

<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

$$ \text{N}_{ops} \propto \sum_{i=1}^{n} \text{Businesses}_i \times \sum_{i=1}^{n} \text{CXOs}_i $$

Where:
- _Businesses_ is the number of distinct businesses, business units, departments, or initiatives.
- _CXOs_ is the number of people in leadership or SLT roles in each unit.
- And "N" is a chaotic, ever-growing scalar quantity.

#### In English? Pretty much everyone is going to have an opinion; if they overlap, you're golden

<figure style="max-width: 100%; margin: 20 auto;">
  <img src="/assets/images/posts/CXO_meet_re_Data.png" alt="Image of the CXO" style="width: 100%; height: auto; display: block;"/>
  <figcaption style="font-size: 0.9em; text-align: center; color: #666;">The CXO all agreeing on where the data team sits /s</figcaption>
</figure>

For me, a data team exists to structure, organise, manage and use the data collected by a company, to derive insights, enable, and provide value to the business.

This helps us understand some key roles that could constitute a data team...

__Storing and structuring data__ requires some _data_ and _database engineers_, and managing, controlling & monitoring these systems could involve a dedicated _database administrator_ .

__Ensuring security and compliance__ are key requirements for businesses - especially in the UK/Europe with the GDPR regulations. _Database_ and _system administrators_, working with IT and legal teams, should be well versed in how to optimise their data infrastructure and documentation to enforce role-based data access and permissions, myriad process controls that allow conformation with various standards e.g. ISO27001; transparency and auditability is often a neccesity for certain potential customers, so the data team can provide huge value here.

__Capturing data__ will likely be done by software; either be off-the-shelf or perhaps something developed internally; a bespoke solution. This could be a simple script which parses automatically generated files, or a full blow web app which interfaces with other systems This would involve some capacity of _software developers_, but also _data engineers_.

__Enabling Access, including via Self-Service Analytics__ is more and more a key objective of the data team, allowing wider teams to interrogate and analyse the data in a safe and simple environment. This capability, developed by _data analysts_ and _data engineers_ working together perhaps with _business analysts_ unburdens the data team from the day-to-day, tactical requirements, allowing _data analysts and data scientists_ to focus on the strategic projects, with greater value-add.

__Driving Insight and supporting decisions__ are a core function for _data analysts_, addressing issues and questions from product and finance teams, as well as working with domain experts to support technical teams. Outputs from these tasks can often inspire development of data products.

__Building and deployment of Data Products__ such as forecasting models, classifier systems, recommendation engines etc etc., will be one of the more visibile and headline-making outputs of a well-established data team, primarily owned and developed by _data scientists_ and _ML engineers_.

__Strategic roadmapping__ to understand how 'data' will be best leveraged to support and enable the wider business requirements and strategy. For this to be successful, and allow the company to extract the most value from its data, data team leaders (Directors, Snr Managers, VPs - whatever) need to be integrated with the SLT and CXO. Data literacy where key decisions are made and strategies signed-off is crucial.


In my next post I'll discuss the possible structures and positions for a data team. Thanks for reading 👍