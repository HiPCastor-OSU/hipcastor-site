---
title: "HiPCastor - Research"
layout: textlay
excerpt: "HiPCastor -- Research"
sitemap: true
permalink: /research/
---

Our overarching goal is to research and develop new techniques applied to
a diverse spectrum of computer systems (including edge, cloud and
high-performance computing) and across layers of abstraction (including
computer architecture, operating systems, virtualization, middleware, software engineering, and
applications).

Here are some areas that we currently work in:

### Serverless Workflows (FaaS)
<div class="hpc-card">
**Function-as-a-Service, serverless workflows.** Modern Function-as-a-Service
(FaaS) cloud platforms offer great potential for supporting event-driven
scientific workflows. Nonetheless, there remain barriers to adoption by the
scientific community in domains such as environmental sciences, where R is the
focal language used for the development of applications and where users are
typically not well-versed with FaaS APIs. We have designed and implemented
[FaaSr](https://faasr.io), a novel open-source middleware that supports
event-driven scientific workflows in R. A key novelty in FaaSr is the ability
to deploy workflows across FaaS providers without the need for any managed
servers for coordination. We have also explored using lightweight per-function
virtual machines ([virtines](https://github.com/virtines/wasp)) to enable more strongly isolated FaaS platforms.
</div>

### High-performance Memory Systems
<div class="hpc-card">
Modern memory systems involve designs aimed at surmounting the "memory wall,"
where memory capacity and bandwidth can limit workload performance. We are
investigating new system software support for disaggregated memory, where
a workload's memory is transparently expanded across nodes in a cluster. In
particular, we developed a new compiler and runtime system for high-performance
far memory called [TrackFM](https://dl.acm.org/doi/10.1145/3617232.3624856). To
address memory bandwidth limitations, near-data processing architectures move
compute nearer to memory, for example with processing units integrated near
DRAM banks. We are investigating new software and hardware abstractions for
next-generation processing-in-memory (PIM) architectures.
</div>

### System Software for HPC
<div class="hpc-card">
We are interested in ground-up redesigns of the
hardware/software layer for high-performance computing. In the past, we have developed new
[operating systems](https://users.cs.northwestern.edu/~pdinda/Papers/sc21.pdf), [virtual machine monitors](https://github.com/virtines/wasp),
[languages](https://doi.org/10.1145/3453483.3460969), [compilers](https://dl.acm.org/doi/10.1145/3617232.3624856), and [hardware designs](https://ieeexplore.ieee.org/document/8842897) for HPC.
</div>

### Scientific Data Compression
<div class="hpc-card">
Scientific simulations and instruments generate data far faster than it can be
stored or moved, and data compression is a direct way to address this challenge.
We design scientific data compressors that provide guarantees on the analysis rather than only on individual data points:
preserving critical points through
[sign-of-determinant predicates (ICDE'24)](https://doi.org/10.1109/icde60146.2024.00378),
topological skeletons in [TspSZ (ICDE'25)](https://doi.org/10.1109/icde65448.2025.00275),
and critical-point trajectories in
[time-varying vector fields (ICDE'26)](https://doi.org/10.1109/icde65706.2026.00168).
Related efforts extend error-controlled compression to
[unstructured scientific data (IPDPS'25, Best Paper)](https://doi.org/10.1109/ipdps64566.2025.00040),
improve the efficiency of interpolation-based compressors with
[adaptive quantization index prediction (IPDPS'25)](https://doi.org/10.1109/ipdps64566.2025.00091),
[mitigate the artifacts](https://doi.org/10.1109/ipdps65963.2026.00024) that
pre-quantization-based compressors introduce, and preserve user-specified
[quantities of interest (VLDB'25)](https://doi.org/10.14778/3742728.3742739).
We are also making compressed data directly usable, enabling
[analytical operations to run on compressed representations (ICDE'26)](https://doi.org/10.1109/icde65706.2026.00117)
through multi-stage decompression instead of full reconstruction.
</div>

### Progressive Data Management
<div class="hpc-card">
Compression alone does not solve data movement: archived data still has to cross
wide-area networks or return from secondary storage, and different analyses need
very different levels of accuracy from the same dataset. We work on progressive
representations, which allow data to be refactored once and then retrieved
incrementally, so a consumer fetches only as many bits as its target accuracy
requires rather than the entire dataset. This line of work established
[error-controlled progressive retrieval under derivable quantities of interest (SC'24)](https://doi.org/10.1109/sc41406.2024.00092),
scaled refactoring and retrieval to modern GPUs in
[HP-MDR (SC'25)](https://doi.org/10.1145/3712285.3759845), added guaranteed
error control for quantity-of-interest-based retrieval in
[QProR (HPDC'26)](https://doi.org/10.1145/3806645.3807579), and most recently
improved the quality of the progressive representations themselves through
adaptive interpolation and coefficient decomposition (SC'26).
</div>

### Software-defined virtual networks for edge-to-cloud computing
<div class="hpc-card">
While within cloud data centers, nodes can communicate without the presence of
Network Address Translators (NATs), edge computing applications require devices
to communicate across different private networks and must deal with NAT
traversal to enable edge-to-edge communication. We have designed and
implemented [EdgeVPN](https://edgevpn.io), a technique that enables
virtual private Ethernet networks that span edge and cloud resources
– including those constrained by NAT and firewall middleboxes. EdgeVPN builds
upon a scalable structured peer-to-peer overlay, and
integrates overlay tunnels with Software Defined Networking (SDN) software
switches to create a virtual network with dynamic membership – supporting
unmodified Ethernet/IP stacks to facilitate the deployment of edge
applications.
</div>

### System techniques to efficiently serve large-scale AI models on HPC systems
<div class="hpc-card">
Systems and algorithms for deploying and optimizing large
deep neural networks at scale on HPC platforms. Foundational work includes
[Fauce (VLDB'21)](https://vldb.org/pvldb/vol14/p1950-liu.pdf), an efficient
framework for deep ensemble inference;
[MD-HM (ICS'21)](https://dl.acm.org/doi/10.1145/3447818.3460365), a memory
optimization scheme for large molecular dynamics simulations; and
[Tahoe (EuroSys'21)](https://dl.acm.org/doi/abs/10.1145/3447786.3456251),
high-performance inference for decision tree ensembles on GPUs.
Building on this base, we have advanced scalable large-scale LLM
serving with new methods for retrieval-augmented generation (RAG), multi-agent
coordination, and an automatic framework for plugging AI surrogates into HPC
applications, [Auto-HPCnet (HPDC'23)](https://dl.acm.org/doi/10.1145/3588195.3592985).
These efforts introduce a unified software stack that
connects low-level operators, model execution, and end-to-end applications for
large-scale AI. 
</div>

### Efficient and physics-informed AI for scientific applications
<div class="hpc-card">
Domain-aware and efficient AI methods that reduce
simulation cost while preserving physical fidelity.
[Adaptive Neural Network-Based Approximation to Accelerate Eulerian Fluid Simulation (SC'19)](https://dl.acm.org/doi/10.1145/3295500.3356147)
demonstrated neural surrogates for accelerating fluid dynamics.
[Smart-PGSim (SC'20)](https://ieeexplore.ieee.org/abstract/document/9355288)
showed AI acceleration for power grid simulation and was later highlighted by
[DOE](https://www.newswise.com/doescience/pnnl-researchers-speed-power-grid-simulations-using-ai/?article_id=741430)
and
[PNNL](https://www.pnnl.gov/news-media/pnnl-researchers-speed-power-grid-simulations-using-ai#:~:text=Share%3A,the%20blink%20of%20an%20eye).
[Auto-HPCnet (HPDC'23)](https://dl.acm.org/doi/10.1145/3588195.3592985)
introduced an automated framework for constructing neural surrogate models for
HPC applications, bridging AI workflows and large-scale simulation codes.
[TimeX++ (ICML'24)](https://dl.acm.org/doi/10.5555/3692070.3693367) extended
these ideas for temporal modeling through an
interpretable and efficient time-series learning framework for scientific
forecasting. Most recently, our submitted IPDPS'26 paper
[LUMOS](https://github.com/Picomp-lab/LUMOS-IPDPS26) advances SciML
efficiency by unifying automatic feature selection and structured parameter
pruning through L0-regularized learning, reducing manual trial-and-error in
building high-quality scientific surrogate models.
Together, these contributions advance surrogate modeling, AI model efficiency,
and uncertainty-aware learning and fine-tuning for scientific workloads. 
</div>

### System optimization on AI accelerators
<div class="hpc-card">
Runtime and system-level techniques for emerging AI
accelerators, with a focus on Cerebras wafer-scale engines. These platforms
depart from the traditional GPU model by providing very large on-chip compute
and memory capacity, and our work helps unlock their potential for training and
serving increasingly large AI models.
Our recent workshop paper,
[Phoenix (SC'25 Workshop)](https://dl.acm.org/doi/10.1145/3731599.3767395),
presents a framework for scalable and memory-efficient execution of sparse LoRA
workloads on Cerebras systems, enabling larger and more efficient fine-tuning
on wafer-scale hardware. This work is conducted in collaboration with Argonne
and Yale University.
Current student projects extend to RAG optimization on Cerebras, leveraging its
massive on-chip memory to redesign dataflow and caching for LLM-based
scientific and data-intensive applications.
</div>

## Software
<div class="hpc-card">
- [EdgeVPN](https://github.com/edgevpnio) - VPN at the edge
- [FaaSr](https://github.com/FaaSr) - Function-as-a-Service for R
- [LUMOS](https://github.com/Picomp-lab/LUMOS-IPDPS26) - SciML workflow optimization with unified feature and parameter adaptation
- [Phoenix](https://github.com/Picomp-lab/Phoenix) - sparse LoRA fine-tuning and inference on wafer-scale systems
- [Shipyard](https://github.com/xyang76/shipyard) - Load balanced, sharded consensus
- [TrackFM compiler](https://github.com/compiler-disagg/TrackFM) - automated far memory for legacy apps
- [Wasp](https://github.com/virtines/wasp) - a microhypervisor for function-granularity virtualization
</div>

## Sponsors
<div class="hpc-card" markdown="0">
  <div class="hpc-sponsor-logos">
    <a href="https://www.nsf.gov" target="_blank" rel="noopener">
      <img src="{{ '/images/logopic/nsf.png' | relative_url }}" alt="National Science Foundation" class="hpc-sponsor-logo" decoding="async">
    </a>
    <a href="https://www.intel.com" target="_blank" rel="noopener">
      <img src="{{ '/images/logopic/intel-logo.svg' | relative_url }}" alt="Intel" class="hpc-sponsor-logo" decoding="async">
    </a>
    <a href="https://www.samsung.com" target="_blank" rel="noopener">
      <img src="{{ '/images/logopic/samsung.png' | relative_url }}" alt="Samsung" class="hpc-sponsor-logo" decoding="async">
    </a>
  </div>
</div>
