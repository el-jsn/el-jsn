# Realtris AI: conversational property search

I designed and built Realtris AI end to end, from the chat interface and backend workflows to the listing-data integration. It helps users search Ontario properties, refine their requirements, explore listing details, and request follow-up from the real estate team.

[Try Realtris AI](https://realtris.ca/ai)

https://github.com/user-attachments/assets/f9a45f45-5495-4fda-9b36-23be649de664

A short excerpt from the Realtris AI product demo.

## The problem

A property search rarely ends with the first set of results. Someone might change their budget, narrow the location, or ask about a home they saw earlier. I needed the assistant to carry that context through the conversation while working with detailed listing information.

## Keeping a search coherent

Losing context across follow-up questions was one of the main challenges. A new request needed to build on the user's existing search without treating every message as a fresh start.

The amount of listing data mattered too. Passing too much information into the conversation could crowd out earlier requirements; passing too little left the assistant without enough detail to answer useful questions. I worked on how search context and listing information were carried forward so the assistant had relevant information available for the next turn.

## Defining the assistant's boundaries

I also built checks to help the assistant recognize questions it should decline, including attempts to extract private implementation details. The challenge was distinguishing those requests from ordinary questions about properties or how to use the product.

## Improving database performance

The assistant relies on database lookups to find properties and retrieve listing details. Working with production data, I removed unused indexes, added indexes better suited to the queries, and improved the queries themselves.

Most queries had been taking more than 500 ms. After this work, most ran in under 100 ms. These timings describe database queries, rather than the assistant's complete response time.

## How it fits together

At a high level, the application connects a conversational interface, backend workflows, and a listing database. A request is interpreted in the context of the conversation, relevant property information is retrieved, and the results are presented through answers and interactive listing cards.

Users can refine searches, explore individual properties, find similar listings, review sold comparables, and use monthly-cost calculators. They can also submit a contact or showing request to the team; a request does not confirm an appointment.

## In use

Realtris AI has been live for several months. I built the complete application and continue improving it based on how it behaves in use.

[Try it for yourself](https://realtris.ca/ai)

[Back to my profile](../README.md)
