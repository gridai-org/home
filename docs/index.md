---
layout: default
title: GridAI
---

# GridAI — GReen Itinerant Distributed AI

*Moving bits, not electrons: following the sun and the wind, making AI workloads nomadic, the renewable way.*

---

## Bits or electrons?

Datacentre electricity demand is projected to double by the end of the decade. In 2024 alone, Europe curtailed more than EUR 7 billion of renewable energy because the grid has not yet been sized to deliver it where compute is concentrated. The current European response is to build transcontinental HVDC corridors to move electrons across the continent, an investment of tens of billions of euros over multi-decade horizons. The dual question has been largely missing: *why not move the computation to where the electrons are?*

## The GridAI bet: nomadic AI compute

GridAI proposes the first operational theory of *nomadic AI compute*. AI workloads are not nailed to the site where they are born, and not all of them need to run immediately. Every eligible workload has a *nomadic envelope*: the space-time surface within which it can run while preserving its quality of service. The envelope has two physical, measurable dimensions, spatial mobility (the joule and time cost of moving the workload state across an inter-site link) and temporal mobility (the workload's deferrability, from seconds for live inference to days for periodic batch). Today the envelope is invisible to AI orchestration; GridAI makes it explicit, measurable and auditable.

Every orchestration choice becomes a selection among three explicitly-priced levers of the *bit ↔ electron ↔ time* hinge: moving bits pays communication, moving electrons pays the HVDC chain, moving in time pays storage or deferrability.

## Compute is virtual power storage

The time lever has two fungible sub-modes: charging a battery, or accelerating a deferrable workload from the backlog using the renewable surplus *now*. The two have the same carbon-balance effect, modulo specific costs and losses. Therefore **compute is virtual power storage for deferrable AI workloads**: part of a national battery can be built in silicon rather than in lithium. GridAI surfaces this trade-off as the *silicon ↔ lithium isopreference frontier*, the quantitative interface for negotiating the build-out of the renewable-native flexibility envelope.

## What is in, what is out

GridAI applies to workloads compatible with inter-site execution: single-GPU jobs, federated training with sparse synchronisation and gradient compression, asynchronous schemes, sharded inference, and any pure inference workload. FullSync data-parallel training of frontier-scale models on NVLink-class fabrics is out of scope by construction, because an NVLink domain is not reproducible across a continental WAN, and the framework does not promise what physics does not allow.

By the same logic, the share of European curtailment GridAI can address is a fraction of what HVDC corridors are designed to transport, and the share of AI workloads that can move off centralised hyperscaler facilities is a fraction of the global AI compute mix. In both cases the fraction is small in relative terms but large in absolute terms, large enough to justify a dedicated infrastructure alongside the HVDC build-out rather than as a competitor to it.

## The operational stack

GridAI is structured around four layers. A *four-scale green infrastructure design* sites compute at four geo-energetic levels: nano-datacentres on low voltage (Home-DC, Building-DC) and micro-datacentres on medium and high voltage (Neighbourhood-DC, Hot-spot-DC). A *programmable data plane* on SRv6 and in-band telemetry measures the per-flow energy and carbon and selects the greenest inter-site path at line rate. A *multi-lever orchestrator* arbitrates at every step among four moves: consume now, charge storage, accelerate the deferrable backlog, or curtail. A *verifiable green-compute certificate* is produced as a byproduct of every decision, anchored in a site-level cryptographic root-of-trust and committed to a tamper-evident transparency log; the format is pushed toward an IETF Internet-Draft.

## The empirical commitment

The framework is being validated end to end on a federated Italian testbed of energy-proximate sites, anchored on the PrinceLab cyber-physical platform at the Politecnico di Bari and connected through the GARR national research backbone. Over thirty-six months, the project will run a federated continual-learning workload of a contemporary large language model on renewable-native energy, demonstrate the storage-compute equivalence principle *in vivo*, and produce a third-party-auditable green-compute certificate covering the entire trajectory. An AI-RAN node is deployed as a second load, at the tightest edge of the envelope.

## A European invitation

The Italian testbed is the right scope for a single research effort, but not for the European-scale conclusions the framework is designed to inform. We invite European partners to engage along three concrete tracks: cross-validation of the simulator on non-Italian grid data, cross-deployment of the federated testbed across European sites via GARR/GÉANT, and IETF standardisation around green-computing monitoring and certification.

---

## Read more

- **[Two-pager pitch (PDF)](papers/gridai-pitch-two-pager.pdf)** — the framework in 5 minutes.
- **[Position paper (PDF)](papers/gridai-position-paper.pdf)** — the full framework, companion to the NOMS 2026 paper *Green Distributed AI Training: Orchestrating Compute Across Renewable-Powered Micro Datacenters*.

---

## The consortium

GridAI is a proposal under PRIN 2026, the main research-funding call of the Italian Ministry of University and Research. The consortium is composed of six Italian state universities: Politecnico di Bari, Politecnico di Milano, Politecnico di Torino, Università Federico II di Napoli, Università di Pisa, Università di Roma "Tor Vergata". It is supported by industrial and institutional stakeholders from the Italian and German energy, telecommunications and academic ecosystems.

*Principal Investigator: Antonio Capone (Politecnico di Milano). Technical coordination contact: Stefano Salsano (Università di Roma Tor Vergata).*
