---
layout: post
title: "Starting an SRS with an LLM (Ahmedira Part 1)"
date: 2023-09-16 00:00:00 +4000
categories: Development
---

Time to create an issue tracker or Jira clone. It shall be called Ahmedira, and I will use Jira for my sprints until I have an MVP (the objective of the first sprint) that I can use for the rest of the application.

I will be implementing Auth0 for the log-ins and I'll also host it on Oracle Cloud - both a bit beyond the scope of a Minimum Viable Product. The database will be relational, though I am delaying a decision between MySQL and PostgreSQL. A bootstrap template will afford me my UI design for now.

With the rise of ChatGPT, I can supplement stackoverflow and documentation for the code proper - the alternative modules, the intricacies, etc. Thus, I am going to use Django as the basis for it as I have been using a lot of Python for small commercial and automation projects recently.

I will also be using and editing ChatGPT to guide me to get - if not from 0 to 1 - at least outside of 0. And after having a bare specification, my dread turned to excitement. I am currently using text with neovim, but eventually I'll make graphs and Figma designs.

An LLM isn't a replacement for a mentor, but it is what it is.

I prompted it for a limited SRS, and after a lot of editing, I received this.



```
**System Requirement Specification (SRS) for Issue Tracker System**

**1. Introduction**

The Issue Tracker System is designed to help users manage and track issues within a specific backlog. This document outlines the functional and non-functional requirements for the system.

**2. Scope**

The Issue Tracker System will allow users to manage issues within a single backlog with the following features:

**3. User Interface**

- Upon entering the site, the user will be presented with a webpage with the following elements:
  - A Title named "Ahmedira"
    - font		: Verdana 32-point 
    - alignment		: left-aligned
  - The background page
    - background color	: #f6f6f6
  - The backlog
    - background color	:	lighter than #f6f6f6
    - font-point	:	14pt
    - border		:	solid 2px black
    - has a shadow between it and the page
    - has
  - The backlog:: The add button
    - margin		: 2px (should look like a cannal separates them)
    - background color	:	lighter than #f6f6f6
  - The backlog:: The scroll
    - margin		: 2px (canal is a question to ask through experiments)
    - background color	:	lighter than #f6f6f6
  - A demi circle
	- takes up a sixth-ish of the SE quadrant
	- color		: tbd 
  
**4. Backlog**

- The backlog will have the following default values:
  - Name: "Pest"
  - Code: "PT"
- A scroll option will be provided if the number of issues in the backlog exceeds visual capacity.
- An "Add" button will allow users to add issues beyond the capacity.

**5. Issue Creation**

- Users can create issues within the backlog.
- An issue is a single line and displays text of 14 points
- When creating an issue, a pop-up-type screen will appear that asks for the following information:
  - Issue name		text		
  - category		select		limited to: Development-Bug-Documentation,
  - description		text area	
  - progress		select		limited to: do-doing-done, 
- When creating an issue, the following information will be generated:
  - (view only) Primary key	text		made according to $"{backlogName}-{increment}"
  - (view only) Created On	timestamp,
  - (view only) Last Edited	timestamp, and
  - (view only) Finished On	timestamp.
- Creating an issue should set the Created On timestamp.
- Editing an issue should update the Last Edited timestamp.
- Marking an issue as "done" should set the Finished On timestamp.

**6. Issue Detail Screen**

- Users can access a detailed view of an issue by clicking a button associated with that issue.
- It will be a darker off-white
- It will gray out the rest of the screen
- It will allow the user to view its user-focused values and allow edition of some

**7. Functional Requirements**

- The system should ensure that each issue in the backlog has a unique identifier.
- Users should be able to view all issues within the backlog.

**8. Non-functional Requirements**

- User-Friendly Interface: The user interface should look like an application of a bootstrap template
- Scalability: The system should assume 1 single user - for now

**9. Constraints and Assumptions**

- The system will be designed for web-based access.
- Compatibility with modern web browsers is assumed.
- The system will be developed using Python-Django.

**10. Revision History**

- Document Version: 1.0.0
- Date: 15 Sep 2023
- Author: ChatGPT
- Editor: Ehsan

```
