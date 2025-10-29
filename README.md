> [!IMPORTANT]
> **Welcome to the Agent Builder Lab Preview!**
>
> You are working with a **pre-release version** of the Agent Builder in Joule Studio. This gives you an early look at our upcoming capabilities. Please keep the following in mind:
>
> *   **Features Are Subject to Change:** The user interface (UI), terminology, and functionalities you see in this lab may differ from the final, generally available (GA) product.
> *   **For Educational Use Only:** This environment is designed for learning and experimentation, not for production use.
> *   **Potential Instability:** As a preview version, you may encounter occasional instability or minor bugs. The exercises are designed to work with the current state of the platform. If you get stuck, please notify a session instructor.

# AI163 - Get hands-on to extend Joule and build AI Agents

## Description

This exercise shows how to build a simple custom Joule Agent in Joule Studio that uses multiple Joule Skills along with Document Grounding via AI Core to manage shipments in the SAP Business Networks Global Track and Trace (GTT) system. The agent can create shipments, get delayed shipment details, and even track details of existing shipments. It uses Document Grounding to read a shipment rate card document and determine the most economically viable shipment carrier based on their rates, source, and destination locations while creating a shipment.

## Overview

### Business problem and persona

Before diving into the use case, let's take a moment to get acquainted with our business user. It's really important to understand the business user as thoroughly as possible before building your custom Joule Agent.

Meet George, a Logistics Coordinator at a global manufacturing company. Every day, George is responsible for creating, tracking, and managing shipments across multiple transportation partners using SAP Business Networks Global Track and Trace — or GTT for short. His job is to ensure that every delivery — from raw materials to finished goods — reaches the customer on time and in full.

#### Persona — Logistics Coordinator
<img width="747" height="432" alt="image" src="https://github.com/user-attachments/assets/d955078e-3896-4a28-b504-6a330525b36e" />

#### Pain Points — Logistics Coordinator
<img width="741" height="468" alt="image" src="https://github.com/user-attachments/assets/edaf66c0-fcd0-4b49-aac9-143a6e96e8a4" />

### You will build a goal-driven Joule Agent in Joule Studio that:

- Understands natural-language requests on Shipment-related activities.
- Can create, track, and get a list of delayed shipments.
- Empowers George to do his job more efficiently.

## Requirements & Prerequisites - already in place

All required backend systems and configurations have been pre-provisioned for this session. This includes:

1.  **Joule Studio in SAP Build**:
    - Agent Builder is enabled and accessible.

2.  **Actions & Destinations**:
    - SAP Build Action projects (`GTTReadService` & `GTTShipment`) are pre-built to access the SAP Business Networks GTT System.
    - BTP Destinations (`gttwriteservice` & `gttGetService`) are available in SAP Build.

3.  **SAP AI Core for document grounding**:
    - A resource group and document grounding pipeline are set up and running.

---


## Begin Your Hands-On Session

Please follow the exercises in order. Each exercise page will link to the next one.

➡️ **[Start Here: Ex. 0 - Getting Started](exercises/ex0/ex0-getting-started.md)**

---

<details>
<summary><strong>Table of Contents (Click to expand for full exercise list)</strong></summary>

- **Setup & Basics**
  - [Ex. 0 - Getting Started - Login to the Tenant](exercises/ex0/ex0-getting-started.md)
  - [Ex. 1 - Test the Action Project](exercises/ex1/ex1-test-action-project.md)
  - [Ex. 2 - Create a Private Environment for Testing](exercises/ex2/ex2-create-private-environment.md)
- **Building Joule Skills**
  - [Ex. 3 - Understanding Joule Skills](exercises/ex3/ex3-understanding-joule-skills.md)
  - [Ex. 3.0 - Create a new Joule Skill Package](exercises/ex3/ex3.0/ex3.0-create-joule-skill.md)
  - [Ex. 3.1.1 - Build the "Get Delayed Shipments" Skill](exercises/ex3/ex3.1/ex3.1.1/ex3.1.1-create-get-delayed-skill.md)
  - [Ex. 3.1.2 - Build the "Track Shipment" Skill](exercises/ex3/ex3.1/ex3.1.2/ex3.1.2-create-track-shipment-skill.md)
  - [Ex. 3.1.3 - Build the "Create Shipment" Skill (Part 1)](exercises/ex3/ex3.1/ex3.1.3/ex3.1.3-create-create-shipment-skill-1.md)
  - [Ex. 3.1.3a - Build the "Create Shipment" Skill (Part 2 - Mapping)](exercises/ex3/ex3.1/ex3.1.3/ex3.1.3a-create-create-shipment-skill-2.md)
  - [Ex. 3.1.3b - Build the "Create Shipment" Skill (Part 3 - Messaging)](exercises/ex3/ex3.1/ex3.1.3/ex3.1.3b-create-create-shipment-skill-3.md)
- **Building & Testing the Agent**
  - [Ex. 4 - Create a Joule Agent](exercises/ex4/ex4-create-joule-agent.md)
  - [Ex. 4.1 - Test an Agent in Private Environment](exercises/ex4/ex4.1-test-joule-agent.md)
- **Deployment**
  - [Ex. 5 - Release, Deploy and Test in Shared Environment](exercises/ex5/ex5-release-deploy-test-agent.md)

</details>

---

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support
Support for the content in this repository is available during the actual time of the online session. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
