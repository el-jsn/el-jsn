# Inventory planning for Chick-fil-A North Barrie

I built a web application that used the location's sales data to estimate daily chicken pull quantities. It started with one kitchen planning problem and later expanded to produce and beverages.

![Weekly allocations dashboard showing chicken pull quantities by day](https://eljsn.vercel.app/project-inventory.png)

*The allocations dashboard turns daily pull estimates into quantities the kitchen team can use.*

## The problem

We used a printed sheet with fixed numbers to decide how much frozen chicken to pull each day. Demand changed from week to week, but updating the sheet regularly was difficult.

The timing made that decision harder. At our location, chicken took approximately 24 hours to thaw, and the planning window was roughly 96 hours from when it was pulled, not from when it finished thawing. We had to plan ahead without pulling more than we could use.

Too little meant risking a shortage before the next batch was ready. Too much meant a greater chance of waste. A fixed sheet could not adjust easily to those changing needs.

## What I built

I built an application that used sales data to estimate how much chicken to pull each day. Instead of relying on the same printed quantities every week, the team had preparation targets informed by the location's demand.

I developed the full-stack application using MongoDB, Express, React, and Node.js, and worked with the on-site team to refine it for daily use. The interface supported tablets and mobile devices so staff could use it at their workstations.

## Decisions that mattered

- **Plan ahead for thawing.** The tool had to support decisions made before the chicken was needed, rather than only show current demand.
- **Count from the pull time.** The thawing period was part of the overall planning window, not extra time added before it.
- **Give staff usable quantities.** The useful output was how much to pull or prepare for a station, rather than a sales figure on its own.
- **Start with one workflow.** I focused on chicken pulls first, then expanded the application once that workflow was working well.

## From chicken pulls to daily prep

We eventually expanded the application to planning for produce and beverages. It turned the same sales-based approach into preparation targets for more of the kitchen's daily work.

## Outcome

The chicken estimates worked well enough that we expanded the tool to other preparation tasks. That adoption is the clearest outcome I can describe here: a tool built for chicken pulls became useful across produce and beverage preparation.

[Back to my profile](../README.md)
