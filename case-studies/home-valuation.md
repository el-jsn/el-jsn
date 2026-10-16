# Home valuation for Realtris

I'm developing a residential valuation system for Realtris, now integrated into its live home valuation experience. Users start with an address and confirm property information to request an automated estimate.

[Try the home valuation tool](https://realtris.ca/whats-my-home-worth)

## The problem

An automated estimate needs to account for both the property and the quality of the information available about it. Records can be incomplete or inconsistent, comparable sales may be limited, and some homes fall outside the situations a system can assess reliably.

My work focuses on producing a useful estimate while making those limitations visible.

## Working with imperfect property data

One challenge was handling conflicting records, ambiguous property matches, and missing information. The system needs to distinguish usable evidence from information that is outdated or does not describe a sale.

At a high level, property information is checked and normalized before it reaches the valuation workflow. The workflow can also handle properties without usable current listing information, with different treatment of the uncertainty involved.

## Evaluating what the system could have known

Historical evaluation creates another challenge: information available today may not have been available on the date being evaluated. Allowing later sale information into an earlier valuation would make the results look better than they really were.

The evaluation workflow separates earlier training data from a later historical period and checks when supporting information became available. It also excludes the property being valued from its own comparable-sale evidence.

Historical results still have limits. Performance measured at one stage of a transaction does not establish the same accuracy for a newly listed home or a property that is not on the market. I continue working on evaluation across different property situations.

## Knowing when to require review

The system returns an estimate with a value range and supporting context. It also checks for weak evidence, unusual properties, and other reasons an estimate may be unreliable.

Depending on the case, it can flag the result for review or refer the property for human assessment instead of returning an automated value. The range communicates uncertainty; it is not a guaranteed selling-price range or a formal appraisal.

## From valuation to a live product

The application connects property inputs, historical market evidence, a valuation service, and a public interface. Supporting workflows package releases and refresh stored estimates when relevant information changes.

The tool is live on Realtris. Development continues on evaluation, data quality, and the handling of less reliable cases.

[Try it for yourself](https://realtris.ca/whats-my-home-worth)

[Back to my profile](../README.md)
