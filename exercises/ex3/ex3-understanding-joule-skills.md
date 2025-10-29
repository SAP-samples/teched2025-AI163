# Ex. 3: 💡 Understanding Joule Skills

**Joule Skills** are modular components within SAP’s conversational AI framework, designed to execute **atomic, predefined operations** within a business context.Each skill performs a single task — such as retrieving data, triggering transactions, or querying systems — based on structured inputs and deterministic logic. Their purpose is to streamline repetitive, rule-based activities by providing a **fast, reliable, and reusable automation mechanism**.

Functioning within clearly defined parameters, Joule Skills are ideal for **low-complexity, high-frequency operations** where consistency and precision are critical.  
They are tightly integrated with **SAP and third-party APIs** via **SAP Build Actions**, enabling seamless execution of system-level commands.  
While they can understand conversation context, their logic is **non-adaptive** — flows are static, and outcomes are predictable.


![Joule Skills Overview](Joule%20Skills.jpg)



> 💡 **Note:** Joule Skills can be triggered:
> 
>    - through SAP Joule’s conversational interface
>    - through another Joule Skills
>    - through Joule Agent



## 🧩 Build Your Joule Skills

In the next series of exercises, you will:
1.  Create a new Joule Skill Package to hold your work.
2.  Build three distinct Joule Skills: one for getting delayed shipments, one for tracking a shipment, and one for creating a shipment.
3.  Configure the inputs, outputs, and logic for each skill.

---

➡️ [Start Building: Ex. 3.0 - Create a new Joule Skill Package](ex3.0/ex3.0-create-joule-skill.md)

---

<details>
<summary><strong>Skill-Building Exercises (Full List for Reference)</strong></summary>

  - [Ex. 3.0 - Create a new Joule Skill Package](ex3.0/ex3.0-create-joule-skill.md)
  - **Get Delayed Shipments Skill**
    - [Ex. 3.1.1 - Build the "Get Delayed Shipments" Skill](ex3.1/ex3.1.1/ex3.1.1-create-get-delayed-skill.md)
  - **Track Shipment Skill**
    - [Ex. 3.1.2 - Build the "Track Shipment" Skill](ex3.1/ex3.1.2/ex3.1.2-create-track-shipment-skill.md)
  - **Create Shipment Skill**
    - [Ex. 3.1.3 - Part 1: Configure Inputs](ex3.1/ex3.1.3/ex3.1.3-create-create-shipment-skill-1.md)
    - [Ex. 3.1.3a - Part 2: Map Action Variables](ex3.1/ex3.1.3/ex3.1.3a-create-create-shipment-skill-2.md)
    - [Ex. 3.1.3b - Part 3: Add Conditional Messages](ex3.1/ex3.1.3/ex3.1.3b-create-create-shipment-skill-3.md)

</details>

---
  
<br> <br>  - [Back To Landing Page](../../README.md)
