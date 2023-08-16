# Adopt Using GitHub Pages to Host SDK Technical Documentation

## Problem

The keywords "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in RFC 2119.

For each of the SDKs, we are keeping technical documentation inside relevant README files. While this is great for keeping a single source of truth (updating developer.vonage.com has latency built-in), we often do not include function/class definitions to aid developers in using our SDKs.

## Duration

01 Apr 2023 - 27 Apr 2023

## Current State

Voting

## Proposers

Chuck Reeves

## Detail

As part of the documentation process, we have various code sample repositories which Bifrost will then include where appropriate. While we are fairly diligent in keeping the samples updated, we have some gaps with this process.

One such gap resides with the Node SDK. Version 3 was released in Q4 of 2022, leaving version 2 support status. Bifrost cannot represent samples from both V3 and V2 leaving those still required to use V2, in the dark. This leads to the code sample repositories will only represent the required parameters that need to be passed in order to function neglecting to demonstrate the full set of features.

Bifrost does not have means of showing details for the parameters. This means if we deprecate a parameter, the user will have no means of knowing how to update their code to support newer versions. 

## Solution

Adapting document generators and hosting them on GitHub pages will provide the details developers need in an automated way. A new GitHub action triggered to run when a PR merges into the main branch, will build the docs and publish. Each language has its own tool to build the docs, but only one action is needed to publish the documents to GitHub.

### Tools

* Javascript/Node/Typescript: JSDoc
* Ruby: Yard
* PHP: PHPDocumentor
* .NET: Sandcastle
* Python: pydoc
* Java: Javadoc
* Github Action

## Record of Votes

| Person             | Accept Proposal |
|--------------------|-----------------|
| Chuck Henry Reeves |                 |
| Chris Tankersley   | ✅              |
| Guillaume Faas     |                 |
| Jim K Seconde      |                 |
| Karl A Lingiah     |                 |
| Max Kahan          |                 |
| Sina Madani        | ✅              |
| Paul Ardeleanu     |                 |
	
