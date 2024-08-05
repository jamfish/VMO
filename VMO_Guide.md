# Vulnerability Management Operations Guide

## Author’s Notes:

Hey all, this guide is not only for use to know what questions to ask, but to also use as a structural template if you’re wanting to document your own Vulnerability Management Operations. If you have any questions, please free free to reach out at tech-at-jam-dot-fish, or open a issue. 

## Introduction

What’s the purpose and goal of your vulnerability management? You’ll want to insert what values and company objectives you hope to achieve (even if it’s just, “patch and track so we can secure things for our customer bottom line”). 

## Scope

What’s the scope of your program? Is it only going to include System and Application dependencies at your company? Will it include bugs found from bug bounties or security code reviews? 

Other things to consider:

- Are there specific services or products that would be considered out of scope?
- Are there specific bugs or findings that would be out of scope?

## Operations Overview

### Sourcing Vulnerabilities

Here you explain how vulnerabilities are currently sourced. 

**System Vulnerabilities** 

How do you source system vulnerabilities? Some common tooling:

1. Synk (for Containers) 
2. AWS Inspector
3. Rapid7 Insight VM 
4. Wiz 
5. Tenable Nessus

**Application Vulnerabilities** 

How do you source application vulnerabilities? Some common tooling:

1. Dependabot 
2. Snyk (for code scanning) 

**Things to consider when evaluating tools:**

1. What are the available ways to source that information in a programmatic way?
    - Does the source allow API calls/integrations?
    - Does it export in data formats that can be read programmatically?
        - Such as CSV
2. Does the toolset scan or evaluate:
    - The architecture of your infrastructure
    - The languages in your stack
    - Are the installation instructions easy to understand and accomplishable by your team.
    - Is the vendor that’s selling the solution able to provide support when things go wrong, or provide best practices?

### Reporting/Tracking

We need to figure out where to put the data we’re sourcing. NOTE: It doesn’t have to be complex from the start, we can spreadsheet first to develop a process. Eventually though, you will grow out of that and need to automate quickly. This is where the answers to sourcing questions are helpful. 

- You also have to think about how you’re ingesting the data
    - Does the ticketing or accounting system you’re looking at allow for certain classifiers and tags?
    - Can you attach reports that you get from your sources?
    - Is there a way for folks to not have to go into the system in order to send updates or change statuses?

### Review and Action

When thinking about Review in Action, it’s more than just the short term review then remediation/mitigation/acceptance action. We also have to think about the longterm of reviewing and taking action on our VMO practice regularly. 

- Short-Term
    - How are we reviewing vulnerabilities?
        - Is it Security, Engineering, or a combination of both?
    - How are we remediating vulnerabilities?
        - How are we prioritizing vulnerabilities
            - Most commonly we’d use a severity system (rating from Critical Risk Impact to Low Risk Impact), as that’s industry best practice. You can see examples of this here.
            - Who’s prioritizing the vulnerabilities?
        - Which teams are in charge of bug fixes.
    - What’s the timeline for fixing vulnerabilities
        - If we’re using severity, how are we documenting the timelines
            - Are these a best effort, or a hard line requirement?
    - What if we can’t fix it? How do we manage accepting that risk and/or mitigating the blast radius of the risk?
    - Also, what are some vulnerabilities we don’t care about/consistently low risk?
- Long-Term
    - What metrics are we using to guage the success of our program?
    - How often are we checking in with the company on the health of the program?
        - And how often are we reviewing the risk we’ve accepted.
    - How do we ensure any improvements we want to make are also tracked and completed?
