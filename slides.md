---
colorSchema: light
favicon: /public/images/diracx-logo-square.png
color: orange-light
layout: cover
routerMode: hash
title: DIRAC, but mostly DiracX, for Workflow Management
theme: neversink
neversink_string: "DIRAC+X"
---

# DIRAC, but mostly DiracX, for Workflow Management

**Federico Stagni** <Email v="federico.stagni@cern.ch" />

4 November 2025
\_\_ <a href="https://indico.fnal.gov/event/73933" class="ns-c-iconlink"><mdi-open-in-new />Scientific Workflow Management Cross-Experiment Retreat at the LPC</a>

---
layout: section
color: cyan-light
title: Intro
---

# Intro

---
layout: top-title
color: gray-light
align: c
title: core-functionalities
clicks: 4
---

:: title ::

# Core functionalities and tools

:: content ::

<v-switch>
<template #0>

Core functionalities:

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart TD
    WMS["`**WMS**
    Workload Management System`"]
    DMS["`**DMS**
    Data Management`"]
    PROD["`**Production Management**
    Workflow Orchestration`"]
    IS["`**Information System**
    Resources & Status`"]

    style WMS fill:#bbf,stroke:#88c
    style DMS fill:#bfb,stroke:#8c8,stroke-width:2px
    style PROD fill:#eef,stroke:#8ec
    style IS fill:#fff,stroke:#000
```

Tools:

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart TD

    DIRAC(["`**DIRAC / DiracX**`"])
    RUCIO(["`**Rucio**`"])
    GLIDE(["`**GlideInWMS+HTCondor**`"])
    CRIC(["`**CRIC**`"])
    PANDA(["`**Panda**`"])
    HARVESTER(["`**Harvester**`"])
    WM(["`**WMAgent**`"])

    style DIRAC fill:#f90,color:#000,stroke:#c60,stroke-width:3px
    style RUCIO fill:#4a9,color:#fff,stroke:#276,stroke-width:3px
    style GLIDE fill:#56b,color:#fff,stroke:#235,stroke-width:3px
    style CRIC fill:#19b,color:#000,stroke:#239,stroke-width:3px
    style PANDA fill:#001,color:#ff0,stroke:#eee,stroke-width:3px
    style WM fill:#ee1,color:#003,stroke:#eee,stroke-width:3px
    style HARVESTER fill:#cc7,color:#004,stroke:#aaa,stroke-width:3px
```

</template>
<template #1>

**LHCb**

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart TD
    WMS["`**WMS**
    Workload Management System`"]
    DMS["`**DMS**
    Data Management`"]
    PROD["`**Production Management**
    Workflow Orchestration`"]
    IS["`**Information System**
    Resources & Status`"]

    style WMS fill:#bbf,stroke:#88c
    style DMS fill:#bfb,stroke:#8c8,stroke-width:2px
    style PROD fill:#eef,stroke:#8ec
    style IS fill:#fff,stroke:#000

    DIRAC(["`**DIRAC / DiracX**`"])

    style DIRAC fill:#f90,color:#000,stroke:#c60,stroke-width:3px

    WMS -->|implemented by| DIRAC
    DMS -->|implemented by| DIRAC
    PROD -->|implemented by| DIRAC
    IS -->|implemented by| DIRAC
```

</template>
<template #2>

**Belle2**, and **CTAO**

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart TD
    WMS["`**WMS**
    Workload Management System`"]
    DMS["`**DMS**
    Data Management`"]
    PROD["`**Production Management**
    Workflow Orchestration`"]
    IS["`**Information System**
    Resources & Status`"]

    style WMS fill:#bbf,stroke:#88c
    style DMS fill:#bfb,stroke:#8c8,stroke-width:2px
    style PROD fill:#eef,stroke:#8ec
    style IS fill:#fff,stroke:#000

    DIRAC(["`**DIRAC / DiracX**`"])
    RUCIO(["`**Rucio**`"])

    style DIRAC fill:#f90,color:#000,stroke:#c60,stroke-width:3px
    style RUCIO fill:#4a9,color:#fff,stroke:#276,stroke-width:3px

    WMS -->|implemented by| DIRAC
    DMS -->|implemented by| RUCIO
    PROD -->|implemented by| DIRAC
    IS -->|implemented by| DIRAC
```

</template>
<template #3>

**ATLAS**

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart TD
    WMS["`**WMS**
    Workload Management System`"]
    DMS["`**DMS**
    Data Management`"]
    PROD["`**Production Management**
    Workflow Orchestration`"]
    IS["`**Information System**
    Resources & Status`"]

    style WMS fill:#bbf,stroke:#88c
    style DMS fill:#bfb,stroke:#8c8,stroke-width:2px
    style PROD fill:#eef,stroke:#8ec
    style IS fill:#fff,stroke:#000

    RUCIO(["`**Rucio**`"])
    CRIC(["`**CRIC**`"])
    PANDA(["`**Panda**`"])
    HARVESTER(["`**Harvester**`"])

    style RUCIO fill:#4a9,color:#fff,stroke:#276,stroke-width:3px
    style CRIC fill:#19b,color:#000,stroke:#239,stroke-width:3px
    style PANDA fill:#001,color:#ff0,stroke:#eee,stroke-width:3px
    style HARVESTER fill:#cc7,color:#004,stroke:#aaa,stroke-width:3px
    
    WMS -->|implemented by| HARVESTER
    DMS -->|implemented by| RUCIO
    PROD -->|implemented by| PANDA
    IS -->|implemented by| CRIC
```

</template>
<template #4>

**CMS**

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart TD
    WMS["`**WMS**
    Workload Management System`"]
    DMS["`**DMS**
    Data Management`"]
    PROD["`**Production Management**
    Workflow Orchestration`"]
    IS["`**Information System**
    Resources & Status`"]

    style WMS fill:#bbf,stroke:#88c
    style DMS fill:#bfb,stroke:#8c8,stroke-width:2px
    style PROD fill:#eef,stroke:#8ec
    style IS fill:#fff,stroke:#000

    DIRAC(["`**DIRAC / DiracX**`"])
    RUCIO(["`**Rucio**`"])
    GLIDE(["`**GlideInWMS+HTCondor**`"])
    CRIC(["`**CRIC**`"])
    WM(["`**WMAgent**`"])

    style DIRAC fill:#f90,color:#000,stroke:#c60,stroke-width:3px
    style RUCIO fill:#4a9,color:#fff,stroke:#276,stroke-width:3px
    style GLIDE fill:#56b,color:#fff,stroke:#235,stroke-width:3px
    style CRIC fill:#19b,color:#000,stroke:#239,stroke-width:3px
    style WM fill:#ee1,color:#003,stroke:#eee,stroke-width:3px

    WMS -->|implemented by| GLIDE
    DMS -->|implemented by| RUCIO
    PROD -->|implemented by| WM -->|replaced by| DIRAC
    IS -->|implemented by| CRIC
```

</template>
</v-switch>


---
layout: top-title
color: gray-light
align: c
title: who
---

:: title ::

# Who am I? why am I here?

:: content ::

- Dirac technical coordinator
  - the project that develops/maintains DIRAC, DiracX, Web, etc... (everything in https://github.com/DIRACGrid)
- CERN employee since 2019. Also part of LHCb.

I am here because CMS reviewed Dirac and has serious interests in using it as Workflow Management of choice for Run4.


---
layout: top-title-two-cols
color: gray-light
align: c-lm-lm
title: disambiguation
columns: is-4
---

:: title ::

# DIRAC and DiracX

:: left ::

<img id="DIRAC" src="/public/images/DIRAC-logo-extended.png" class="mx-auto w-2/5"> </img>

- An "interware" (a tool for doing distributed computing)
- Started by LHCb, today is used **in production** by few dozens communities
- It can be used for managing jobs (via pilots), data, productions, dataset transfers, etc

:: right ::

<img id="DIRAC" src="/public/images/diracx-logo-full-transparent-background.png" class="mx-auto w-2/5"> </img>

- "The neXt DIRAC incarnation", a complete rewrite aiming at fully replacing DIRAC. A cloud native app, multi-VO from the get-go, standards-based
  - Younger, faster, better, stronger.
- Used **in production** by LHCb, with few others getting there.
- Right now it can do few things, with the bulk of the operations still done by DIRAC.

<AdmonitionType type='important' >
Still DIRAC, in terms of functionalities.
</AdmonitionType>

---
layout: top-title
color: gray-light
align: cm
title: question
clicks: 1
---

:: title ::

# The question, for this WS

:: content ::


<v-switch>
<template #0>

<span class="bg-red-200 text-cyan-800 p-10 border-l-6 border-2 border-black-800 rounded-lg pl-16 pr-16 w-2/3 block mr-auto mt-20">
DiracX Workflow Management: what, and how?
</span>

</template>
<template #1>

<span class="bg-red-200 text-cyan-800 p-10 border-l-6 border-2 border-black-800 rounded-lg pl-16 pr-16 w-2/3 block mr-auto mt-20">
DiracX Workflow Management: what, and how?
</span>

<span class="bg-red-200 text-cyan-800 p-10 border-l-6 border-2 border-black-800 rounded-lg pl-16 pr-16 w-1/3 block ml-auto mb-40">
and when?
</span>

</template>
</v-switch>


---
layout: section
color: cyan-light
title: Dirac(X) and Workflows
---

# Dirac(X) and Workflows

---
layout: side-title
color: gray-light
align: lm-lm  
title: TS
---

:: title ::

## Transformation System
### For productions and Dataset management

- A *Data Processing* **transformation** (e.g. Simulation, Merge, DataReconstruction...) creates jobs in the WMS (and re-submits them if needed, eventually destroys them).​

- A *Data Manipulation* **transformation** replicates, or removes, data from storage elements.

:: content ::

<span class="bg-cyan-100 text-cyan-600 p-4 border-l-6 border-2 border-cyan-400 rounded-lg pl-8 pr-8 w-full block">
The Transformation System is used to automate common tasks related to production activities. It can handle thousands of productions, millions of files and jobs.
</span>

&nbsp;
&nbsp;

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart LR;
TS[("`**Transformation
System**`")]
style TS fill:#bbf
WMS[("`**Workload
Management
System**`")]
style WMS fill:#bba
RMS[("`**Request
Management
System**`")]
style RMS fill:#bba
DMS[("`**Data
Management
System**`")]
style DMS fill:#bba
PM@{ shape: sl-rect, label: "Productions Management" }
DM@{ shape: sl-rect, label: "DataSets Management" }

PM-->|Productions Definitions|TS
DM-->|DataSets Operations|TS
TS-->|Jobs|WMS
TS-->|Data Operations|RMS
RMS-->DMS
```



---
layout: section
color: lime-light
---

<div style="display: flex; align-items: center; justify-content: center;">
    <img id="DIRAC" src="/public/images/DIRAC-logo-extended.png" alt="DIRAC logo" style="width: 300px;">
    <span style="margin: 0 50px;">--></span>
    <img id="DiracX" src="https://raw.githubusercontent.com/DIRACGrid/management/master/branding/diracx/svg/diracx-logo-full.svg" alt="DiracX" style="width: 300px;">
</div>


---
layout: top-title
color: gray-light
align: c
title: points
---

:: title ::

# Notable points

:: content ::

<AdmonitionType type='note' >
There are several communities using DIRAC right now. Their business continuity is our top priority.
</AdmonitionType>

<AdmonitionType type='important' >
DIRAC and DiracX will live together for a while
</AdmonitionType>

<AdmonitionType type='info' >
One functionality at a time, we'll eventually migrate all from DIRAC to DiracX.
</AdmonitionType>


---
layout: top-title
color: gray-light
align: c
title: DiracX v0.0.1
---

:: title ::

# The first DiracX releases

:: content ::

### It contains:

- All service/client underpinnings.
- Extension support.
- Jobs sandboxes can be stored in an object store.
- The DIRAC `WorkloadManagement/JobStateUpdateHandler` service can be replaced by an "equivalent" DiracX service.
- The helm chart is considered "stable enough".
- Documentation "sufficiently complete".
- DiracX extensions working.

We will keep working, within the patches of this first version, on adding new services and documentation.


---
layout: top-title-two-cols
color: gray-light
align: c-lm-lm
title: Timeline
columns: is-7
---

:: title ::

# Timeline of the next year

:: left ::

```mermaid {scale:0.5}
%%{init: { 'logLevel': 'debug', 'theme': 'base', 'timeline': {'disableMulticolor': true}}}%%
    timeline
        section DIRAC and DiracX coexisting (forcefully)
            2 weeks ago : Release of DIRAC v9.0 and DiracX 0.0.1
                        : JobStateUpdate service migrated and tested
                        : Possible adoption by non-LHCb DIRAC users
            Q1 2026 : Release DiracX 0.1.0
                    : DiracX introduces a task management system
            Q3 2026 : Release DIRAC v9.1 and 0.1.X (or 0.2.0)
                    : First DiracX-only service.
                    : Adoption of new Pilot security mechanism
                    : First DiracX replacements for DIRAC agents or executors using DiracX tasks
```

:: right ::

- DiracX 0.1.0 will bring "tasks", for replacing DIRAC's _agents_, _executors_, and the RMS machinery (the _RequestExecutingAgent_)
- We will need a DIRAC v9.1 because there will be database changes (some PRs already in _draft_)
- Standalone DiracX will take at least 2 years from now


---
layout: top-title
color: gray-light
align: c
title: Users-WhatsNew
---

:: title ::

# What's new for users

:: content ::

<ul class="text-sm">
  <li><strong>Logging-in</strong> requires that you are previously registered in an IdP implementing OpenID Connect protocol
    <ul>
      <li>essentially this is the VOMS-&gt;IaM migration. Admins should have done this already, transparently, for all the users of a VO</li>
      <li>if a VO is not migrated to IaM, it can't be "enabled" (see later on)</li>
    </ul>
  </li>
  <li>New <strong>Web app</strong> (which, for DiracX 0.0.1 is not of much use)</li>
  <li>Enriched and modern <strong>CLI</strong> (but not many functionalities in there)</li>
  <li><strong>REST</strong> interface for programmatic usage (for advanced users -- but again, not much user-facing info to use)</li>
</ul>

<p>But effectively, for now <strong>users can largely be agnostic</strong> of DiracX, as for the first version users' interactions will still be done via the DIRAC tools they know (and love?).</p>

<p>Also, users should be setting the correct environment variables (<code>DIRACX_URL</code> mostly)</p>

<ul class="text-sm">
  <li>admins should be setting it already for the users</li>
</ul>

---
layout: side-title
side: left
color: gray-light
titlewidth: is-4
align: rm-lm
title: WebAPI
---

:: title ::

# DiracX APIs

:: content ::

DIRAC Web APIs with <devicon-fastapi-wordmark class="text-7xl align-middle inline-block mx-0"></devicon-fastapi-wordmark>

Nicely documented by <devicon-swagger-wordmark class="text-7xl align-middle inline-block mx-0"></devicon-swagger-wordmark>

Follows the <devicon-plain-openapi-wordmark class="text-7xl align-middle inline-block mx-1"></devicon-plain-openapi-wordmark> specification, with the (python) client generated by [AutoREST](https://github.com/Azure/autorest/blob/main/docs/introduction.md)
- clients in another language are just one pipeline away.

<!--
- there is also redoc
- AutoREST supports several langagues, not only python
-->

---
layout: side-title
side: right
color: gray-light
titlewidth: is-4
align: lm-lm
title: DiracX-Web
---

:: title ::

# DiracX web

![diracx-web](/public/images/diracx-web-structure.png)

![diracx-login](/public/images/diracx-auth.png)


:: content ::

### We are also rewriting [the Web App](https://github.com/DIRACGrid/diracx-web) from scratch.

Software stack:

- NextJS <devicon-nextjs-wordmark class="text-4xl align-middle inline-block mx-2" />
- Material UI <devicon-materialui class="text-3xl align-middle inline-block mx-2" />
- TypeScript <devicon-typescript class="text-3xl align-middle inline-block mx-2" />

(very similary to Rucio Web UI stack)

- There is no tight coupling between API and frontend: the web app acts as any other diracx client using the same set of endpoints.
- As per DiracX, DiracX-Web is extendable.


---
layout: top-title
color: gray-light
align: c 
title: DiracXWMS
---

:: title ::

# WMS evolution in DiracX

:: content ::

There are several features that will be added in the next year in DiracX (few already in DIRAC), evolving its WMS functionalities. Few examples:
- Perfecting the **Pilot push model** for closed HPCs (in parallel to the default pull model)
- A new an improved security model for pilots, using tokens
- Enforcing of CGroup2 limits for full node allocations



---
layout: top-title
color: gray-light
align: c
title: FutureExtensions
---

:: title ::

# DiracX extensions

:: content ::

<span class="bg-cyan-100 text-cyan-600 text-center p-4 border-l-6 border-2 border-cyan-400 rounded-lg pl-8 pr-8 w-full block">
    By now, we know that it is sometimes necessary to extend all Dirac(X) components 
    
    DiracX aims to provide an easy way to do so.
</span>


```toml
# entrypoints in pyproject.toml

[project.entry-points."diracx.db.sql"]
AuthDB = "diracx.db.sql:AuthDB"
JobDB = "<extension>.db.sql:ExtendedJobDB"
```

<SpeechBubble position="t" color='amber' shape="round"  v-drag="[400,310,220,140]">
For DiracX and DiracX-Web we already provide reference extensions
</SpeechBubble>


---
layout: top-title
color: gray-light
align: cm 
title: DiracXWMS
---

:: title ::

# WMS evolution in DiracX: CWL

:: content ::

<div class="flex justify-center gap-4">
  <img src="/public/images/CWL1.png" class="w-1/2 object-contain" />
  <img src="/public/images/CWL2.png" class="w-1/4 object-contain" />
  <img src="/public/images/CWL3.png" class="w-1/4 object-contain" />
</div>



---
layout: top-title-two-cols
align: cm-cm-lm
color: orange-light
columns: is-4
title: summary
--- 
:: title ::

# Summary

:: left :: 

<img id="DiracX" src="https://raw.githubusercontent.com/DIRACGrid/management/master/branding/diracx/svg/diracx-logo-square.svg" class="mx-auto w-4/5"> </img>

:: right ::

<ul class="text-base">
  <li>DiracX is "the neXt Dirac incarnation", ensuring the future of the widely used DIRAC. The first DiracX release is here.
    <ul class="text-sm">
      <li>It will live together with DIRAC v9 for a while, until it will replace it completely</li>
      <li>DiracX will still have the Data Management part, but its Workload Management functionalities will come first</li>
    </ul>
  </li>
</ul>

In general, DIRAC has a very active community of users and developers.
- Apart from the regular zoom meetings, we meet for hackathons 3 times per year, plus once in a workshop. Next will be [13-16 Oct 2026 in Prague](https://indico.cern.ch/event/1588323/).
- For the latest presentations, check [our latest WS](https://indico.cern.ch/event/1433941/)



---
layout: credits
color: navy
loop: true
speed: 1.0
title: credits/people
---

<div class="grid text-size-4 grid-cols-3 w-3/4 gap-y-10 auto-rows-min ml-auto mr-auto">
    <div class="grid-item text-center mr-0- col-span-3">
        <strong>People</strong><br>
    </div>
    <div class="grid-item text-right mr-4 col-span-1">
        <strong>Current Developers, maintainers, supporters</strong>
    </div>
    <div class="grid-item col-span-2">
        Chris Burr <i>CERN, LHCb</i><br/>
        Christophe Haen <i>CERN, LHCb</i><br/>
        Alexandre Boyer <i>CERN, LHCb</i><br/>
        Natthan Piggoux <i>LUPM (FR), CTA</i><br/>
        Cedric Serfon <i>Brookhaven National Laboratory (US), Belle2</i><br/>
        Ryunosuke O'Neil <i>CERN, LHCb</i><br/>
        Daniela Bauer <i>Imperial college (UK), GridPP</i><br/>
        Simon Fayer <i>Imperial college (UK), GridPP</i><br/>
        Janusz Martyniak <i>Imperial college (UK), GridPP</i><br/>
        Xiaomei Zhang <i>Beijing, Inst. High Energy Phys. (CN), Juno</i><br/>
        Luisa Arrabito <i>LUPM (FR), CTA</i><br/>
        André Sailer <i>CERN</i><br/>
        Jorge Lisa Laborda <i>Univ. of Valencia and CSIC (ES), LHCb</i><br/>
        Bertrand Rigaud <i>IN2P3 (FR)</i>
    </div>
    <div class="grid-item text-right mr-4 col-span-1">
        <strong>Project lead</strong>
    </div>
    <div class="grid-item col-span-2">
        Federico Stagni <i>CERN, LHCb</i><br/>
        Andrei Tsaregorotsev <i>CPPM (FR), EGI and LHCb</i>
    </div>
</div>

&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;

<div class="grid-item col-span-3 text-center mt-180px mb-auto font-size-1.5rem">
    <strong>Questions?</strong>
</div>

---
layout: section
color: cyan-light
title: Backup
---

# Backup


---
layout: top-title-two-cols
color: gray-light
align: c-lm-lm
title: dirac
columns: is-5
---

:: title ::

# DiracX and heterogeneous slots

:: left ::

- Nowadays *Dirac(X) can take a node consisting of several CPUs and partition it*. CPUs only.
- The **match-making** process (the process of matching job needs to job slots capabilities) can use a very simple system for tagging slots including GPUs. This is not fully applicable for heterogeneous nodes.

:: right ::

Would not be able to fully exploit nodes like this:

<div class7="relative">
  <img src="/public/images/lumig-overview.svg" class="w-full" />

  <div class="absolute bottom-0 right-0 text-xs text-gray-500">
    Source: https://docs.lumi-supercomputer.eu/hardware/lumig/
  </div>
</div>

---
layout: top-title-two-cols
color: gray-light
align: c-lm-lm
title: diracx
columns: is-5
---

:: title ::

# DiracX and heterogeneous slots (cont)

:: left :: 

In the context of DiracX, LHCb is working on:

- Using CWL for jobs and workflow description

![](/public/images/CWL1.png)

:: right ::

![](/public/images/diracx-logo-full-transparent-background.png)

- A realistic **slot description for heterogeneous architectures**
- An advanced jobs match-making
- "Solving" the general case of **whole node scheduling**: whole-node scheduling and benchmarking seem to be the best way forward.


---
layout: side-title
align: lm-lm
color: gray-light
title: WMS
titlewidth: is-3
---

:: title ::

## Workload Management System
- Pull model based on Pilot jobs
- Also "Push" solution for HPCs that do not support pilots (because of limited internet access).
- Will integrate [CWL (Common Workflow Language)](https://www.commonwl.org) as a way of defining jobs (replacing JDL)

:: content ::

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart LR;
Jobs["`Users see only **Jobs**`"]
A@{ shape: sl-rect, label: "APIs" }
WMS[("`**Workload
Management
System**`")]
style WMS fill:#bbf
HPC["`High
Perfomance
Computers`"]
style HPC fill:#A145
clusters["`Computer clusters`"]
style clusters fill:#A145
Grid_Nodes["Grid"]
Pilots["`**Pilots**
administer computing slots, and match (pull) jobs`"]

style HTCondorCE fill:#F23A
style ARC-AREX fill:#F23A
style libcloud fill:#F23A
style SSH fill:#F23A
style Grid_Nodes fill:#A145
style Iaas:Clouds fill:#A145
style HTCondor fill:#F26
style SLURM fill:#F26
style Jobs fill:#FFF
style Pilots fill:#FFF

A-->|jobs|WMS

WMS-->|pilots|libcloud
WMS-->|pilots|HTCondorCE
WMS-->|pilots|ARC-AREX
WMS-. jobs .->HPC
WMS-->|pilots|SSH

libcloud-->|VMs starting pilots|Iaas:Clouds
HTCondorCE-->Grid_Nodes
ARC-AREX-->Grid_Nodes
ARC-AREX-->HPC
SSH-->|pilots|SLURM
SSH-->|pilots|HTCondor
SSH-->|pilots|clusters
SLURM-->HPC
SLURM-->clusters
HTCondor-->clusters
```

---
layout: side-title
align: lm-lm
color: gray-light
titlell: DMS
titlewidth: is-5
---

:: title ::

## Data Management System
It’s about **files**:​ placing, replicating, removing files​

- there are **LFNs** (logical file names)
- **LFNs** are registered in *catalog(s)​*
    - where are the LFNs? (in the DIRAC File Catalog (DFC), or in Rucio)​
    - where are their metadata? (in the DFC, or in the LHCb Bookkeeping, or in AMGA)​
- LFNs *may* have **PFNs** (physical file names), stored in **SEs** (Storage Elements), that can be accessed with several protocols.​

:: content ::

```mermaid
%%{init: { 'theme': 'default' }}%%
flowchart LR;
A@{ shape: sl-rect, label: "APIs" }
DMS[("`**Data
Management
System**`")]
style DMS fill:#bbf
FC[["`**Catalog**`"]]
style FC fill:#bbf
StorageBase[["`**Storage Base**`"]]
style StorageBase fill:#bbf
DFC[("`DIRAC
Files
Catalog`")]
Rucio[("Rucio")]
style Rucio fill:#6001
TS[("`DIRAC
Transformation
System`")]
WebDav@{ shape: lin-cyl, label: "WebDav (http)" }
XRootD@{ shape: lin-cyl, label: "XRootD" }

style WebDav fill:#F23A
style XRootD fill:#F23A

A-->DMS
DMS-->FC
DMS-->StorageBase
FC-->DFC
FC-->Rucio
FC-->TS
StorageBase-->WebDav
StorageBase-->XRootD
```

<!-- 
A catalog is effectively an interface, that needs implementation. Such implementation can be the DIRAC Files Catalog, or Rucio, or any other, including extension specific ones
-->

---
layout: top-title
color: gray-light
align: c
title: integration
---

:: title ::

# How DIRAC and Rucio work together

:: content ::

The entry point is the DIRAC's `RucioFileCatalog`, which is an implementation of the `FileCatalog` "abstract" class (DIRAC has few different implementation of the same class, and you can `register_file()` to more than 1 catalog at the same time)
- in DIRAC since 2021
- by now it supports *Multi VO* and *Rucio metadata*
- The synchronization between DIRAC and Rucio is done via DIRAC
agents

Once the data is in the Rucio catalog, all the replication policies, 3rd party copy are handled by Rucio subscriptions and rules. 

This also means that:
- Admins still updates the DIRAC configuration
- No change for the download/upload from jobs: still done via the DIRAC's `DataManager`

---
layout: top-title
color: gray-light
align: c
title: namespace
---

:: title ::

# How DIRAC and Rucio work together -- namespace

:: content ::

- By default, Rucio has a flat namespace that contains files
  - Files that can be aggregated to datasets
  - Then datasets can be aggregated to container
- DIRAC uses a hierarchical namespace

The `RucioFileCatalog` "translates" from DIRAC to Rucio's namespace. All details in [this vCHEP presentation](https://indico.cern.ch/event/948465/contributions/4323983/attachments/2247115/3811355/The%20Rucio%20File%20Catalog%20in%20Dirac%20implemented%20for%20Belle%20II-2.pdf)

