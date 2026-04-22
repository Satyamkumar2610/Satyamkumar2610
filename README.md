<!--═══════════════════════════════════════════════════════════════════
  HERO
═══════════════════════════════════════════════════════════════════-->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,30:161b2e,60:1e2a45,100:0d1117&height=220&section=header&text=Satyam%20Kumar&fontSize=56&fontColor=e6edf3&animation=fadeIn&fontAlignY=38&desc=Research%20Engineer%20%C2%B7%20Geospatial%20Systems%20%C2%B7%20Applied%20AI&descAlignY=60&descColor=7d8ba1&descSize=15" width="100%"/>

<div align="center">

<a href="https://readme-typing-svg.demolab.com">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=15&pause=2000&color=58A6FF&center=true&vCenter=true&width=700&height=28&lines=Building+data-backed+systems+for+hard%2C+real-world+problems.;Where+rigorous+methodology+meets+production+software.;Geospatial+%C2%B7+Civic+Data+%C2%B7+Applied+Intelligence." alt="Typing SVG"/>
</a>

<br/><br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white&labelColor=0d1117)](https://linkedin.com/in/)&ensp;
[![GitHub](https://img.shields.io/badge/GitHub-e6edf3?style=flat-square&logo=github&logoColor=0d1117&labelColor=0d1117)](https://github.com/Satyamkumar2610)&ensp;
[![I‑ASCAP Live](https://img.shields.io/badge/I–ASCAP-Live-58A6FF?style=flat-square&logo=vercel&logoColor=white&labelColor=0d1117)](https://i-ascap.vercel.app)&ensp;
[![MausamTrekk Live](https://img.shields.io/badge/MausamTrekk-Live-7c3aed?style=flat-square&logo=vercel&logoColor=white&labelColor=0d1117)](https://mausam-trekk.vercel.app)

<br/>

```
CS Undergraduate · Rishihood University, Haryana
```

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,50:58A6FF,100:0d1117&height=1" width="100%"/>

<br/>

<!--═══════════════════════════════════════════════════════════════════
  SECTION 01 · VALUE PROPOSITION
═══════════════════════════════════════════════════════════════════-->

## `[ 01 ]` &ensp; What I Build — and Why It's Hard

> *The problems I gravitate toward share a common trait: they resist simple solutions.*

Most geospatial and data systems fail not because of bad code, but because of **bad assumptions** — about data stability, boundary permanence, or completeness. I build systems that are honest about this complexity.

Concretely, that means:

| Problem Class | What I engineer |
|---|---|
| Data that breaks over time | Harmonisation pipelines that preserve longitudinal validity |
| Geospatial systems at scale | `PostGIS`-backed APIs with topological integrity guarantees |
| Research → production gap | Full-stack systems that ship, not just notebooks |
| Disaster & civic risk | Verified-source spatial analytics with no synthetic fill |

<br/>

If you're building something where **correctness is non-negotiable** — research infrastructure, civic data platforms, geospatial intelligence — that's where I work best.

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,50:58A6FF,100:0d1117&height=1" width="100%"/>

<br/>

<!--═══════════════════════════════════════════════════════════════════
  SECTION 02 · FEATURED PROJECTS
═══════════════════════════════════════════════════════════════════-->

## `[ 02 ]` &ensp; Featured Work

<br/>

### ◈ &ensp; [I-ASCAP](https://github.com/Satyamkumar2610/I-ASCAP) &ensp;—&ensp; Indian Agri-Spatial Comparative Analytics Platform
###### `Live` [i-ascap.vercel.app](https://i-ascap.vercel.app) &ensp;·&ensp; `Stack` Next.js 14 · FastAPI · PostGIS · GeoPandas · Docker · Rasterstats

<br/>

**The Problem**

India has 800+ districts today. In 1966, it had far fewer. Every split, merger, and administrative renaming over six decades introduces a **topological discontinuity** that makes direct data comparison statistically invalid — yet most agricultural datasets ignore this entirely. Asking *"did yields improve in Telangana's carved-out districts after 2014?"* requires answering a harder prior question: *what do those districts' pre-2014 data even mean?*

**The Architecture**

```
OpenData CSVs + Shapefiles
        │
        ▼
DistrictHarmonizer  ←── topological lineage graph (splits, merges, renames)
        │                   areal interpolation + proportional apportioning
        ▼
PostGIS + GeoPandas ──→ FastAPI ──→ Next.js 14 App Router
        │
        ▼
Rasterstats (climate raster overlays) + Mapbox GL JS (dynamic time slider)
```

**The Engineering**

Built a custom `DistrictHarmonizer` class that models the complete ancestral lineage of every Indian district split — then apportions historical agricultural values proportionally to modern geometries. Each data point carries full **provenance metadata** (parent district, split year, apportioning method), making every visualised figure methodologically defensible rather than assumed.

**Impact**
- Valid 58-year time-series comparison across 800+ districts, with automatic boundary correction
- Lineage tracking: trace any district to its administrative ancestry (e.g. `Adilabad → Nirmal, Mancherial, Kumuram Bheem`)
- One-command deployment: `docker-compose up --build` spins the entire stack (DB + API + Frontend)

<br/>

---

<br/>

### ◈ &ensp; [Disaster Risk Mapping — India](https://github.com/Satyamkumar2610/Satyamcapstone)
###### `Stack` Python · GeoPandas · Folium · Pandas

<br/>

**The Problem**

Disaster response planning in India suffers from a data-availability mismatch: risk zone data exists at a coarse level, while deployment decisions (portable hospitals, logistics) require sub-district precision. Most available maps are static, unverified, and treat India as homogeneous.

**The Approach**

Designed an interactive geospatial visualisation pipeline that cross-references verified natural disaster risk indices with portable/mobile hospital deployment capacity — layered by district. Enforced a strict **no-synthetic-data constraint** throughout: every figure traces to a verifiable primary source. The result reads less like a dashboard and more like a planning instrument.

<br/>

---

<br/>

### ◈ &ensp; [MausamTrekk](https://github.com/Satyamkumar2610/MausamTrekk)
###### `Live` [mausam-trekk.vercel.app](https://mausam-trekk.vercel.app) &ensp;·&ensp; `Stack` Next.js · Firebase · JavaScript

Weather-aware trekking route intelligence. Real-time meteorological integration for route planning decisions — built as a clean, deployed product.

<br/>

---

<br/>

### ◈ &ensp; Sub-District Administrative Mapping Tool &ensp;`in progress`
###### `Stack` Leaflet.js · Python · GeoJSON · zero-cost stack

**The Gap:** India's tehsil/taluka boundary change data below district level is almost entirely absent from public datasets. This tool tracks sub-district administrative changes over time and overlays environmental and agricultural data layers — solving a known research gap in Indian civic data infrastructure.

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,50:58A6FF,100:0d1117&height=1" width="100%"/>

<br/>

<!--═══════════════════════════════════════════════════════════════════
  SECTION 03 · SYSTEMS THINKING
═══════════════════════════════════════════════════════════════════-->

## `[ 03 ]` &ensp; How I Think About Systems

The projects above aren't independent — they reflect a consistent methodology:

```
  [ identify the assumption that breaks the data ]
           ↓
  [ model the real-world complexity formally ]
           ↓
  [ build the system that handles it correctly ]
           ↓
  [ ship it as a working, documented product ]
```

This means I spend significant time **before writing code** — mapping data lineages, questioning source validity, stress-testing edge cases that standard tutorials don't cover. Formal coursework in Set Theory and Group Theory sharpens this: reasoning about sets of administrative units, boundary transformations, and group-like operations on spatial data isn't just academic — it directly informs how I model these systems.

The measurable output: systems that don't silently produce wrong answers.

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,50:58A6FF,100:0d1117&height=1" width="100%"/>

<br/>

<!--═══════════════════════════════════════════════════════════════════
  SECTION 04 · TECH STACK
═══════════════════════════════════════════════════════════════════-->

## `[ 04 ]` &ensp; Technical Capabilities

<div align="center">

**Geospatial & Data Engineering**

![Python](https://img.shields.io/badge/Python-1e2a3a?style=flat-square&logo=python&logoColor=4B9CD3)
![GeoPandas](https://img.shields.io/badge/GeoPandas-1e2a3a?style=flat-square&logo=pandas&logoColor=139C5A)
![PostGIS](https://img.shields.io/badge/PostGIS-1e2a3a?style=flat-square&logo=postgresql&logoColor=336791)
![Rasterstats](https://img.shields.io/badge/Rasterstats-1e2a3a?style=flat-square&logo=satellite&logoColor=58A6FF)
![Pandas](https://img.shields.io/badge/Pandas-1e2a3a?style=flat-square&logo=pandas&logoColor=6272a4)
![NumPy](https://img.shields.io/badge/NumPy-1e2a3a?style=flat-square&logo=numpy&logoColor=4DABF7)
![Plotly](https://img.shields.io/badge/Plotly-1e2a3a?style=flat-square&logo=plotly&logoColor=7c3aed)
![Mapbox GL](https://img.shields.io/badge/Mapbox%20GL-1e2a3a?style=flat-square&logo=mapbox&logoColor=58A6FF)

**Backend & Infrastructure**

![FastAPI](https://img.shields.io/badge/FastAPI-1e2a3a?style=flat-square&logo=fastapi&logoColor=009688)
![Node.js](https://img.shields.io/badge/Node.js-1e2a3a?style=flat-square&logo=node.js&logoColor=339933)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1e2a3a?style=flat-square&logo=postgresql&logoColor=336791)
![MongoDB](https://img.shields.io/badge/MongoDB-1e2a3a?style=flat-square&logo=mongodb&logoColor=47A248)
![Docker](https://img.shields.io/badge/Docker-1e2a3a?style=flat-square&logo=docker&logoColor=2496ED)
![Firebase](https://img.shields.io/badge/Firebase-1e2a3a?style=flat-square&logo=firebase&logoColor=FFCA28)

**Frontend & Interfaces**

![Next.js](https://img.shields.io/badge/Next.js-1e2a3a?style=flat-square&logo=next.js&logoColor=e6edf3)
![React](https://img.shields.io/badge/React-1e2a3a?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-1e2a3a?style=flat-square&logo=typescript&logoColor=007ACC)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-1e2a3a?style=flat-square&logo=tailwind-css&logoColor=38B2AC)

**Applied Intelligence**

![scikit-learn](https://img.shields.io/badge/scikit--learn-1e2a3a?style=flat-square&logo=scikit-learn&logoColor=F7931E)
![LangChain](https://img.shields.io/badge/LangChain-1e2a3a?style=flat-square&logo=langchain&logoColor=1C9E6E)
![Jupyter](https://img.shields.io/badge/Jupyter-1e2a3a?style=flat-square&logo=jupyter&logoColor=FA0F00)

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,50:58A6FF,100:0d1117&height=1" width="100%"/>

<br/>

<!--═══════════════════════════════════════════════════════════════════
  SECTION 05 · PROOF OF WORK
═══════════════════════════════════════════════════════════════════-->

## `[ 05 ]` &ensp; Proof of Work

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Satyamkumar2610&show_icons=true&theme=github_dark&hide_border=true&border_radius=6&count_private=true&rank_icon=github&title_color=58A6FF&icon_color=7c3aed&text_color=8b949e&bg_color=0d1117" height="160"/>
&ensp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Satyamkumar2610&theme=github_dark&hide_border=true&layout=compact&border_radius=6&langs_count=6&hide=html,css&title_color=58A6FF&text_color=8b949e&bg_color=0d1117" height="160"/>

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Satyamkumar2610&bg_color=0d1117&color=8b949e&line=58A6FF&point=7c3aed&area=true&area_color=1e2a45&hide_border=true&radius=6" width="92%"/>

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,50:58A6FF,100:0d1117&height=1" width="100%"/>

<br/>

<!--═══════════════════════════════════════════════════════════════════
  SECTION 06 · CURRENT FOCUS
═══════════════════════════════════════════════════════════════════-->

## `[ 06 ]` &ensp; Current Focus

```python
ACTIVE = {
    "I-ASCAP v2"       : "Adding climate raster overlays — rainfall/temp correlation with yield trends",
    "Sub-District Tool" : "Filling India's tehsil-level boundary-change data gap",
    "Coursework"        : ["Set Theory", "Group Theory", "LLM Architecture", "Responsible AI"],
    "Exploring"         : "Formal verification approaches for spatial data pipelines",
}
```

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,50:58A6FF,100:0d1117&height=1" width="100%"/>

<br/>

<!--═══════════════════════════════════════════════════════════════════
  SECTION 07 · CALL TO ACTION
═══════════════════════════════════════════════════════════════════-->

## `[ 07 ]` &ensp; Let's Work Together

I'm selectively open to:

- **Research Collaboration** — geospatial systems, civic data infrastructure, agricultural analytics
- **Consulting / Contract** — data pipelines, spatial backend engineering, research-to-product builds
- **Interesting Problems** — if it involves data that breaks over time, complex spatial relationships, or systems where correctness matters more than speed

> *I don't take on every project — but if the problem is non-trivial and the work is serious, let's talk.*

<br/>

<div align="center">

[![Email](https://img.shields.io/badge/Reach%20Out-0d1117?style=for-the-badge&logo=gmail&logoColor=58A6FF&label=&labelColor=1e2a45)](mailto:your@email.com)&ensp;
[![LinkedIn](https://img.shields.io/badge/Connect-0d1117?style=for-the-badge&logo=linkedin&logoColor=58A6FF&label=&labelColor=1e2a45)](https://linkedin.com/in/)

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,40:1e2a45,70:161b2e,100:0d1117&height=130&section=footer&fontColor=8b949e&fontSize=11&text=Systems%20that%20don't%20silently%20produce%20wrong%20answers.&fontAlignY=65&animation=fadeIn" width="100%"/>
