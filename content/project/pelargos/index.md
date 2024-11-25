---
title: 'Pelargos: An AI Tool for Identification of ASD in Newborns'

date: 2024-11-25

summary: Assessment of Autism Risk in Newborns Through Analysis of Routine Maternity Data

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
The project has passed successfully the proof-of-concept phase and is actually in phase 1.
{{% /callout %}}

Pelargos blablabla:

- **What:** This project focuses on creating a cutting-edge medical device powered by artificial intelligence to identify early indicators of Autism Spectrum Disorders (ASD) in newborns. By analyzing data collected immediately after birth, the device aims to enhance early detection, enabling timely interventions and better outcomes for children at risk. The innovation seeks to bridge gaps in neonatal care and ASD diagnosis, promoting precision medicine in pediatric health.

- **Why:** ASD, characterized by persistent communication and social interactions deficits, and restricted and repetitive behaviors, affected about 67 million individuals in the world. The global prevalence of ASD is estimated to be  approximately 2% and continues to rise steadily. In the absence of an approved pharmacological treatment, symptom improvement relies on compensatory behavioral therapies (e.g., TEACCH, ABA). These therapies are most effective when initiated early, during the peak of brain plasticity (around 2–3 years of age). However, the current average age of diagnosis for these complex and heterogeneous disorders remains between 4 and 5 years, preventing timely interventions at the most critical developmental period. Early identification of children with ASD is a major global public health challenge.

{{< figure src="example-image.jpg" title="Beautiful Landscape" alt="A breathtaking view" >}}

- **How:** Clinical and histological observations suggest that ASD is generated in-utero. So, we analyzed biological and ultrasound measurements routinely collected in maternities from the first
pregnancy trimester to 1 day after birth to determine if they could enable a prognosis of ASD at birth. To this aim, we compared retrospectively maternity parameters in babies diagnosed 4–5 years later with ASD, and in an age-matched population of neurotypical (NT) babies. Due to the large number of features and complex multivariate and poorly understood links between them, we used several statistical tools to reveal patterns that distinguish NT babies from those with ASD. A supervised machine learning (ML) algorithm was trained to classify babies in two groups, ASD and NT while taking a strategy to keep the false positive rate below 5% and maximizing the sensitivity. A cross-validation (CV) technique was used to ensure the generalizability of the classifier’s results on an unseen independent cohort. The features with the highest impact on the classifier’s decisions were identified and analyzed more precisely. In parallel, significant changes in the distribution of all collected features between NT and ASD babies were identified through conventional statistical hypothesis tests. Finally, the longitudinal developmental trajectories of head circumference (HC) growth in fetuses were analyzed by statistical models to investigate the possibility that megalencephalic ASD brains in children and adolescents are generated in utero.

{{< figure src="example-image.jpg" title="Beautiful Landscape" alt="A breathtaking view" >}}

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