---
id: symposium26
title: symposium26
---

# The First New Zealand Symposium on Software Supply Chain Security

Time:		1 December 2026 9:00 AM - 4:30 PM

Venue: 	[Victoria University of Wellington, Kelburn Campus Murphy Building MY501](https://www.wgtn.ac.nz/about/campuses-facilities/campuses/kelburn/kelburn-campus-map.pdf)

## Introduction

*Jens Dietrich and Stephen MacDonell (Victoria University of Wellington – Te Herenga Waka)*

The symposium brings together research on software supply chain security with practical approaches to strengthening the software organisations build, use, and maintain. Talks on detecting incomplete vulnerability fixes, investigating resource exhaustion, and repairing breaking changes in dependency updates address closely related challenges: understanding security weaknesses, checking that patches work, and making updates easier to adopt. Presentations on reproducibility in Rust and explainable approaches to binary equivalence explore how practitioners can verify that the packages being used in applications correspond to their source code, even when legitimate differences in build environments complicate comparison. Emerging risks in AI supply chains form another theme, spanning vulnerabilities introduced when loading downloaded models and the possibility that AI-assisted reimplementation of dependencies preserves hidden code connections and security exposures. Foundational contributions include the JavaScript taint-analysis presentation and the talk on how applications (don't) deal with errors resulting from the exhaustion of computational resources. Finally, the work on organisational capability, practitioner training, and industry collaboration, together with the SBOMBLE platform for enriching and analysing software inventories, connects these research themes to practical interventions. For practitioners, the programme offers insights into assessing exposure, validating fixes and builds, prioritising improvements, and evaluating tools that can support everyday security decisions. Throughout the programme, these presentations also showcase how state-of-the-art AI capabilities—including large language models, agentic coding tools, and explainable machine learning—are being harnessed to advance this security research. 

This project does not operate in isolation. Our work on build security is conducted in close collaboration with, and co-funded by, Oracle Inc., building on a long-standing collaboration between Oracle Labs Australia and one of the projects primary investigators. Our work on JavaScript taint analysis is carried out in collaboration with a project funded by a recently awarded major EU ERC grant, led by project member Prof. Anders Møller from Aarhus University. Finally, some of the techniques underpinning our empirical work with local industry and the public service have emerged from the NSF-funded Secure Software Supply Chain Center (S3C2) led by Prof. Laurie Williams at North Carolina State University (NCSU). We are delighted that several of these collaborators will be present at the symposium. Prof. Laurie Williams and Dr Cristina Cifuentes, former VP at Oracle Inc., will deliver keynote talks, while Prof. Anders Møller will present his latest work. The symposium therefore provides a particularly valuable opportunity to bring together researchers from these closely connected projects and collaborations.

# Keynotes 

## 9.35am Keynote 1: Cristina Cifuentes -- Software Supply Chain in the Age of AI

### Abstract

Modern software depends on components developed within organisations, supplied commercially or obtained from open-source projects. These dependencies can expand the attack surface of the resulting software. Software Bills of Materials (SBOMs) provide visibility into its composition, but translating that information into effective security decisions remains challenging. Which vulnerabilities affect a particular deployment, and how can teams address them efficiently?

Enhanced SBOM approaches, including DARPA’s E-BOSS programme, investigate how richer metadata and program analysis can support vulnerability triage and repair. Complementary frameworks such as Supply-chain Levels for Software Artifacts (SLSA) address the integrity of source and build processes.

AI is changing both vulnerability discovery and patch generation, increasing pressure on defenders to assess findings and deliver reliable fixes quickly. Initiatives such as Patch the Planet, a collaboration between OpenAI and Trail of Bits, combine AI-assisted security research with expert review to help open-source maintainers validate vulnerabilities and develop patches. These efforts also highlight the challenge of patch quality: a patch that stops a reported exploit may still leave related vulnerabilities unresolved or introduce regressions.

This keynote examines current software supply chain tools and emerging research, connecting applications of program analysis and AI with the practical needs of development teams. It considers how vulnerability findings can lead to actionable fixes, whether through dependency upgrades or patches to existing code. Particular attention will be given to the evidence needed to establish that a fix addresses the vulnerability while preserving intended behaviour, and to the tests and evaluation methods that support such assessments. The talk will explore how these capabilities can support shift-left security through feedback as developers write code, while fitting organisations’ chosen development workflows, including CI/CD where appropriate. It will also discuss barriers to adoption and research opportunities for making software supply chain security more effective in practice.

### Bio

Cristina is an Adjunct Professor at The University of Queensland where she collaborates with students and academics in the area of Software Assurance. She was previously the Vice President of the Oracle Software Assurance organisation where she led a team of security researchers and software and machine learning engineers to make application security and software assurance, at scale, a reality.  She was the founding Director of Oracle Labs Australia in 2010, where she led a team of researchers and engineers for close to 12 years, with a focus on scaling up Program Analysis techniques in new application security tools.  Cristina led and successfully released Oracle Parfait, a static analysis tool used by thousands of C, C++ and Java developers each day.  Cristina’s passion for tackling the big issues in the field of Program Analysis began with her PhD work in binary decompilation at the Queensland University of Technology, which led to her being named the Mother of Decompilation for her pioneering contributions to this domain.

## 10.30am Keynote 2: Laurie Williams -- Dependable Software, Untrusted Parts: Security Research for the Software Supply Chain

### Abstract

Since 2020, software supply chain attacks have expanded from isolated incidents to a persistent global threat. Adversaries increasingly target package ecosystems, build infrastructure, CI/CD pipelines, developer workstations, and project maintainers—exploiting the systems and relationships involved in producing software rather than the software itself. For the software engineering community, these attacks expose an uncomfortable reality: the dependability of modern software now relies as much on the integrity of its dependencies, build processes, and development environments as on the correctness of the code developers write. Organizations must continuously adapt simply to keep pace.
This talk argues that the path to transformative software supply chain research runs directly through practice. Without that grounding, researchers risk solving elegant versions of the wrong problems. Drawing on research and sustained engagement with more than 150 practitioners from over 50 companies through the NSF-funded Secure Software Supply Chain Center (S3C2), I will discuss lessons learned from the field and highlight high-impact research opportunities hidden within operational pain points, including software provenance, measurement, vulnerability intelligence, and developer environment security. These challenges call for the empirical methods, repository mining, measurement, and process research in pursuit of more reliable, dependable, and trustworthy software systems.
Just as the research community has begun to understand one software supply chain, another is emerging. AI-assisted development is transforming software production by introducing new dependencies, new trust assumptions, and new attack surfaces. Foundation models, training data, AI-generated code, hallucinated package references, and autonomous agents operating with credentials of their own are rapidly becoming part of the software ecosystem.  
The central lesson of the past five years is that trust cannot be assumed, threat models must evolve alongside development practices, and impactful research must remain grounded in operational reality. As software production becomes increasingly automated, interconnected, and AI-assisted, the challenge before us is not simply securing software artifacts—it is engineering trustworthy software production systems. The dependability of the next generation of software will depend on how well we meet that challenge

### Bio

Laurie Williams is the Goodnight Distinguished University Professor of Security Sciences in the Computer Science Department of the College of Engineering at North Carolina State University (NCSU). Laurie is the director of the National Science Foundation-sponsored Secure Software Supply Chain Center (S3C2), and co-director of the NSA-sponsored North Carolina Partnership for Cybersecurity Excellence (NC-PaCE) and the NCSU Secure Computing Institute.  Laurie is an IEEE Fellow and an ACM Fellow.  Laurie's research focuses on software security, software processes, and empirical software engineering.

## 11.30am Tehnical presentation and demonstration by Jens Dietrich and Shawn Rasheed - sbomble
 
We introduce sbomble, a tool platform we are developing to support the use and analysis of Software Bills of Materials (SBOMs) produced by a wide range of tools using standardised formats such as SPDX and CycloneDX. Sbomble visualises SBOMs and enriches them with information from multiple external data sources, currently including: (1) Vulnerability data from the current GitHub Security Advisory database and CISA’s Known Exploited Vulnerabilities (KEV) Catalog. This information helps assess vulnerability severity and exploitability, and determine whether vulnerability information contained in an SBOM is complete and up to date. (2) License data from the SPDX License List, enabling checks such as whether component licenses are OSI-approved. (3) Component and project metadata from ecosyste.ms, providing trust and maintenance signals and information about available upgrades and patches. (4) Reproducibility data from reproducible-central.

In its current form, sbomble is conceptually similar to existing tools such as OWASP Dependency-Track. We are now developing sbomble into a platform for advanced software supply-chain analysis, with a particular focus on integrating and showcasing research results. This includes capabilities for compliance checks against software supply-chain regulations and standards, as well as analyses of component reproducibility, estimated upgrade effort including automated patchability, provable exploitability of vulnerabilities, and integration of AI supply chains. Our goal is for sbomble to provide a bridge between SBOMs as standardised software inventories and more sophisticated analyses that can support security assessment, compliance, and software supply-chain research.

# 12pm Panel Discussion Moderated by Stephen MacDonell

Our expert panel of Laurie Williams, Cristina Cifuentes, Kelly Blincoe and Jens Dietrich will be providing their perspectives on a range of current related issues. You will have the opportunity to ask your questions to our panel

# 12.40pm Lunch and Networking
A light lunch is provided for those attending in person.

# Team Talks  

## 1.30pm AI-driven Automated Test Generation to Verify Partial CVE Fixes

*Valerio Terragni (University of Auckland) · Shawn Rasheed (Victoria University of Wellington – Te Herenga Waka)*

A partial vulnerability fix is a patch that addresses the originally reported vulnerability but leaves related inputs, execution paths, program states, interfaces, or configurations exploitable. To better understand this problem, we collected and analysed a Maven-focused dataset of 59 partial fixes, pairing initial vulnerability advisories with follow-on advisories and classifying what the first patch missed. Building on this dataset, we are exploring automated test-generation techniques for determining whether a vulnerability fix is complete. Our approach relies on the combination of static and dynamic analysis, large language models, and execution feedback to generate and refine executable proof-of-vulnerability tests. By running these tests against vulnerable, initially patched, and follow-on-fixed software versions, we aim to distinguish complete fixes from patches that address only the originally reported vulnerability instance. This presentation describes our research progress, the insights obtained from the dataset, and our direction for test-based validation of vulnerability fixes.

## 1.45pm Understanding Agentic AI for Repairing Dependency Breaking Changes 

*Maryam Masoudian, Kelly Blincoe, Valerio Terragni (University of Auckland)*

Library updates often introduce breaking changes that leave client code failing to compile or behaving differently. Research has proposed LLM-based techniques designed specifically to repair such breaking changes. Existing general-purpose coding agents, such as CLAUDE CODE and CODEX, can now explore and modify entire repositories on their own. Yet, it is unknown how well these agents perform compared with the proposed techniques. We compare two general-purpose agents with two techniques designed for repairing breaking changes, BYAM and the agent from prior work by Fruntke and Krinke, on BUMP and HUMANPATCH, a new dataset with human-authored fixes. The breaking-change-specific agent is the most effective, fixing up to 82.5% of the breaking changes with compilation errors and 72.8% with test failures in the BUMP dataset, whereas the general-purpose agents fix the fewest bumps. On HUMANPATCH, the general-purpose agents achieve the highest repair rates, particularly on behavioural cases that can be addressed through configuration-based adaptations. Behavioural breaking changes that require source code adaptations remain challenging. Compared with the developers’ fixes, the agents’ fixes are narrower, as they rarely improve the readability or maintainability of the adapted code as developers do. Our results show that general-purpose agents do not yet replace dedicated techniques for repairing breaking changes, but could complement them.

## 2pm Reproducibility of Rust Packages

*Elliott Wen, Chenye Ni (University of Auckland)*

Reproducible builds are increasingly viewed as an important foundation for software supply-chain security: if an independently rebuilt artifact matches the published artifact, users gain confidence that the software they receive corresponds to publicly available source code. But how well does this idea work in practice, and what should we do when legitimate differences in build environments make byte-for-byte reproduction impossible?

In this talk, I examine these questions in the Rust ecosystem from two complementary perspectives. First, I present a large-scale empirical study of independent rebuilding on crates.io. Using OSS-Rebuild, we rebuild 20,000 Rust package releases and find that only 10.3% can be reproduced byte for byte. Most unsuccessful attempts do not reveal malicious or inherently unreproducible software; instead, they expose a more fundamental challenge: faithfully recovering the conditions under which an artifact was originally packaged. Differences in Cargo versions, dependency resolution, source checkout settings, archive metadata, and publishers' local environments can all cause independently produced artifacts to diverge.

These findings motivate a broader question. If two artifacts are produced from the same source but under different legitimate toolchains or build configurations, must they be identical to be trusted? I introduce RustBuildEq, a large-scale benchmark designed to study this problem through binary equivalence rather than strict binary equality. RustBuildEq contains millions of equivalent and non-equivalent Rust artifact pairs generated across diverse toolchains, code-generation backends, optimization settings, and target platforms, providing ground truth for training and evaluating automated equivalence techniques.

## 2.15pm JavaScript Taint Analysis

*Anders Møller (Aarhus University)*

Taint analysis is a widely used approach for detecting security vulnerabilities, such as command injection and leakage of sensitive information. Existing taint analyzers for JavaScript often ignore complex language features, leading to substantial unsoundness and imprecision, and rely on library models to achieve scalability. I will argue that whole-program points-to analysis can provide a more robust foundation for taint analysis, and present preliminary results from a new tool built on the Jelly analyzer. Finally, I will outline the plans for my new ERC Advanced Grant project, "Program Analysis for Software Supply Chain Security".

## 2.30pm Binary Equivalence for Reproducing Builds Using Explainable AI

*Andrew Lensen, Jens Dietrich, Alix Van Schultze (Victoria University of Wellington – Te Herenga Waka)*

A known attack vector is to exploit weaknesses in automated processes used to build and deliver software. Real-world attacks and incidents in this space include SolarWinds, XCodeGhost, and xz. A common approach to checking for compromised builds is to reproduce those builds, i.e. independently re-build a package and compare the results. Differences may suggest problems, such as backdoors injected by a compromised compiler or another build tool. Unfortunately, this does not work well in practice, as build results often differ due to hard-to-control variability in build environments. This makes security analyses based on comparing build results imprecise, and therefore of limited use.

In our prior work, together with researchers from Oracle Inc., we designed tooling (daleq and daleq4py) that successfully tackles the precision issue by providing a sound notion of binary equivalence supported by provenance. A limitation of this approach is that it requires the manual coding of rules and is therefore hard to maintain. In this talk, we present a novel approach to address this limitation using AI and machine learning techniques, along with initial results from evaluation experiments. Notably, these techniques use explainable AI: they preserve the generation of rich provenance information, making the resulting analyses transparent and trustworthy to security engineers.

## 2.45pm Deserialization Vulnerabilities in Hugging Face

*Xiang Guo, Heitor Gomes, Jens Dietrich (Victoria University of Wellington – Te Herenga Waka)*

Machine learning models and large language models (LLMs) are increasingly distributed through centralized repositories such as Hugging Face. These models rely on a variety of serialization formats and on complex software libraries for deserialization. As deserialization is prone to vulnerabilities, loading such models introduces risks into the supply chains of AI applications. Numerous vulnerabilities have been reported that can trigger severe impacts during model loading when crafted payloads are deserialized, such as CVE-2025-62609, CVE-2026-27489, CVE-2026-24747, and others. At the same time, AI application frameworks such as vLLM, Ollama, and LangGraph are being rapidly adopted by both industry and independent developers. These frameworks can consume and deploy models across multiple formats, thereby facing deserialization-related security risks introduced by the underlying software supply chain. Our preliminary work conducts a longitudinal analysis of 56,533 models across 39 time points, documenting a community-wide transition from Pickle toward SafeTensors and GGUF while a long tail of co-existing formats sustains non-trivial download volume. A complementary SBOM analysis of 9,983 Hugging Face Spaces identifies 472 deserialization-related CVEs affecting 5,734 spaces, confirming that supply-chain-level exposure is both widespread and largely underexplored. To validate the deserialization threats we have found, we are constructing a benchmark dataset of exploitable CVEs covering model formats, deserialization libraries, and AI application frameworks. This dataset will be used to evaluate the capability of state-of-the-art AI vulnerability scanners and to support the development of our own detection methodologies.

## 3pm Helping New Zealand Organisations Understand, Develop, and Advance Software Supply Chain Security

*Lisa Patterson, Stephen MacDonell (Victoria University of Wellington – Te Herenga Waka), Kelly Blincoe (University of Auckland)*

Software supply chain security (SSCS) has become a strategic capability for organisations of all sizes. Yet many still face the same pressing questions: what are the key things we do not know about SSCS, what capability gaps exist, and which improvements should be prioritised.

This session will present opportunities for NZ organisations to engage with our work in three areas: (1) practitioner-focused capability development, (2) evaluation of emerging software supply chain security tools, and (3) organisational assessments of SSCS capability.

Developed at the Secure Software Supply Chain Center (S3C2), the Proactive Secure Software Supply Chain Risk Management (P-SSCRM) Framework aims to help organisations understand, quantify, and strengthen their software supply chain risk management initiatives. To support practitioners, we are exploring the potential of a role-aware training platform that translates P-SSCRM practices into personalised, self-paced learning. Informed by feedback from NZ industry partners, the platform will be designed to deliver concise, practical guidance tailored to an individual's role and responsibilities, helping practitioners build capability and turn good practice into everyday action.

We are also seeking collaborators in NZ to trial and evaluate software supply chain security technologies currently under development by our research team, helping assess their practical value in real-world environments and enabling organisations early access to cutting-edge tools to improve SSCS capability.
Finally, we are seeking to partner with New Zealand organisations to undertake comprehensive P-SSCRM assessments that help identify strengths, uncover improvement opportunities, and prioritise next steps.

This session will highlight practical opportunities to strengthen software supply chain security and resilience through capability development, evaluating emerging technologies, and understanding your organisation's current position.


## 3.15pm How the Grinch may steal Dependencies

*Timothee Riom, Heitor Gomes, Jens Dietrich (Victoria University of Wellington – Te Herenga Waka)*

The Software Supply-Chain is a space of Trust.
Trust that you can use a library without being flooded with disclosed vulnerabilities; trust that the maintainer will ship a fix, should a vulnerability be disclosed; trust that you can safely use a binary or a model that you download; trust that you can replicate the same results from machine to machine; and trust that all the actors are aware of the risk and enforce the best practices to protect this sphere.
One must trust many, notably external actors. Mostly people you do not know, some you will never know, and many you do not even know you implicitly trust.

We investigate a future where the skyrocketing number of AI-discovered exposures has worn down organisations' patience. They decided not to rely on dependencies anymore, or significantly less, and to reimplement each functionality internally. And the scourge of our time may also provide the remedy of our age, as AI collapses the cost of generating code. Either way, the consequence is substantially less collective effort to fix what exists and expand the software supply chain, while it remains the foundation language models are trained on and memorise.

We investigate this future in today’s programs that don't declare any dependencies yet carry the same functionality. We investigate if they are truly independent, truly severed from the Supply Chain. Or whether they hide their connections: do they share code, share exposures?
And finally, if this is the next dawn of programming: is it so bad after all?
What tools from the software supply chain can we keep, which ones should we tweak, and which should we build?


## 3.30pm Resource Exhaustion in the Wild

*Shawn Rasheed, Jens Dietrich (Victoria University of Wellington – Te Herenga Waka)*

Resource exhaustion in software is a common cause of denial of service. As the recent PHP2Shell vulnerability illustrates, code that handles resource exhaustion can also introduce more serious vulnerabilities. These risks make it important to understand how resource exhaustion occurs and how software handles it. We examined both aspects in 93 parsing libraries for 24 widely used file and data formats (e.g. YAML, JSON, Markdown, PDF, TrueType) across the Java (Maven), Python (PyPI), Go and JavaScript (npm) ecosystems. We used static analysis to locate instances of a code pattern associated with resource exhaustion. We used those instances as inputs to a large language model to generate test inputs. We then ran the parsers on those inputs to determine whether their behavior led to resource exhaustion and characterised the resulting failure modes, including stack overflows, out-of-memory errors, timeouts, and program crashes. We also characterised the libraries’ mitigations and their effectiveness. Maintainers accepted some of the reported issues as vulnerabilities and performance bugs.

## 3.45pm Closing remarks and thanks
*Jens Dietrich

## 4pm Symposium concludes
