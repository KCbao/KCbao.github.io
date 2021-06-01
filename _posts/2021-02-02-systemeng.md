---
layout: post
title:  "System Engineering"
date:   2021-02-02 11:18:12 -0700
categories: system
---

## System Engineering Introduction

__What is system engineering__
* design, test, and evaluation to meet cost, schedule and techinical performance
    * understand customers needs (risk management etc)
    * subject to real-world constraints
    * design full scale development (system requirements, system design, etc.)
    * production and deployment

__Difference between software engineering__
* System engineering more focuses on design 
* Software engineering focuses more on implementation

__Software Development Life Cycle (SDLC)__
Software Development Life Cycle (SDLC) is a process used by the software industry to design, develop and test high quality softwares. There are some popular life-cycle models. 
* waterfall: In this Waterfall model, typically, the outcome of one phase acts as the input for the next phase sequentially. ![Waterfall Model](/assets/images/sdlc_waterfall_model.jpg)
    * Works well for smaller projects where requirements are very well understood. But High amounts of risk and uncertainty for long and ongoing projects.
    * difficult to measure progress within stages.
    * Cannot accommodate changing requirements.
* spiral: ![Spiral Model](/assets/images/sdlc_spiral_model.png) Risk-driven model
    * 一个典型的螺旋模型应该由以下的步骤构成：
        * 明确本迭代阶段的目标、备选方案以及应用备选方案的限制；
        * 对备选方案进行评估，明确并解决存在的风险，建立原型；
        * 当风险得到很好的分析与解决后，应用瀑布模型进行本阶段的开发与测试；
        * 对下一阶段进行计划与部署；
        * 与客户一起对本阶段进行评审；
    * When there is a budget constraint and risk evaluation is important. For medium to high-risk projects. End of the project may not be known early. Spiral may go on indefinitely. Not suitable for small or low risk projects and could be expensive for small projects.
* staged delivery: The staged delivery model involves the following steps: 
    * Software Concept
    * Requirements Analysis
    * Architectural Design
    * Stage 1, 2, ..., n, Repeat the following steps creating a potentially releasable product at the end of each stage. Each stage produces a more robust, complete version of the software.
        * Detailed Design
        * Code Construction and Unit Testing
        * System Testing
        * Release
* agile: ![Agile](/assets/images/sdlc_agile_model.jpg) In Agile, the tasks are divided to time boxes (small time frames) to deliver specific features for a release.
    * The product is tested very frequently, through the release iterations, minimizing the risk of any major failures in future.
    * Suitable for fixed or changing requirements
    * Little or no planning required.
    * Enables concurrent development and delivery within an overall planned context.

|Statement   |                            Waterfall  | Spiral| Staged Delivery| Agile|
|------------|---------------------------------------|-------|----------------|------|
|works with poorly understand requirements|Poor      |Excellent|Poor          |Excellent|
|works with poorly understand architecture|Poor      |Excellent|Poor          |Poor|
|can be constraint on a pre-defined schedule|Fair    |Poor|   Fair            |Excellent|
|allows midcourse correction|Poor                    |Excellent|Fair/Excellent|Excellent|
|provide customer with progress visibility|Poor      |Excellent|Excellent     |Excellent|

__V-diagram__
![V-diagram](/assets/images/v-diagram.png)
The left side of the "V" represents the decomposition of requirements, and creation of system specifications. The right side of the "V" represents integration of parts and their validation.

* Validation. The assurance that a product, service, or system meets the needs of the customer and other identified stakeholders. It often involves acceptance and suitability with external customers. Contrast with verification. (test if satisfy stakeholder's requirements)
* Verification. The evaluation of whether or not a product, service, or system complies with a regulation, requirement, specification, or imposed condition. It is often an internal process. Contrast with validation. (test if satisfy system requirements)