# The Phases of SDLC

## Table of Contents

* [Introduction](#introduction)
* [The seven phases of SDLC](#the-seven-phases-of-sdlc)
  * [1. Feasibility study](#1-feasibility-study)
  * [2.Requirement analysis](#2-requirement-analysis)
  * [3. Design](#3-design)
  * [4. Development](#4-development)
  * [5. Testing](#5-testing)
  * [6. Implementation](#6-implementation)
  * [7. Maintenance](#7-maintenance)
* [Resources](#resources)

## Introduction

This chapter lists the seven phases of SDLC, as identified by the [BCS](http://www.bcs.org/) (The UK Chartered Institute for IT), and explains the key aspects of each phase.

## The seven phases of SDLC

### 1. Feasibility study

This first phase is intended ensure it is a good idea to proceed with a project, before too much work is done. It should answer questions like:

* Is the project practical?
* Is the project technically possible?
* Can it be done within a certain timeframe?
* What is the budget? Is it affordable?
* Will there be demand for the product? How much revenue will it generate?
* Is it legal? Will the product break any laws (e.g. privacy / data protection)?

This phase is all about making prediction, which is a risky business. Therefore, answers to these questions will often come with assumptions and caveats (e.g. "We assume we can build this with X staff members, so it will cost £Y. If we need to hire 20% more staff it will cost £Z").

### 2. Requirement analysis

This phase should provide a detailed understanding of what is needed to make the project a success. It involves 3 steps: gathering, analysing and recording requirements.

This phase should create a set of specifications by which the final product can be measured.

***Gathering* requirements:**
* Reviewing previous projects
* Looking at existing documentation
* Interview stakeholders (colleagues, clients, users, etc...)

***Analysing* requirements:**
* Create clear, complete, and consistent requirements
* Resolve conflict between requirements (e.g. the client wants the product in 3 months, but the team wants 6 months to build it)

***Record* requirements:**
* Create a single summary or list of requirements
* Write user cases
* Write user stories
* Create a process specification
* Build prototypes of possible solutions

### 3. Design

The design phases is not just about how the product will look (UI, branding, etc...). It is more designing/ structuring the code.

It involves designing:
* System architecture - what is the Object Oriented / class structure of the system?
* System logic - what algorithms / data structures will be used?
  * Abstract representation of data flows
  * Abstract model of the system
  * Includes entity relationship diagrams
* Physical aspects:
  * What are the inputs and outputs of the system
  * UI
  * Data design (maybe database structure)
  * Process design (how will the team work)


### 4. Development

The actual programming bit.

This involves implementing design documentation by writing code.

### 5. Testing

This phase should provide a degree of confidence in the system. It ensures the system:

* Matches requirements
* Responds correctly to all agreed inputs
* Works within time constraints
* Is sufficiently usable.
* Runs in intended environments
* Satisfies stakeholders

### 6. Implementation

The implementation phase includes launching the product for public use. This involves deploying code to the production environment / servers. This is work is often carried out with/ by [DevOps](https://en.wikipedia.org/wiki/DevOps) specialists.

A final public launch is often precursed by [alpha and beta releases](https://en.wikipedia.org/wiki/Software_release_life_cycle).

### 7. Maintenance

There 3 main types of maintenance:
1. Keeping the system running
   * Creating backups
   * Handling demand/ traffic spikes
   * etc...
2. Fixing bugs:
   * Analysing crash reports
   * Fixing errors
3. Making enhancement:
   * Improving existing functionality
   * Adding new features

Almost all systems will require all of these types of maintenance.

## Resources:

* [SDLC: Seven Phases of the System Development Life Cycle](https://www.innovativearchitects.com/KnowledgeCenter/basic-IT-systems/system-development-life-cycle.aspx)
