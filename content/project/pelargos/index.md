---
title: 'Pelargos: An AI-based Medical Device for Prognosis of ASD in Newborns'

date: 2024-11-25

summary: Assessment of autism risk in newborns through the analysis of maternity care data routinely collected during pregnancy follow-ups and childbirth

authors:
  - admin

tags:
  - AI
  - Data mining
  - Classification
  - ASD
  - Medicine

# Is this a featured project? (true/false)
featured: true

image:
  # caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/bzdhc5b3Bxs)'
  # focal_point: Right

links:
  - name: Publication
    url: https://www.nature.com/articles/s41598-021-86320-0
#  - icon: twitter
#    icon_pack: fab
#    name: Follow
#    url: https://twitter.com/georgecushen
# url_code: 'https://github.com'
# url_pdf: ''
# url_slides: 'https://slideshare.net'
# url_video: 'https://youtube.com'

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects:
#   - example

# Usage of info box after ---
# {{% callout note %}}
# The project has successfully completed the proof-of-concept phase and is currently progressing through Phase 1.{{% /callout %}}

# Usage of my custom box after ---
# <div class="light-blue-box">
# This is my text inside a frame with a light blue background.
# </div>

publication:
  - caly-2021


# List of tools and packages used: Python, pandas, XGBoost, etc.
# {{< figure src="XGBoost_logo.png" alt="Figure: XGBoost logo" >}}




# - **Why:** 

# - **How:** Clinical and histological evidence suggests that ASD originates in-utero. To investigate this hypothesis, we analyzed biological and ultrasound measurements routinely collected in maternity clinics from the first trimester of pregnancy through the first days after birth. The goal was to determine whether these data could support an early prognosis of ASD. Retrospective analysis was performed on a cohort of 63 children diagnosed with ASD at 4–5 years of age, compared to an age-matched control group of 189 neurotypical (NT) children.

#     Given the large number of variables and the complex, multivariate, and poorly understood relationships among them, we employed advanced statistical tools to identify distinguishing patterns between NT and ASD groups. A supervised machine learning (ML) algorithm, XGBoost, was trained to classify newborns into ASD and NT categories. The model was designed to maintain a false positive rate below 5% while maximizing sensitivity. To ensure the robustness and generalizability of the classifier, a cross-validation (CV) technique was employed. The variables most influential in the classifier's decisions were identified using SHAP (SHapley Additive exPlanations) analysis.

#     Simultaneously, traditional statistical hypothesis tests were applied to detect significant differences in the distributions of collected variables between NT and ASD groups. Additionally, we analyzed longitudinal developmental trajectories of head circumference (HC) growth in fetuses using statistical models such as ANCOVA and quadratic mixed-effect models. These analyses aimed to explore whether the megalencephalic brains observed in children and adolescents with ASD could originate during fetal development.

#     This multi-faceted approach integrates advanced machine learning with conventional statistical methods to uncover potential biomarkers and developmental patterns associated with ASD.

#     {{< figure src="pelargos-how.png" alt="Figure: Methods used in Pelargos" >}}

# - **Results:**
#     1) **Trained ASD classifier:**
#         The primary outcome of the project is a trained classifier, which serves as the core component of the Pelargos medical device. Regarding our training strategy, aimed at maintaining the false positive rate below 5% while maximizing sensitivity, the performance of the classifier, measured by a CV technique, is summerized in the table below:
    
#         | Score        | Description                     | Value   |
#         | :----------- | :------------------------------ | :-----: |
#         | Specificity  | Ability to correctly identify neurotypical cases (true negatives) | 96%±1%  |
#         | Sensitivity  | Ability to correctly identify ASD cases (true positives) | 41%±4%  |
#         | PPV          | Proportion of positive results that are true positives (precision) | 7%±5%  |
    
#         **Interpretation of the classifier's output:**
#         The SHAP analysis provided valuable insights into the classification results, identifying variables that significantly influence the classifier's performance. From a clinical perspective, these variables hold potential as biomarkers for ASD. Below are the 5 most impactful variables:
    
#         {{< figure src="Pelargos-results-shap.png" alt="Figure: SHAP analysis" >}}

#         Each row represents a variable, with a point colored according to its corresponding value for each subject. The color map illustrates how the impact of each variable varies with its values. Values on the positive (orange) or negative (green) side of the SHAP distribution correspond to classifications of ASD or NT, respectively. The following table presents the variables, along with the value ranges that drive the classifier toward an ASD diagnosis.

#         | Variable        | Relative impact                     | Critical Value Range for ASD Classification   |
#         | :-------------- | :----------------------------------: | :------------------------------------------- |
#         | Timing of fetal rotation on head | 44% | Earlier than 148 days of gestational age |
#         | white blood cell count in the third trimester  | 16% | Less than 9100  |
#         | Femur length percentile in the third trimester | 13% | Higher than 72%  |
#         | Sex | 9% | Male |
#         | Newborn feeding | 5% | Mixed (breastfeeding and artificial) |

#     2) Statistical hypothesis testing identified 5 variables with significant differences between the ASD and NT groups, suggesting their potential as biomarkers for ASD.

#        {{< figure src="Pelargos-stat-test.png" alt="Figure: Statistical hypothesis test analysis results" >}} 

#        The statistical details are summarized in the table below.

#        {{< figure src="Pelargos-stat-test-table.png" alt="Table: Statistical hypothesis test analysis results" >}} 

#     3) Through the analysis of fetal developmental trajectories, we identified a distinct subgroup of ASD subjects with significantly larger head circumferences (HCs) compared to both age-matched neurotypical (NT) peers and other ASD subjects during the second (T2) and third trimesters(T3), as well as prior to birth.

#         {{< figure src="Pelargos-head-circumference.png" alt="Figure: identification of a subpopulation of ASD subjects with significantly larger head circumferences." >}}

# - **Next steps:**

# {{< figure src="example-image.jpg" title="Beautiful Landscape" alt="A breathtaking view" >}}

---

<div class="info-box overview">
  <div class="content">
    <div class="title-container">
      <div class="icon">📝</div>
      <div class="title">Overview</div>
    </div>
    <div class="description">
        Pelargos project, powered by artificial intelligence, has two key goals: developing a cutting-edge medical device for the early prognosis of Autism Spectrum Disorders (ASD) in newborns and identifying new ASD biomarkers. By leveraging data routinely collected during pregnancy follow-ups, childbirth, and the first days of life, the device aims to enable timely interventions, improving outcomes for children at risk. Simultaneously, the identification of biomarkers will open new research pathways, shedding light on the unknown underlying mechanisms and early indicators of ASD, fostering innovation in both clinical and scientific fields.
        {{< figure src="pelargos-what.png" alt="Figure: What is the Pelargos project?" >}}
    </div>
  </div>
</div>

<div class="info-box tools">
  <div class="content">
    <div class="title-container">
      <div class="icon">🛠️</div>
      <div class="title">Tech Stack</div>
    </div>
    <div class="description">
        Tech Tech Tech Tech Tech
    </div>
  </div>
</div>

<div class="info-box challenge">
  <div class="content">
    <div class="title-container">
      <div class="icon">🔒</div>
      <div class="title">Challenge</div>
    </div>
    <div class="description">
        ASD, characterized by persistent deficits in communication and social interactions, along with restricted and repetitive behaviors, affects approximately 67 million individuals worldwide. The global prevalence of ASD is estimated to be around 2% and is steadily increasing. In the absence of an approved pharmacological treatment, symptom management relies on compensatory behavioral therapies, such as TEACCH and ABA, which are most effective when **started early, during the peak of brain plasticity, before 2–3 years of age. Unfortunately, the current average age of diagnosis for these complex and heterogeneous disorders remains between 4 and 5 years, preventing timely interventions at the most critical developmental period. Early identification of children with ASD thus remains a significant global public health challenge.
        {{< figure src="pelargos-why.png" alt="Figure: ASD in numbers--Why Pelargos is needed?" >}}
    </div>
  </div>
</div>

<div class="info-box approach">
  <div class="content">
    <div class="title-container">
      <div class="icon">🔑</div>
      <div class="title">Approach</div>
    </div>
    <div class="description">
        Approach Approach Approach Approach Approach
    </div>
  </div>
</div>

<div class="info-box impact">
  <div class="content">
    <div class="title-container">
      <div class="icon">🌟</div>
      <div class="title">Impact</div>
    </div>
    <div class="description">
        impact impact impact impact impact
    </div>
  </div>
</div>

<div class="info-box innovation">
  <div class="content">
    <div class="title-container">
      <div class="icon">💡</div>
      <div class="title">Innovation</div>
    </div>
    <div class="description">
        innovation innovation innovation innovation innovation
    </div>
  </div>
</div>

<div class="info-box perspective">
  <div class="content">
    <div class="title-container">
      <div class="icon">🔭</div>
      <div class="title">Perspective</div>
    </div>
    <div class="description">
        Perspective Perspective Perspective Perspective Perspective
    </div>
  </div>
</div>
