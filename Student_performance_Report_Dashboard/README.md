<div align="center">

<img src="Dashboard_Overview/banner.svg" alt="Student Performance Dashboard banner" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=22&pause=1000&color=15803D&center=true&vCenter=true&width=640&lines=Track+Performance%2C+Identify+Potential%3B;1%2C000+Students+%C2%B7+2+Pages+%C2%B7+1+Dashboard;Built+with+Power+BI+%F0%9F%93%8A" alt="Typing SVG" />

<br/>

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-8_Measures-15803D?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power_Query-4_CSV_Sources-0EA5E9?style=for-the-badge)
![Students](https://img.shields.io/badge/Students-1%2C000-CA8A04?style=for-the-badge)
![Records](https://img.shields.io/badge/Records-137%2C500-22C55E?style=for-the-badge)
![Pages](https://img.shields.io/badge/Pages-2-A855F7?style=for-the-badge)
![Visuals](https://img.shields.io/badge/Data_Visuals-26-F97316?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-10B981?style=for-the-badge)

<br/>

[![Dashboard Overview](https://img.shields.io/badge/%F0%9F%96%BC_Dashboard_Overview-15803D?style=for-the-badge)](#-dashboard-overview)
[![Page 1](https://img.shields.io/badge/%F0%9F%93%98_Page_1-Academic-0EA5E9?style=for-the-badge)](#-page-1--academic-performance)
[![Page 2](https://img.shields.io/badge/%F0%9F%93%99_Page_2-Behavioral-CA8A04?style=for-the-badge)](#-page-2--behavioral-insights)
[![DAX](https://img.shields.io/badge/%F0%9F%A7%AE_DAX-Measures-A855F7?style=for-the-badge)](#-dax--measures--calculated-columns)
[![How to Open](https://img.shields.io/badge/%E2%96%B6_How_to_Open-10B981?style=for-the-badge)](#-how-to-open--use)

<br/>

> 🚀 A **two-page Power BI report (EduTRACK)** that turns **137,500 school records** — scores, attendance and behaviour logs for **1,000 students** across the **2024–25 academic session** — into an interactive dashboard with KPI cards, charts, tables and written key insights.

</div>

---

## 📑 Table of Contents

1. [Overview](#-overview)
2. [Problem Statement](#-problem-statement)
3. [Features](#-features)
4. [Key Features](#-key-features)
5. [Project Structure](#-project-structure)
6. [Dashboard Layout](#-dashboard-layout)
7. [Data Preparation (Power Query)](#-data-preparation-power-query)
8. [Data Model & Relationships](#-data-model--relationships)
9. [DAX — Measures & Calculated Columns](#-dax--measures--calculated-columns)
10. [Page 1 — Academic Performance](#-page-1--academic-performance)
11. [Page 2 — Behavioral Insights](#-page-2--behavioral-insights)
12. [Tech Stack](#-tech-stack)
13. [Results & Insights](#-results--insights)
14. [Advantages](#-advantages)
15. [How to Open & Use](#-how-to-open--use)
16. [Dashboard Overview](#-dashboard-overview)
17. [License](#-license)
18. [Author](#-author)
19. [Acknowledgements](#-acknowledgements)

---

## 🔭 Overview

**Student Performance Dashboard** is a two-page `.pbix` report built on four linked tables — **Students, Scores, Attendance and Behavior** — covering **1,000 students** in the *Academic Session 2024–25*.

- 📘 **Page 1 — Academic Performance:** scores by subject, term, gender and exam type, plus attendance and a student-wise scores table.
- 📙 **Page 2 — Behavioral Insights:** behaviour types, incidents by class, a behaviour trend and a detailed behaviour report.

A left navigation panel switches between the two pages, and each page has **four slicers** (Class and Section on both pages). All headline numbers come from **8 DAX measures** stored in a dedicated *Measure Table*.

<div align="center">

| 👩‍🎓 **1,000** | 📈 **49.87%** | 🗓️ **90.05%** | 🧾 **6,500** |
|:---:|:---:|:---:|:---:|
| Total Students | Avg % Score | Attendance | Behaviour Records |

</div>

---

## ❗ Problem Statement

School data usually lives in separate sheets — marks in one, attendance in another, discipline notes in a third. That makes it hard to answer the questions teachers and administrators ask every day:

- 📊 How are students performing overall, and how do subjects and terms compare?
- 🗓️ What is the attendance rate across the session?
- 🧑‍🎓 How does each student's average score and attendance look side by side?
- 🧾 Which behaviours are logged most often, and are they mostly positive or critical?
- 🏫 Do behaviour patterns differ by class or gender?

**Student Performance Dashboard** answers these in **one connected report**, with slicers to focus on any class, section, subject, term, gender or behaviour type.

---

## ✨ Features

| Feature | Page | Visual | Description |
|---|:---:|---|---|
| 👥 **Total Students** | 1 · 2 | Card | Distinct count of `StudentID` |
| 📈 **Avg % Score** | 1 | Card | Average of the `% Score` column |
| 🗓️ **Attendance %** | 1 | Card | Share of attendance records marked *Present* |
| 🏆 **High Performers** | 1 | Card | Students in the *High* performance category |
| 📊 **Avg Score by Subject** | 1 | Clustered Bar | Average score for each of the 5 subjects |
| 📉 **Avg Score by Term** | 1 | Line Chart | Average score for Term 1, 2 and 3 |
| 🍩 **Score by Subject** | 1 | Donut Chart | Share of total points per subject |
| 🧩 **Score by Gender & ExamType** | 1 | Treemap | Total points by gender and exam type |
| 📋 **Student-wise Scores Table** | 1 | Table | Name, class, section, average score, performance category and attendance % |
| 🧾 **Total Behaviour** | 2 | Card | Count of all logged behaviour records |
| 🌟 **Positive Incidents** | 2 | Card | *Participative* + *Helpful* records |
| 🚨 **Critical Incidents** | 2 | Card | *Disruptive* + *Absent without notice* records |
| 🍩 **Behavior Type Distribution** | 2 | Donut Chart | Count and share of each behaviour type |
| 🏫 **Behavior by Class** | 2 | Stacked Column | Behaviour records per class, split by type |
| 📈 **Behavior Trend** | 2 | Area Chart | Behaviour count by type |
| 🧩 **BehaviorType Treemap** | 2 | Treemap | Count of each behaviour type |
| 📋 **Student Behavior Report** | 2 | Table | Date, student, class, behaviour type and notes |
| 🎛️ **Slicers** | 1 · 2 | List / Dropdown | Class, Section, Subject, Term · Class, Section, Gender, BehaviorType |

---

## 🌟 Key Features

| Feature | Description |
|---|---|
| 🔗 **Star-Schema Model** | One `Students` dimension table linked to the `Scores`, `Attendance` and `Behavior` tables |
| 🧮 **8 DAX Measures** | Kept in a separate *Measure Table* for clean, reusable calculations |
| 🎛️ **8 Slicers, 2 Pages** | Class and Section on both pages; Subject and Term on Page 1; Gender and BehaviorType on Page 2 |
| 🧭 **Left Navigation Panel** | *Academic Performance* and *Behavioral Insights* buttons plus a back arrow, with 4 saved bookmarks |
| 💡 **Written Key Insights** | Each page ends with a *Key Insights* strip that explains the numbers in plain language |
| 🎨 **Conditional Formatting** | Colour scale on *Avg Score* and arrow icons on *Attendance %* in the student table |
| 🖼️ **Custom Branding** | EduTRACK logo, custom icons for every KPI card and a campus illustration on the side panel |
| 🖥️ **Fit-to-Page Canvas** | Both pages are designed at 1920 × 1080 with *Fit to page* |
| 🎨 **Themed Report** | Fluent 2 base theme plus a custom theme with a white page background |

---

## 📁 Project Structure

```
📦 Student-Performance-Dashboard/
 ┣ 📄 README.md                            ← Project documentation (you're here!)
 ┣ 📊 Student_Performance_Dashboard.pbix   ← Power BI report (2 pages, 1920 × 1080)
 ┣ 🖼️ Page_-1_Academic_Performance.png     ← Page 1 screenshot
 ┣ 🖼️ Page_2_-_Behavioral_Insights.png     ← Page 2 screenshot
 ┗ 📁 assets/
    ┗ 🎨 banner.svg                        ← README header banner
```

---

## 🖥️ Dashboard Layout

**📘 Page 1 — Academic_Information**

```
┌──────────────────────┬─────────────────────────────────────────────────────────────────────────────────┐
│       EduTRACK       │┌───────────────────────────────────────────────────────────────────────────────┐│
│                      ││                      STUDENT ACADEMIC PERFORMANCE DASHBOARD                   ││
│ Academic Performance ││                        [Class] [Section] [Subject] [Term]                     ││
│ Behavioral Insights  │└───────────────────────────────────────────────────────────────────────────────┘│
│                      │┌───────────────────┬───────────────────┬───────────────────┬───────────────────┐│
│                      ││ Total Students    │ Avg % Score       │ Attendance %      │ High Performers   ││
│                      │└───────────────────┴───────────────────┴───────────────────┴───────────────────┘│
│                      │┌─────────────────────────┬──────────────────────────┬──────────────────────────┐│
│                      ││ Avg Score by Subject    │ Avg Score by Term        │ Score by Subject         ││
│                      ││ (clustered bar)         │ (line chart)             │ (donut chart)            ││
│                      │└─────────────────────────┴──────────────────────────┴──────────────────────────┘│
│                      │┌──────────────────────────────┬────────────────────────────────────────────────┐│
│                      ││ Score by Gender and          │ Student-wise Scores Table                      ││
│                      ││ ExamType (treemap)           │ (7 columns)                                    ││
│                      │└──────────────────────────────┴────────────────────────────────────────────────┘│
│                      │┌───────────────────────────────────────────────────────────────────────────────┐│
│ <- back arrow        ││ Key Insights: attendance | mathematics | term trend                           ││
│                      │└───────────────────────────────────────────────────────────────────────────────┘│
└──────────────────────┴─────────────────────────────────────────────────────────────────────────────────┘
```

**📙 Page 2 — Behavior_Insights**

```
┌──────────────────────┬─────────────────────────────────────────────────────────────────────────────────┐
│       EduTRACK       │┌───────────────────────────────────────────────────────────────────────────────┐│
│                      ││                      STUDENT BEHAVIORAL INSIGHTS DASHBOARD                    ││
│ Academic Performance ││                    [Class] [Section] [Gender] [BehaviorType]                  ││
│ Behavioral Insights  │└───────────────────────────────────────────────────────────────────────────────┘│
│                      │┌───────────────────┬───────────────────┬───────────────────┬───────────────────┐│
│                      ││ Total Students    │ Total Behaviour   │ Positive Incidents│ Critical Incidents││
│                      │└───────────────────┴───────────────────┴───────────────────┴───────────────────┘│
│                      │┌─────────────────────────┬──────────────────────────┬──────────────────────────┐│
│                      ││ Behavior Type           │ Behavior by Class        │ Behavior Trend           ││
│                      ││ Distribution (donut)    │ (stacked column)         │ (area chart)             ││
│                      │└─────────────────────────┴──────────────────────────┴──────────────────────────┘│
│                      │┌──────────────────────────────┬────────────────────────────────────────────────┐│
│                      ││ BehaviorType counts          │ Student Behavior Report                        ││
│                      ││ (treemap)                    │ (5 columns)                                    ││
│                      │└──────────────────────────────┴────────────────────────────────────────────────┘│
│                      │┌───────────────────────────────────────────────────────────────────────────────┐│
│ <- back arrow        ││ Key Insights: disruptive | positive vs critical | gender                      ││
│                      │└───────────────────────────────────────────────────────────────────────────────┘│
└──────────────────────┴─────────────────────────────────────────────────────────────────────────────────┘
```

> Footer on both pages: *Academic Session 2024–25 | Confidential Student Records*.

---

## 🧪 Data Preparation (Power Query)

The report loads **four CSV files** from a local `Dataset` folder, plus one empty table that holds the measures:

| Query | Source file | Columns | Steps applied |
|---|---|:---:|---|
| 🧑‍🎓 **Students** | `Students - Students.csv.csv` | 5 | Promote headers → set types (`Class` as whole number, others as text) |
| 📝 **Scores** | `Scores - Scores.csv.csv` | 6 | Promote headers → set types (`Score` and `MaxScore` as whole numbers) |
| 🗓️ **Attendance** | `Attendance - Attendance.csv.csv` | 4 | Promote headers → set types (`Date` as date) → blank `Reason` values replaced with **"Due to Sick"** |
| 🧾 **Behavior** | `Behavior - Behavior.csv.csv` | 4 | Promote headers → set types (`Date` as date) |
| 🧮 **Measure Table** | — | 0 | Empty table (its only column is removed) used purely to organise DAX measures |

---

## 🔗 Data Model & Relationships

```
 ┌────────────┐                 ┌────────────┐                 ┌────────────┐
 │   Scores   │  many ───▶ one  │  Students  │  one ◀─── many  │ Attendance │
 │ (30,000)   │                 │  (1,000)   │                 │ (100,000)  │
 └────────────┘                 └─────┬──────┘                 └────────────┘
                                      ▲ one
                                      │
                                      │ many
                                ┌─────┴──────┐
                                │  Behavior  │
                                │  (6,500)   │
                                └────────────┘
```

| From (many) | To (one) | Join column | Cardinality | Cross-filter | Active |
|---|---|---|:---:|:---:|:---:|
| `Scores[StudentID]` | `Students[StudentID]` | StudentID | Many-to-one | Single | ✅ |
| `Attendance[StudentID]` | `Students[StudentID]` | StudentID | Many-to-one | Single | ✅ |
| `Behavior[StudentID]` | `Students[StudentID]` | StudentID | Many-to-one | Single | ✅ |

**📌 Dataset at a glance**

| Metric | Value |
|---|---|
| 🧑‍🎓 Students | **1,000** — Male 525 · Female 475 |
| 🏫 Classes · Sections | Classes **1–12** · Sections **A, B, C** (352 · 318 · 330 students) |
| 📚 Subjects · Exam types · Terms | 5 · 3 · 3 (Math, Science, English, History, Geography · Unit Test, Mid Term, Final Exam · Term 1–3) |
| 📝 Score records | **30,000** (30 per student, each out of 100) |
| 🗓️ Attendance records | **100,000** (100 per student) between **16 Jun 2024 and 16 Jun 2025** — 90,048 present · 9,952 absent |
| 🧾 Behaviour records | **6,500** across 5 behaviour types (6.5 per student) |
| 📦 Total records | **137,500** |

---

## 🧮 DAX — Measures & Calculated Columns

**📌 Measures** (all stored in `Measure Table`)

```dax
Total Students = DISTINCTCOUNT(Students[StudentID])

Attendance % = DIVIDE(
    CALCULATE(COUNTROWS(Attendance), Attendance[Status] = "Present"),
    COUNTROWS(Attendance),
    0
)

Avg % Score = AVERAGE(Scores[% Score])

Avg Score = AVERAGE(Scores[Score])

Behavior Count = COUNTROWS(Behavior)

High Performers = COALESCE(
    CALCULATE(
        [Total Students],
        Scores[Performance Category] = "High"
    ),
    0
)

Positive Incidents = CALCULATE(
    COUNTROWS(Behavior), 
    Behavior[BehaviorType] IN {"Participative", "Helpful"}
)

Critical Incidents = CALCULATE(
    COUNTROWS(Behavior), 
    Behavior[BehaviorType] IN {"Disruptive", "Absent without notice"}
)
```

| Measure | Used In |
|---|---|
| `Total Students` | Page 1 card · Page 2 card |
| `Avg % Score` | Page 1 card |
| `Attendance %` | Page 1 card · Student-wise Scores Table |
| `High Performers` | Page 1 card |
| `Avg Score` | Avg Score by Subject · Avg Score by Term · Student-wise Scores Table |
| `Behavior Count` | Behavior Trend (area chart) |
| `Positive Incidents` | Page 2 card |
| `Critical Incidents` | Page 2 card |

Some visuals use Power BI's implicit aggregations instead of measures: `Sum(Scores[Score])` (donut and treemap), `CountNonNull(Behavior[BehaviorType])` (Total Behaviour card, donut, stacked column and treemap) and `Sum(Students[Class])` (the *Sum of Class* column in both tables).

**📌 Calculated columns**

```dax
Scores[% Score] = DIVIDE(SUM(Scores[Score]), SUM(Scores[MaxScore]), 0)

Students[Student Avg %] = CALCULATE(AVERAGE(Scores[% Score]))

Scores[Performance Category] = SWITCH(
    TRUE(),
    Scores[% Score] >= 0.80, "High",
    Scores[% Score] >= 0.50, "Medium",
    "Low"
)
```

| Column | Table | Purpose |
|---|---|---|
| `% Score` | Scores | `SUM(Score) ÷ SUM(MaxScore)` — score as a share of the maximum possible marks; feeds the `Avg % Score` measure |
| `Performance Category` | Scores | Labels `% Score` as **High** (≥ 80%), **Medium** (≥ 50%) or **Low**; feeds the `High Performers` measure and the student table |
| `Student Avg %` | Students | `AVERAGE` of `% Score`, evaluated in each student's context |

---

## 📘 Page 1 — Academic Performance

> Title: **STUDENT ACADEMIC PERFORMANCE DASHBOARD** — *Track Performance, Identify Potential, Achieve Excellence*. Slicers: **Class · Section · Subject · Term**.

**💳 KPI Cards**

| Card | Measure | What it calculates | Shown on dashboard |
|---|---|---|---|
| 👥 Total Students | `Total Students` | Distinct students | **1,000** |
| 📈 Avg % Score | `Avg % Score` | Average of `% Score` across all score records | **49.87%** |
| 🗓️ Attendance % | `Attendance %` | Present records ÷ all attendance records (90,048 ÷ 100,000) | **90.05%** |
| 🏆 High Performers | `High Performers` | Students whose `Performance Category` is *High* | **1,000** |

**📊 Avg Score by Subject** — clustered bar · `Scores[Subject]` × `Avg Score`

| Subject | Avg Score | Shown on chart |
|---|---|:---:|
| 🥇 Math | 50.78 | 51 |
| 🥈 Science | 49.96 | 50 |
| 🥉 English | 49.82 | 50 |
| 4️⃣ History | 49.55 | 50 |
| 5️⃣ Geography | 49.24 | 49 |

> [!TIP]
> ✅ **Reading it:** **Math** leads with **50.78**, and **Geography** is lowest at **49.24** — a spread of just **1.54 points** across subjects.

**📉 Avg Score by Term** — line chart · `Scores[Term]` × `Avg Score`

| Term | Avg Score |
|---|---|
| Term 3 | 50.26 |
| Term 1 | 49.73 |
| Term 2 | 49.62 |

> [!TIP]
> ✅ **Reading it:** scores dip slightly from **Term 1 (49.73)** to **Term 2 (49.62)**, then rebound to peak in **Term 3 (50.26)**.

**🍩 Score by Subject** — donut · `Scores[Subject]` × `Sum of Score`

| Subject | Sum of Score | Shown on chart | Share |
|---|---|:---:|:---:|
| Math | 302,062 | 302K | 20.19% |
| Science | 301,771 | 302K | 20.17% |
| English | 301,714 | 302K | 20.17% |
| Geography | 298,444 | 298K | 19.95% |
| History | 292,032 | 292K | 19.52% |

**🧩 Score by Gender and ExamType** — treemap · `Students[Gender]` › `Scores[ExamType]` × `Sum of Score`

| Gender | Exam Type | Sum of Score |
|---|---|---|
| Female | Final Exam | 239,986 |
| Female | Mid Term | 234,881 |
| Female | Unit Test | 241,048 |
| Male | Final Exam | 257,822 |
| Male | Mid Term | 261,791 |
| Male | Unit Test | 260,495 |

| Gender | Students | Total points | Share of points | Avg score per record |
|---|:---:|---|:---:|:---:|
| Male | 525 | 780,108 | 52.15% | 49.53 |
| Female | 475 | 715,915 | 47.85% | 50.24 |

> [!NOTE]
> Male students hold the larger share of total points because there are more of them (525 vs 475); per score record, the averages are close — Female **50.24** vs Male **49.53**.

**📋 Student-wise Scores Table** — `StudentID`, `Name`, *Sum of Class*, `Section`, `Avg Score`, `Performance Category`, `Attendance %` (first rows shown):

| StudentID | Name | Class | Section | Avg Score | Attendance % |
|---|---|:---:|:---:|:---:|:---:|
| S0001 | Lara Simmons | 10 | A | 51.40 | 96.00% |
| S0002 | Brenda Peters | 4 | C | 52.70 | 93.00% |
| S0003 | Carlos Carlson | 1 | A | 41.83 | 90.00% |
| S0004 | Jeffrey Giles | 5 | B | 52.60 | 98.00% |
| S0005 | Stephen Medina | 9 | A | 49.40 | 89.00% |
| S0006 | Theodore Joseph | 4 | C | 57.87 | 86.00% |
| S0007 | Margaret Acosta | 10 | A | 59.37 | 85.00% |
| **Total** | | **6,328** | | **49.87** | **90.05%** |

**💡 Key Insights strip on the dashboard**

- 🗓️ **Attendance:** the student body maintains an average attendance rate of **90.05%** across all academic terms.
- ➕ **Mathematics** leads all disciplines with the highest average score (**50.78%**, rounded to **51%**) and accounts for the largest share of total points scored.
- 📉📈 **Term trend:** a slight dip between **Term 1 (49.73)** and **Term 2 (49.62)**, before rebounding strongly to peak in **Term 3 at 50.26**.

---

## 📙 Page 2 — Behavioral Insights

> Title: **STUDENT BEHAVIORAL INSIGHTS DASHBOARD** — Slicers: **Class · Section · Gender · BehaviorType**.

**💳 KPI Cards**

| Card | Source | What it calculates | Shown on dashboard |
|---|---|---|---|
| 👥 Total Students | `Total Students` | Distinct students | **1,000** |
| 🧾 Total Behaviour | `CountNonNull(Behavior[BehaviorType])` | All logged behaviour records | **6,500** |
| 🌟 Positive Incidents | `Positive Incidents` | *Participative* + *Helpful* | **2,593** |
| 🚨 Critical Incidents | `Critical Incidents` | *Disruptive* + *Absent without notice* | **2,605** |

**🍩 Behavior Type Distribution** — donut · `Behavior[BehaviorType]` × `Count`  (centre total: **6,500**)

| Behaviour Type | Records | Share | Visual |
|---|---|:---:|---|
| 🥇 Disruptive | 1,333 | 20.51% | 🟩🟩🟩🟩🟩🟩🟩 |
| 🥈 Late | 1,302 | 20.03% | 🟩🟩🟩🟩🟩🟩🟩 |
| 🥉 Helpful | 1,299 | 19.98% | 🟩🟩🟩🟩🟩🟩 |
| 4️⃣ Participative | 1,294 | 19.91% | 🟩🟩🟩🟩🟩🟩 |
| 5️⃣ Absent without notice | 1,272 | 19.57% | 🟩🟩🟩🟩🟩🟩 |

The same counts drive the **Behavior Trend** area chart (`Behavior Count` by type, ordered from highest to lowest) and the **BehaviorType treemap**.

> [!TIP]
> ✅ **Reading it:** **Disruptive** is the single largest category (**1,333 — 20.51%**), closely followed by **Late** (**1,302 — 20.03%**). All five types fall between **19.57% and 20.51%**.

**⚖️ Positive vs Critical**

| Group | Behaviour types | Records | Share |
|---|---|:---:|:---:|
| 🌟 Positive | Helpful + Participative | **2,593** | **39.89%** |
| 🚨 Critical | Disruptive + Absent without notice | **2,605** | **40.08%** |

> [!TIP]
> ✅ **Reading it:** positive and critical incidents nearly match — critical incidents lead by only **12** records.

**🏫 Behavior by Class** — stacked column · `Students[Class]` × `Count`, split by `BehaviorType`

| Class | Records | Share | Visual |
|---|:---:|:---:|---|
| Class 1 | 692 | 10.65% | 🟨🟨🟨🟨🟨🟨🟨 |
| Class 2 | 532 | 8.18% | 🟨🟨🟨🟨🟨 |
| Class 3 | 609 | 9.37% | 🟨🟨🟨🟨🟨🟨 |
| Class 4 | 577 | 8.88% | 🟨🟨🟨🟨🟨🟨 |
| Class 5 | 527 | 8.11% | 🟨🟨🟨🟨🟨 |
| Class 6 | 555 | 8.54% | 🟨🟨🟨🟨🟨🟨 |
| Class 7 | 428 | 6.58% | 🟨🟨🟨🟨 |
| Class 8 | 478 | 7.35% | 🟨🟨🟨🟨🟨 |
| Class 9 | 561 | 8.63% | 🟨🟨🟨🟨🟨🟨 |
| Class 10 | 596 | 9.17% | 🟨🟨🟨🟨🟨🟨 |
| Class 11 | 471 | 7.25% | 🟨🟨🟨🟨🟨 |
| Class 12 | 474 | 7.29% | 🟨🟨🟨🟨🟨 |

> [!TIP]
> ✅ **Reading it:** **Class 1 (692)** logs the most behaviour records and **Class 7 (428)** the fewest.

**🚻 Behaviour by Gender**

| Gender | Records | Share |
|---|:---:|:---:|
| Male | **3,473** | **53.4%** |
| Female | **3,027** | **46.6%** |

**📋 Student Behavior Report** — `Date`, `Name`, *Sum of Class*, `BehaviorType`, `Notes` (first entries for 16 June 2024, sorted by name):

| Date | Name | Class | BehaviorType | Notes |
|---|---|:---:|---|---|
| 16 June 2024 | Brenda Peters | 4 | Helpful | Become interview race soldier participant. |
| 16 June 2024 | Christopher Peterson | 9 | Helpful | Power car institution pattern charge. |
| 16 June 2024 | Daniel Petersen | 3 | Helpful | Clear adult impact perform see oil. |
| 16 June 2024 | Edward West | 10 | Late | Turn at call item data ball. |
| 16 June 2024 | Jaime Banks | 10 | Participative | Detail week move. |
| 16 June 2024 | Johnny Perez | 8 | Helpful | Indicate the analysis me. |

**💡 Key Insights strip on the dashboard**

- 🚨 **Disruptive behavior** is the single largest category recorded (**1,333 incidents, 20.51%**), followed closely by **Late** arrivals (**1,302, 20.03%**).
- ⚖️ Across the **6,500** logged behavioural events, positive incidents (**2,593**, or **39.89%** across *Helpful* and *Participative*) nearly match critical incidents.
- 🚻 **Male** students account for **53.4%** (**3,473**) of recorded incidents, while **Female** students account for **46.6%** (**3,027**).

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| 📊 **Power BI Desktop** | Report authoring, data modelling and visual design |
| 🧪 **Power Query (M)** | Loading and cleaning the four CSV sources |
| 🧮 **DAX** | 8 measures and 3 calculated columns |
| 🔗 **Data Model** | Star schema — one `Students` table linked to three fact tables |
| 🎨 **Native Visuals** | Card, Clustered Bar, Line, Donut, Treemap, Stacked Column, Area, Table, Slicer |
| 🎛️ **Bookmarks & Buttons** | Left navigation panel with page buttons and 4 saved bookmarks |
| 🖼️ **Themes & Branding** | Fluent 2 base theme, custom theme, EduTRACK logo and custom icons |

---

## 🏆 Results & Insights

| Area | Key Insight |
|---|---|
| 📈 **Overall Performance** | Average score is **49.87%**; **Math (50.78)** is the strongest subject and **Geography (49.24)** the lowest — only **1.54 points** apart |
| 📉 **Term Trend** | Dip from Term 1 (49.73) to Term 2 (49.62), then a rebound to **50.26** in Term 3 |
| 🗓️ **Attendance** | **90.05%** of attendance records are *Present* (90,048 of 100,000), with 9,952 absences across the session |
| 🧾 **Behaviour Mix** | Five behaviour types are almost evenly split (**19.57%–20.51%**); *Disruptive* is the largest at **1,333** |
| ⚖️ **Positive vs Critical** | **2,593** positive vs **2,605** critical incidents — a gap of only **12** |
| 🏫 **Class View** | **Class 1 (692)** has the most behaviour records; **Class 7 (428)** the fewest |
| 🚻 **Gender View** | Male **53.4%** · Female **46.6%** of recorded incidents |

---

## 💡 Advantages

- ⚡ **One Connected Report** — scores, attendance and behaviour all filter together through the shared `Students` table
- 🎯 **Two Focused Pages** — academic and behavioural views are separated but share the same Class and Section slicers
- 🧩 **Clean DAX Design** — all measures live in one `Measure Table`, easy to find and reuse
- 💬 **Insights in Plain Language** — every page has a written *Key Insights* strip next to the charts
- 🎨 **Polished, Branded Design** — green-and-gold EduTRACK theme with custom icons, logo and campus artwork
- 🧪 **Transparent Data Prep** — every cleaning step is documented in Power Query
- 🌱 **Easy to Extend** — new subjects, terms or behaviour types appear automatically once added to the source CSVs

---

## ▶️ How to Open & Use

1. 💻 Install **Power BI Desktop** (free, Windows).
2. 📂 Open `Student_Performance_Dashboard.pbix`. The data is stored inside the file, so the visuals load immediately.
3. 🧭 Use the **left navigation panel** to switch between *Academic Performance* and *Behavioral Insights*.
4. 🎛️ Use the slicers at the top — **Class, Section, Subject, Term** on Page 1 and **Class, Section, Gender, BehaviorType** on Page 2 — to filter every visual on the page.
5. 🔄 **To refresh from your own CSV files:** go to *Home → Transform data ▾ → Data source settings → Change Source…*, point each of the four queries (Students, Scores, Attendance, Behavior) to your `Dataset` folder, then click **Refresh**.

---

## 🖼️ Dashboard Overview

<div align="center">

### 📘 Page 1 — Academic Performance

<img src="Dashboard_Overview/Page 1 - Student_Academic_Performance.png" alt="Page 1 — Student Academic Performance Dashboard" width="900"/>

*KPI cards, subject and term charts, gender and exam-type treemap, and the student-wise scores table.*

<br/>

### 📙 Page 2 — Behavioral Insights

<img src="Dashboard_overview/Page 2 - Student_Behavioral_Insights.png" alt="Page 2 — Student Behavioral Insights Dashboard" width="900"/>

*Behaviour KPIs, type distribution, behaviour by class, behaviour trend and the student behaviour report.*

</div>

---

## 📄 License

```
MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
```

---

## 👩‍💻 Author

<div align="center">

| | |
|---|---|
| 👤 **Name** | _KRINA GHORI_ |
| 📊 **Tool** | Power BI Desktop |
| 📁 **Project** | Student Performance Dashboard (EduTRACK) |
| 💡 **Purpose** | Interactive academic performance & behavioural analytics dashboard |

<br/>

Made with 💚 using **Power BI**

![Power BI Love](https://img.shields.io/badge/Made%20with-%F0%9F%92%9A%20Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

</div>

---

## 🙏 Acknowledgements

- 📊 **Microsoft Power BI Team** — for the report engine and visualization framework behind this dashboard
- 📖 **Power BI & DAX Documentation** — for reference on Power Query, DAX measures and data modelling
- 💻 **Open Source Community** — for README badge tools (shields.io) and typing SVG animations
- 🎓 **All learners and educators** — who use data to track performance, identify potential and achieve excellence

---

<div align="center">

⭐ **Star this repo if you found it helpful!** ⭐

</div>
