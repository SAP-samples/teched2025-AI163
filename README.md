# AI163 -  Get hands-on to extend Joule and build AI agents 

## Description

This exercise shows how to build a simple custom Joule Agent in Joule Studio that uses multiple Joule Skills along with Document Grounding via AI Core to manage  shipments in the SAP Business Networks Global Track and Trace (GTT) system. The agent can create shipments, get delayed shipment details and even tracking details of existing shipment. It uses Document Grounding to read a shipment rate card document and determine the most economically viable shipment carrier based on their rates, source location and destination location while creating a shipment.

## Overview

### Busiess problem and persona   

Before diving into the use case, let's take a moment to get acquainted with our business user. It's really important to understand the business user as thoroughly as possible before building your custom Joule Agent.

Meet George, a Logistics Coordinator at a global manufacturing company.

Every day, George is responsible for creating, tracking, and managing shipments across multiple transportation partners using SAP Business Networks Global Track and Trace — or GTT for short.
His job is to ensure that every delivery — from raw materials to finished goods — reaches the customer on time and in full. 

#### Persona — Logistics Coordinator
<img width="747" height="432" alt="image" src="https://github.com/user-attachments/assets/d955078e-3896-4a28-b504-6a330525b36e" />

#### Pain Points — Logistics Coordinator
<img width="741" height="468" alt="image" src="https://github.com/user-attachments/assets/edaf66c0-fcd0-4b49-aac9-143a6e96e8a4" />

### You will buid a goal-driven Joule Agent in Joule Studio that: 

- Understands a natural-language request on the Shipment related activities.
- Create, Track & get a list of Delayed shipments.
- Empower George to do his job more efficently.


## Requirements & Prerequisites - already in place

1. Joule Studio in SAP Build 
    - Joule Studio with Agent Builder is enabled and accessible.
      
2.  Actions & Destinations
    - SAP Build Action projects - "GTTReadService" & "GTTShipment" to access the SAP Business Networks GTT System via the destinations mentioned below.
    -  BTP Destination "gttwriteservice" & "gttGetService" made available in SAP Build via Control Tower. 
 
3. SAP AI Core for document grounding 

    - Resource group created and assigned.
    - Document grounding pipeline set up and running.

## Exercises

<br> Below are the exercises. Please follow them in order to begin your hands-on session

- [Exercise 0 - Getting Started - Login to the Tenant](exercises/ex0/Getting%20Started%20-%20Login%20to%20the%20Tenant.md) 
- [Exercise 1 - Test the Action Project](exercises/ex1/Exercise%201%20-%20Test%20an%20Action%20Project.md) 
- [Exercise 2 - Create a Private Environment for Testing](exercises/ex2/Exercise%202%20-%20Create%20a%20Private%20Environment%20for%20Testing.md)
- [Exercise 3 - Understanding Joule Skills](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/Exercise%203%3A%20Understanding%20Joule%20Skills.md)
- [Exercise 3.0 -Create a new Joule Skill Package](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.0/Exercise%203.0%3A%20Create%20a%20new%20Joule%20Skill%20Package.md)
    - [Exercise 3.1.1 - Create a new Joule Skill](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.1/ex3.1.1/Exercise%203.1.1%3A%20Create%20a%20new%20Joule%20Skil.md)
    - [Exercise 3.1.2 - Create the second Joule Skill](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.1/ex3.1.2/Exercise%203.1.2%3A%20Create%20the%20second%20%20Joule%20Skill.md)
    - [Exercise 3.1.3 - Create your last Joule Skill](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.1/ex3.1.3/Exercise%203.1.3%20-%20Create%20final%20Joule%20Skill.md)
    - [Exercise 3.1.3a - Mapping Input variables of the Action project with Joule Skill Inputs](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.1/ex3.1.3/Exercise%203.1.3a%20-%20Mapping%20Input%20variables%20of%20the%20Action%20project%20with%20Joule%20Skill%20Inputs.md)
    - [Exercise 3.1.3b - Add Send Message steps in Joule Skill](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.1/ex3.1.3/Exercise%203.1.3b:%20Add%20a%20Condition%20and%20Send%20message%20in%20Joule%20Skill.md)

     
- [Exercise 4 -Creation of an Agent](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex4/Exercise%204%3A%20Create%20a%20Joule%20Agent.md)
    - [Exercise 4.1: Test an Agent in Private Environment](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex4/Exercise%204.1%3A%20Test%20an%20Agent%20in%20Private%20Environment.md)
- [Exercise 5 - Additional Section - Exercise to Release, Deploy and Test the Agent in Shared Environment]()




**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
