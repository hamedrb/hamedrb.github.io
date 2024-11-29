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

publication:
  - caly-2021
---

{{% callout note %}}
The project has successfully completed the proof-of-concept phase and is currently progressing through Phase 1.{{% /callout %}}

- **What:** Pelargos project, powered by artificial intelligence, has two key goals: developing a cutting-edge medical device for the early prognosis of Autism Spectrum Disorders (ASD) in newborns and identifying new ASD biomarkers. By leveraging data routinely collected during pregnancy follow-ups, childbirth, and the first days of life, the device aims to enable timely interventions, improving outcomes for children at risk. Simultaneously, the identification of biomarkers will open new research pathways, shedding light on the unknown underlying mechanisms and early indicators of ASD, fostering innovation in both clinical and scientific fields.

{{< figure src="pelargos-what.png" alt="What is Pelargos project?" >}}

- **Why:** Autism Spectrum Disorder (ASD), characterized by persistent deficits in communication and social interactions, along with restricted and repetitive behaviors, affects approximately 67 million individuals worldwide. The global prevalence of ASD is estimated to be around 2% and is steadily increasing. In the absence of an approved pharmacological treatment, symptom management relies on compensatory behavioral therapies, such as TEACCH and ABA, which are most effective when started early—during the peak of brain plasticity, before 2–3 years of age. Unfortunately, the current average age of diagnosis for these complex and heterogeneous disorders remains between 4 and 5 years, preventing timely interventions at the most critical developmental period. Early identification of children with ASD thus remains a significant global public health challenge.

{{< figure src="pelargos-why.png" alt="ASD in numbers: Why Pelargos is needed?" >}}

- **How:** Clinical and histological evidence suggests that Autism Spectrum Disorder (ASD) originates in utero. To investigate this hypothesis, we analyzed biological and ultrasound measurements routinely collected in maternity clinics from the first trimester of pregnancy through the first days after birth. The goal was to determine whether these data could support an early prognosis of ASD. Retrospective analysis was performed on a cohort of 63 children diagnosed with ASD at 4–5 years of age, compared to an age-matched control group of 189 neurotypical (NT) children.

    Given the large number of variables and the complex, multivariate, and poorly understood relationships among them, we employed advanced statistical tools to identify distinguishing patterns between NT and ASD groups. A supervised machine learning (ML) algorithm, XGBoost, was trained to classify newborns into ASD and NT categories. The model was designed to maintain a false positive rate below 5% while maximizing sensitivity. To ensure the robustness and generalizability of the classifier, a cross-validation (CV) technique was employed. The variables most influential in the classifier's decisions were identified using SHAP (SHapley Additive exPlanations) analysis.

    Simultaneously, traditional statistical hypothesis tests were applied to detect significant differences in the distributions of collected variables between NT and ASD groups. Additionally, we analyzed longitudinal developmental trajectories of head circumference (HC) growth in fetuses using statistical models such as ANCOVA and quadratic mixed-effect models. These analyses aimed to explore whether the megalencephalic brains observed in children and adolescents with ASD could originate during fetal development.

    This multi-faceted approach integrates advanced machine learning with conventional statistical methods to uncover potential biomarkers and developmental patterns associated with ASD.

{{< figure src="pelargos-how.png" alt="Methods used in Pelargos." >}}

- **Results:**
1) This analysis resulted in the first version of a trained classifier that is the backbone of the medical device that we are developing. Regarding our training strategy, the performance of the classifier, measured by CV technique, is given in the following table:

TABLE

Moreover, the interpretation of the classification results by SHAP analysis revealed variables that impact the classifier's function. Clinically speaking, those variables could be considered as ASD biomarkers. Here are the most impactuf variables:

{{< figure src="example-image.jpg" title="Beautiful Landscape" alt="A breathtaking view" >}}

2) Statistical hypothesis tests revealed 5 variables that are significantly different between ASD and NT groups and can be considered as ASD biomarkers.

TABLE

3) By analysing different fetal developmental trajectories we identified a subpopulation of ASD subjects with significantly larger HCs than age-matched NTs during the 2nd and 3rd trimesters and before birth.

{{< figure src="example-image.jpg" title="Beautiful Landscape" alt="A breathtaking view" >}}

- **Next steps:**

{{< figure src="example-image.jpg" title="Beautiful Landscape" alt="A breathtaking view" >}}