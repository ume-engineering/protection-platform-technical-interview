# protection-platform-technical-interview

## Overview
The Protection Platform gives Financial Advisors access to accurate and fully underwritten protection premiums from multiple providers in real time.

Obtaining protection products often involves disclosing sensitive medical details. The current process involves the advisor capturing these details over the phone. 

We wish to add a new feature to allow the end customer(s) to complete these questions. Once the necessary questions have been answered the customer we obtain the relevant premiums and send them to the customer.

## Requirements
The product team have identified the following requirements:
* An Application can only be shared if:
    * it was created less than one month ago
    * Each Customer on the application must have at least one product selected
    * Each Customer must have provided their email address.
    * On the day the policy starts all customers must not be over 80 years old.
* If the above critieria are satisified send an email to each customer inviting them to complete their questions.
* Each customer must provide their height, weight and occupation.
* Once the above questions have been captured obtain a decision and premium from the Underwriting Rules Engine.
* Send the 'Buy Now' email to the customer if a quote is available.
* If there are no quotes send the 'Unable to offer cover' email to the customer.

## Task
* Using Test Driven Devleopment (TDD) implement a simple application that meets the above requirements.

Note: This is primarily an excercise in domain modelling so you don't need to worry about:
* Writing a RESTful/web API or User interface
* Databases or persistence
* Authentication or Authorisation
* Infrastructure or deploying to the cloud
* Enhancing or extending the build process
* Bringing in additional frameworks or libraries

## What we're looking for
* Clean code.
* An incremental approach.
* A useful, fast set of unit tests that are resistant to refactoring of the internal implementation.
* A modular design with clear separation between the domain and technical concerns.
