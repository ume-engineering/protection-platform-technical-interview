# protection-platform-technical-interview

## Overview
The Protection Platform gives Financial Advisors access to accurate and fully underwritten protection premiums from multiple providers in real time.

Obtaining protection products often involves disclosing sensitive medical details. The current process involves the advisor capturing these details over the phone. 

We wish to add a new feature that allows the advisor to share the insurance application with the end customer(s) in order to complete these questions. Once the necessary questions have been answered by the customer we obtain the relevant premiums and send them to the customer.

## Requirements
The product team have identified the following requirements:
* An Application can only be shared if:
    * it was created less than one month ago
    * Each Customer on the application must have at least one insurance product selected
    * Each Customer must have provided their email address.
    * On the day the policy starts all customers must not be over 80 years old.
* If the above critieria are satisified send an email to each customer inviting them to complete their questions.
* Each customer must provide their height, weight and occupation.
* Once the above questions have been captured obtain a decision and premium from the Underwriting Rules Engine.
* Send the 'Buy Now' email to the customer if a quote is available.
* If there are no quotes send the 'Unable to offer cover' email to the customer.

Assume the Underwriting Rules Engine is deployed as a microservice.

It accepts a `POST` request to `/quote` containing:
```json
{
    "height": 180,
    "weight": 80,
    "occupation": "Accountant"
}
```

if a quote is available it will respond with:
```json
{
    "decision": "QUOTE",
    "premium": 450.00
}
```
if no quote is available it will respond with:
```json
{
    "decision": "DECLINE"
}
```
⚠️⚠️ for this excercise you should not need a running instance of the Underwriting Rules Engine ⚠️⚠️

## Task
* Implement a simple application that meets the above requirements.

Note: This is primarily an excercise in domain modelling so you don't need to worry about:
* Writing a RESTful/web API or User interface
* Databases or persistence
* Authentication or Authorisation
* Infrastructure or deploying to the cloud
* Enhancing or extending the build process
* Knowledge of or bringing in additional frameworks or libraries
* Modifying/Updating/Extending the Underwriting Rules Engine microservice.

## What we're looking for:
* Clean code and a modular design with clear separation between the domain and technical concerns.
* An incremental approach.
* An automated test suite.

:information_source: There is no one correct solution to the problem. The goal is to get a sense of how you think, how you collaborate to deliver a solution that solves a specific customer need.


