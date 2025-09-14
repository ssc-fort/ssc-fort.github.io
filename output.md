---
id: output
title: output
---


# Software

- [DALEQ - Datalog-based Binary Equivalence.](DALEQ - Datalog-based Binary Equivalence) - a tool for the comparison of binaries from alternative / reproduced builds, currently being used or evaluated by Oracle and Google. [[paper]](https://www.arxiv.org/abs/2508.01530)
- [shade detector](https://github.com/jensdietrich/shadedetector) - a tool to find vulnerable clones in Maven Central, has led to several [GHSA](https://github.com/advisories) updates, including for [CVE-2021-44228 (aka log4shell)](https://nvd.nist.gov/vuln/detail/cve-2021-44228) [[paper]](https://dl.acm.org/doi/10.1145/3689944.3696165)


# Datasets

- [xshady](https://github.com/jensdietrich/xshady) - Proof-Of-Vulnerability Tests for common Java vulnerabilities. [[paper]](https://dl.acm.org/doi/10.1145/3689944.3696165) 
- [alternative builds dataset](https://zenodo.org/records/14915249) - binaries built from the same source by different organisations (Oracle, Google, RedHat, developer) [[paper1]](https://arxiv.org/abs/2410.08427), [[paper2]](https://www.arxiv.org/abs/2508.01530)
- [oracles for the equivalence of java bytecode](https://zenodo.org/records/13381845) - pairs of compiled Java classes that should be classified either as equivalent, or not equivalent [[paper]](https://dl.acm.org/doi/10.1145/3689944.3696162)

# Vulnerabilities


### Changes to GHSA Entries 

Details are described in [this paper](https://dl.acm.org/doi/10.1145/3689944.3696165).

| CVE | GHSA PR |
| --- | --- |
| CVE-2022-38749 | https://github.com/github/advisory-database/pull/2258 |
| CVE-2022-42889 |  https://github.com/github/advisory-database/pull/2273 |
| CVE-2015-6420  | https://github.com/github/advisory-database/pull/2326  |
| CVE-2018-10237 |  https://github.com/github/advisory-database/pull/2444  |
| CVE-2021-44228 |  https://github.com/github/advisory-database/pull/2445 |
| CVE-2019-12402 |  https://github.com/github/advisory-database/pull/2823 |
| CVE-2016-5394  |  https://github.com/github/advisory-database/pull/2826 |
| CVE-2016-6798  |  https://github.com/github/advisory-database/pull/2827 |
| CVE-2015-7501  |  https://github.com/github/advisory-database/pull/2841 |
| CVE-2018-1324  |  https://github.com/github/advisory-database/pull/2855 |
| CVE-2021-29425 | https://github.com/github/advisory-database/pull/3506 | 



### Deserialisation Vulnerabilities

These CVEs were discovered as part of Shawn Rasheed's PhD co-supervised by Jens and inspired by the [Evil Pickles study](https://drops.dagstuhl.de/storage/00lipics/lipics-vol074-ecoop2017/LIPIcs.ECOOP.2017.10/LIPIcs.ECOOP.2017.10.pdf). 

- CVE-2018-11797 (PDFBox)
- CVE-2019-17063 (PDFxStream)
- CVE-2018-19478 (GhostScript)
- CVE-2019-20446 (Librvg) 
- https://github.com/advisories/GHSA-2pr6-76vf-7546  (js-yaml )

We discovered and disclosed the following: PDFBox CVE-2018-11797, PDFxStream CVE-2019-17063, GhostScript CVE-2018-19478 , Librvg CVE-2019-20446, js-yaml https://github.com/advisories/GHSA-2pr6-76vf-7546 



 



