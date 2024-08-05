# Vulnerability Management Operations Template

## Introduction

Purpose of vulnerability management. In this section, you’ll want to insert what values and company objectives you hope to achieve (even if it’s just, “patch and track so we can secure things for our customer bottom line”). 

## Scope

What’s the scope of your program? Is it only going to include System and Application dependencies at your company? Will it include bugs found from bug bounties or security code reviews? 

Other things to consider:

- Are there specific services or products that would be considered out of scope?
- Are there specific bugs or findings that would be out of scope?

## Operations

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
    - Do you have other things

### Reporting/Tracking

### Review and Action
