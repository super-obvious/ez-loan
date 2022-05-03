# EZ Loan

## Introduction

EZ Loan is a fictional company providing home loans to individuals through their easy to use web application.

Take some time to read through this document and prepare if possible for a 1 hour session with the team at Super Obvious discussing this scenario and how you would best approach building the required services.

## Instructions

* Read the product brief below.
* Prepare if possible for a follow up casual chat with the team at Super Obvious discussing how you would approach building the application.
* We've kept this scenario open-ended by design, but some hints on what topics you could bring to the discussion include (but not limited to):
  * Infrastructure & architecture of the backend solution.
  * Tech stack choices & reasoning.
  * Data modeling to fulfil any business requirements.
* We're looking for high level solutions and concerns, rather than implementation of the specifics!

## Product Brief

EZ Loan is starting the development phase of their initial app offering: An onboarding and dashboard experience for users to sign up and apply for a home loan.

The product team has provided the engineering team with some wireframes of the application to be built:

![flows](./flows.png)

The core features of the application should resolve the following user stories:

* As a User, I can sign up
* As a User, I can fill out my personal details, which are:
  * Full Name
  * Phone Number
  * Address
* As a User, I can apply for a loan, which requires:
  * An amount of money requested for loan
  * An uploaded document of my most recent bank statement
* As a User, I can view my personal details and loan application progress in a dashboard.
* As a User, I can login and be redirected to my dashboard.

A/B testing is a core focus for EZ Loan, and for the initial application two flows are required to be built:

### Flow A:

A User:
1. Signs up with a Sign Up form.
2. Enters personal details into a form.
3. Is presented with their dashboard, with a prompt to apply for a loan.
4. Upon clicking the prompt, enters information into a Loan Application form.
5. Is presented with a success page, and a prompt to return to the dashboard.

### Flow B:

A User:
1. Signs up with a Sign Up form.
2. Enters personal details into a form.
3. Enters information into a Loan Application form.
4. Is presented with a success page, and a prompt to continue to the dashboard.
5. Is presented with their dashboard.

The flow a user is entered in to is decided at random and is specific per user. In the future, new flows may be introduced and tested for conversion metrics.

## The Chat

We'll either bring you in or zoom for a chat with the team at Super Obvious about the above scenario. In the chat, you can expect us to ask questions about your approach to the scenario, a high-level walkthrough of a solution, as well as any concerns you may raise as an engineer. We're leaving this open ended by design, be creative!

