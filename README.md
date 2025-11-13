# 🧬 Medical Data Analysis for **Duchenne Muscular Dystrophy (DMD)**

## 🧠 Function: `create_Age_at_diagnosis(row)`

### 🎯 Purpose:

To generate a **logical age of diagnosis** that corresponds to the
**current age** of the patient.

### 🧩 Medical Logic:

-   DMD is usually **diagnosed between 3 and 10 years old**.\
-   The **diagnosis age** cannot exceed the **current age**.\
-   Minimum possible diagnosis age: **3 years** (rarely earlier).\
-   Maximum possible diagnosis age: **10 years** (often detected
    earlier).

``` python
def create_Age_at_diagnosis(row):
    """
    Function to generate the age of diagnosis based on the current age
    using logical constraints consistent with DMD clinical patterns.
    """
    current_age = row['Age']
    max_age_rand = min(10, current_age)
    if max_age_rand >= 3:
        return np.random.randint(3, max_age_rand + 1)
    else:
        return 3
```

------------------------------------------------------------------------

## ⚧️ Gender Distribution

The percentage of **males** is intentionally higher than **females**,
because: - **Males** are the ones who **develop and exhibit** the
disease.\
- **Females** are typically **carriers** of the defective gene and
usually **do not show symptoms**.

------------------------------------------------------------------------

## 🚶‍♂️ Mobility Status by Age

  Age Group        Stage                   Mobility Ability       Approximate Percentage
  ---------------- ----------------------- ---------------------- ------------------------
  Under 10 years   Early Stage             Able to walk           ✅ Most can walk
  10--12 years     Transitional Stage I    \~75% can walk         ⚖️
  12--15 years     Transitional Stage II   \~80% unable to walk   ❌
  Over 15 years    Advanced Stage          Unable to walk         🚫 Nearly all

------------------------------------------------------------------------

## 🧫 Gene Mutation Types

Three main mutation types are seen in DMD, each with a different
frequency and severity:

  Mutation Type        Incidence Rate   Severity Level
  -------------------- ---------------- --------------------
  **Deletion**         65--70%          Moderate to Severe
  **Point Mutation**   20--25%          Variable
  **Duplication**      10--15%          Mild to Moderate

### 🔍 Mutation Examples

#### 🧬 Deletion Examples

-   `Exon 45`\
-   `Exon 45–50`\
-   `Exon 48–52`\
-   `Exon 3–7`

#### 🔁 Duplication Examples

-   `Exon 2`\
-   `Exon 44`\
-   `Exon 8–9`

#### 🎯 Point Mutation Examples

-   `Exon 23`\
-   `Exon 51`\
-   `Exon 14`

------------------------------------------------------------------------

## 👨‍👩‍👦 Family History

-   Approximately **30--40%** of DMD cases are **inherited** (positive
    family history).\
-   The remaining **60--70%** are due to **new mutations (de novo)**
    with **no family history**.

------------------------------------------------------------------------

## 🧪 Creatine Kinase (CK) Levels

-   In children with DMD, **CK levels** peak at **10--20× the upper
    normal limit** around the age of **2 years**.\
-   Levels then **decrease by about 25% per year** as muscle tissue is
    gradually replaced by **fat and fibrotic tissue**.\
-   In **female carriers**, CK levels are **normal**.\
-   In **advanced disease**, CK levels may **return to normal** due to
    extensive muscle loss.

------------------------------------------------------------------------

## 💊 Steroid Therapy

### 📊 Treatment Statistics:

-   In a large U.S. study, **84% of males with DMD** received steroid
    therapy by **age 8** (peak usage).\
-   The rate of steroid use **gradually declines** after **age 10**.

### 🚫 Reasons for Not Starting Therapy:

-   Parental concerns about **side effects**.\
-   **Lack of a medical prescription**.

------------------------------------------------------------------------

### 🕒 Optimal Time to Begin Treatment:

-   **Age Range:** Typically between **4--6 years old**.\
-   **Functional Stage:** When **motor skills** (running, jumping) have
    **plateaued or begun to decline**, but **independent walking is
    still possible**.\
-   This corresponds to the **intermediate stage** of disease
    progression.

------------------------------------------------------------------------

## ❤️ Left Ventricular Ejection Fraction (LVEF%)

### 🔻 Patients **Not Receiving Steroid Therapy**

-   **Faster deterioration** of cardiac function.\
-   **Heart failure** develops **earlier and more frequently**.\
-   **Onset:** Usually between **10--14 years old**.\
-   By **age 18**, almost all patients show **reduced LVEF**.\
-   **Values:**
    -   LVEF \< 55% → indicates dysfunction.\
    -   LVEF \< 40% or \< 30% → indicates severe heart failure.

📌 **Summary:**\
Without steroids, cardiac deterioration is **rapid and progressive**,
leading to **early heart failure** and a **sharp LVEF decline**.

------------------------------------------------------------------------

### 💪 Patients **Receiving Steroid Therapy**

-   **Clear protective effect:** Steroids (e.g., *prednisone*,
    *deflazacort*) slow skeletal muscle atrophy and protect **cardiac
    muscle**.\
-   **Slower LVEF decline:** Steroid therapy **delays the onset** of
    cardiomyopathy for several years.\
-   **Lower incidence of heart failure.**\
-   **LVEF remains \>50--55%** for a longer time.\
-   Even when decline begins, it occurs **gradually**, reducing risk of
    severe cardiac failure.

📌 **Summary:**\
Steroid therapy **significantly reduces** the rate and severity of
**cardiomyopathy in DMD**, delays its onset, and **preserves LVEF**
within healthy ranges for longer periods.

------------------------------------------------------------------------

## 🌟 Overall Summary

-   DMD is a **genetically complex and progressive** disorder.\
-   **Early diagnosis** and **appropriate steroid therapy** dramatically
    **improve life quality and outcomes**.\
-   **Data-driven analysis** of clinical variables (age, mobility, gene
    type, therapy) allows for **accurate modeling** of disease
    progression.

------------------------------------------------------------------------

