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
        <b>Python libraries:</b>
        <ul class="two-column-list">
            <li>XGBoost</li>
            <li>SHAP</li>
            <li>scikit-learn</li>
            <li>Pandas</li>
            <li>NumPy</li>
            <li>SciPy</li>
            <li>statsmodels</li>
            <li>Matplotlib</li>
        </ul>
        <style>
          .two-column-list {
            columns: 2; /* Creates two columns */
            -webkit-columns: 2;
            -moz-columns: 2;
            list-style-position: inside; /* Ensures list bullets align */
            padding-left: 0;
          }

          .two-column-list li {
            display: inline-block;
            width: 100%;
          }
        </style>
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
        ASD, characterized by persistent deficits in communication and social interactions, along with restricted and repetitive behaviors, affects approximately 67 million individuals worldwide. The global prevalence of ASD is estimated to be around 2% and is steadily increasing. In the absence of an approved pharmacological treatment, symptom management relies on compensatory behavioral therapies, such as TEACCH and ABA, which are most effective when started early, during the peak of brain plasticity, before 2–3 years of age. Unfortunately, the current average age of diagnosis for these complex and heterogeneous disorders remains between 4 and 5 years, preventing timely interventions at the most critical developmental period.<br>
        <b>Early identification of children with ASD thus remains a significant global public health challenge.</b>
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
        <b>Rationale:</b><br>
        Our approach is based on a hypothesis, supported by clinical and histological evidence, that ASD originates in the perinatal period. According to this hypothesis, it may be possible to detect ASD markers through biological and ultrasound measurements routinely collected in pregnancy follow-ups and maternity clinics, from the first trimester through the first days after birth.
        <p>
        <b>Population:</b><br>
        To explore this, we conducted a retrospective analysis on a cohort of 63 children diagnosed with ASD at ages 2–5 years, along with an age-matched control group of 189 neurotypical (NT) children, all born in 2012–2013 at the Hospital of the University of Limoges in France.
        </p>
        <p>
        <b>Classification:</b><br>
        Given the large number of variables and the complex, multivariate, and poorly understood relationships among them, we employed advanced statistical tools to identify distinguishing patterns between NT and ASD groups. A supervised machine learning (ML) algorithm, XGBoost, was trained to classify newborns into ASD and NT categories. In line with ethical considerations, the model was designed to maintain a false positive rate below 5% while maximizing sensitivity. To ensure the classifier's robustness and generalizability, as well as to optimize hyperparameters, a nested cross-validation (CV) approach was utilized. The variables most influential in the classifier's decisions were identified using SHAP (SHapley Additive exPlanations) analysis.
        </p>
        <p>
        <b>Statistical tests and modelling:</b><br>
        Simultaneously, traditional statistical hypothesis tests were applied to detect significant differences in the distributions of collected variables between NT and ASD groups.The Benjamini–Hochberg procedure was employed to control the false discovery rate for multiple comparisons. Additionally, we analyzed longitudinal developmental trajectories of head circumference (HC) growth in fetuses using statistical models such as ANCOVA and quadratic mixed-effect models. These analyses aimed to explore whether the megalencephalic brains observed in children and adolescents with ASD could originate during fetal development.
        </p>
        <p>
        This multi-faceted approach integrates advanced machine learning with conventional statistical methods to uncover potential biomarkers and developmental patterns associated with ASD.
        </p>
        {{< figure src="pelargos-how.png" alt="Figure: Methods used in Pelargos" >}}
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
          <b>Trained ASD classifier</b><br>
          The primary outcome of the project is a trained classifier, which serves as the core component of the Pelargos medical device. Regarding our training strategy, aimed at maintaining the false positive rate below 5% while maximizing sensitivity, the performance of the classifier, measured by a CV technique, is summerized in the table below:
        <table>
          <tbody>
            <tr>
              <td><b>Score</b></td>
              <td><b>Description</b></td>
              <td><b>Value</b></td>
            </tr>
            <tr>
              <td>Specificity</td>
              <td>Ability to correctly identify neurotypical cases (true negatives)</td>
              <td>96%±1%</td>
            </tr>
            <tr>
              <td>Sensitivity</td>
              <td>Ability to correctly identify ASD cases (true positives)</td>
              <td>41%±4%</td>
            </tr>
            <tr>
              <td>PPV</td>
              <td>Proportion of positive results that are true positives (precision)</td>
              <td>7%±5%</td>
            </tr>
          </tbody>
        </table>
        <p>
          <b>Interpretation of the classifier's output</b><br>
          The SHAP analysis provided valuable insights into the classification results, identifying variables that significantly influence the classifier's performance. From a clinical perspective, these variables hold potential as biomarkers for ASD. Below are the 5 most impactful variables:
          {{< figure src="Pelargos-results-shap.png" alt="Figure: SHAP analysis" >}}
          Each row represents a variable, with a point colored according to its corresponding value for each subject. The color map illustrates how the impact of each variable varies with its values. Values on the positive (orange) or negative (green) side of the SHAP distribution correspond to classifications of ASD or NT, respectively. The following table presents the variables, along with the value ranges that drive the classifier toward an ASD diagnosis.
        </p>
        <table>
          <tbody>
            <tr>
              <td><b>Variable</b></td>
              <td><b>Relative Impact</b></td>
              <td><b>Critical Value Range for ASD Classification</b></td>
            </tr>
            <tr>
              <td>Timing of fetal rotation on head</td>
              <td>44%</td>
              <td>Earlier than 148 days of gestational age</td>
            </tr>
            <tr>
              <td>White blood cell count in the third trimester</td>
              <td>16%</td>
              <td>Less than 9100</td>
            </tr>
            <tr>
              <td>Femur length percentile in the third trimester</td>
              <td>13%</td>
              <td>Higher than 72%</td>
            </tr>
            <tr>
              <td>Sex</td>
              <td>9%</td>
              <td>Male</td>
            </tr>
            <tr>
              <td>Newborn feeding</td>
              <td>5%</td>
              <td>Mixed (breastfeeding and artificial)</td>
            </tr>
          </tbody>
        </table>
        <p>
          <b>Statistical hypothesis testing</b><br>
          Statistical hypothesis testing identified 5 variables with significant differences between the ASD and NT groups, suggesting their potential as biomarkers for ASD.
          {{< figure src="Pelargos-stat-test.png" alt="Figure: Statistical hypothesis test analysis results" >}} 
          The statistical details are summarized in the table below.
          {{< figure src="Pelargos-stat-test-table.png" alt="Table: Statistical hypothesis test analysis results" >}} 
        </p>
        <p>
          <b>Analysis of fetal developmental trajectories</b><br>
          Through the analysis of fetal developmental trajectories, we identified a distinct subgroup of ASD subjects with significantly larger head circumferences (HCs) compared to both age-matched neurotypical (NT) peers and other ASD subjects during the second (T2) and third trimesters(T3), as well as prior to birth.
          {{< figure src="Pelargos-head-circumference.png" alt="Figure: identification of a subpopulation of ASD subjects with significantly larger head circumferences." >}}
        </p>
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
      <b>World’s First Breakthrough</b><br>
      Pelargos is the first-ever medical test capable of identifying ASD right after birth. Unlike existing tests in research phase, which can only be performed at least six months after birth, Pelargos empowers parents and healthcare providers by offering a critical head start. By identifying newborns at risk, Pelargos unlocks a vital six-month advantage during the peak neuroplasticity period (ages 2–3), enabling early interventions that can significantly impact a child's development trajectory.
      <p>
        <b>Ethical Assurance</b><br>
        We fully understand the anxiety and stress that a false identification of ASD in a newborn can cause for parents. To address this critical concern, and in alignment with ethical principles, our classifier model has been meticulously designed to minimize the false positive rate to below 5%, while simultaneously maximizing the true positive rate. This ensures that the tool is both accurate and responsible, prioritizing the well-being of families while striving for effective early detection.
      </p>
      <p>
        <b>Non-invasive Detection</b><br>
        At the core of Pelargos is an advanced AI-driven method that assesses ASD risk without the need for invasive procedures. By analyzing routine biological and ultrasound data collected during pregnancy and shortly after birth, Pelargos ensures a safe, stress-free, and reliable approach to early detection.
      </p>
      <p>
        <b>Affordable</b><br>
        Pelargos leverages existing clinical data routinely collected during pregnancy and after birth, eliminating the need for additional medical procedures. This innovative approach ensures accessibility and affordability, making early ASD detection feasible for families worldwide.
      </p>
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
      With the proof-of-concept phase successfully completed, Pelargos is now advancing toward market readiness. To achieve this, we are <b>partnering with leading maternity hospitals across France</b> to expand our database, refine the classification model with a larger and more diverse cohort, and <b>enhance the test’s sensitivity</b>. The next step will involve transitioning to the <b>validation phase</b> where the classifier will be rigorously tested on external datasets. This critical phase aims to confirm the test’s reliability and generalizability, ensuring its effectiveness for future real-world applications.
      <table>
        <tbody>
          <tr>
            <td><b>Phase</b></td>
            <td><b>Goals & Achievements</b></td>
            <td><b>Works Completed/Underway</b></td>
          </tr>
          <tr>
            <td>✅ Proof-of-Concept</td>
            <td>Demonstrated the feasibility of using AI for ASD detection based on perinatal data.</td>
            <td>Built and tested an initial classifier on a cohort of 63 ASD and 189 neurotypical children.</td>
          </tr>
          <tr>
            <td>⏳ Development</td>
            <td>Expand the database, improve sensitivity, and fine-tune the classifier with diverse datasets.</td>
            <td>Collaborating with leading maternity hospitals in France to collect more comprehensive data.</td>
          </tr>
          <tr>
            <td>🔜 Validation</td>
            <td>Validate the classifier's generalizability on external datasets to prepare for market entry.</td>
            <td>Test classifier with unseen data and assess its real-world performance.</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</div>
