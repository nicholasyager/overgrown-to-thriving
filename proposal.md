---
theme: gaia
backgroundColor: #fff
marp: true
---

<!--
This video should be 2-5 minutes long. Your pitch does not need to be refined! Tell us the main idea behind your session, key topics that you plan to cover, and what audience members will learn. Feel free to share your screen if you want to use a doc or slides to run through your session at a high level. We recommend using Loom
--->

<!-- _class: lead -->

# From Overgrown to **Thriving**

Scaling Your dbt Project Like a Gardener

---

<!-- footer: 'Coalesce 2023 Pitch'  -->

# Draw a comparison between a complex dbt project and a garden

---

# <!--fit--> dbt deployments can be tricky to scale

1. Large organizations tend toward decentralization

<!-- Suppose you're in an organization of ~ 4,000 employees. Based on dbt Lab's reporting that organizations tend to resource their data teams with 1-2% of headcount, we should expect there to be ~40 - 80 people in the data organization. If we're conservative and estimate that maybe a quarter of those people work within the organization's dbt project, we're looking at 10 - 20 full time dbt contributors. Following the two-pizza rule of team sizes, it would be reasonable to expect there to be 2 to 4 distinct operating teams working within the project. -->

---

# <!--fit--> dbt deployments can be tricky to scale

1. Large organizations tend toward decentralization
2. Decentralization can lead to inconsistent standards and design principles

<!--
Once you're in territory where there are multiple distinct teams forming, storming, norming, and performing, it's common for there to be drift in how the teams operate. This can be something as trivial as leading commas vs trailing commas. It can also, however, become something as important as the definition of a Customer. Perhaps GTM analytics defines a customer as a CRM account with subscription, whereas a finance analytics team may define a customer as a corporate entity. This definition mismatch means that these two analytics teams now have entirely incompatible customer reporting.
-->

---

# <!--fit--> dbt deployments can be tricky to scale

1. Large organizations tend toward decentralization
2. Decentralization can lead to inconsistent standards and design principles
3. It's so easy to add "just one more" model

<!-- And now we're in the endgame of how to resolve our differences. Do we put in the effort to have GTM align with Finance or vis versa, or do we make just a few more models that shim together bits of both to workaround the reporting difference? dbt makes it delightfully easy to reference existing models and start pulling in data from somewhere else in the project. -->

---

<!-- _class: lead -->

# This leads to **sprawl**

---

# We start our journey

---

# Survey your garden

1. What are your core entities?
2. What are your exposures?
3. Are there any obvious architectural issues?

---

# Clear out the weeds and trash

1. Remove deprecated or otherwise unused models
2. Consolidate duplicate models

![bg right 80%](https://hips.hearstapps.com/hmg-prod/images/hankscorpioflamethrower-1528493255.gif)

---

# Renewal pruning

<!--
Gradual removal of unproductive branches to allow a plant to spend its resources growing healthy branches.
-->

---

# Divide the perennials

<!--
Dividing the perennials is the notion that we ought to separate your most industrious plants to prevent overcrowding and to allow for specialized treatment of plants in the garden.

Just like a garden needs to be divided into separate areas for different plants, your dbt project can be modularized into smaller sections. You'll discuss how to identify which models should be grouped together, how to consolidate similar models, and how to leverage groups and access controls to manage dependencies between sections.
-->

---

# Keep the weeds under control

<!--
Now that we've gotten our garden into a more maintainable state state, it's
vital that we prevent weeds and other unwanted plants from taking root. In a garden
this can take a great deal of time and effort. Thankfully, this is where our
metaphor breaks down in our favor. Instead of manual effort, we can use fantastic
tools to keep our garden productive. For a while, we've had tools like pre-commit
and sqlfmt to keep our queries readable and maintainable. As of last year, we've
also had developments in architectural monitoring tools like dbt-project-evaluator and Whetstone to monitor and report on _what_ we've built as well.
-->

---

# <!-- fit --> Take a short break, and grow a bright future

<!--
We've come a long way! Our project now has fewer unused models, a more efficient
structure, clearly-delineated responsibilities, and automated guardrails to keep
new growth in check. We can now take a small break and enjoy our handy work.

When we're ready, we can start to
--->

---

<!-- _class: lead -->

Nicholas A. Yager
yager@nicholasyager.com
