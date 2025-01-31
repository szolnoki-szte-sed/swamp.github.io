---
title: Introduction
layout: home
nav_order: 1
description: "SWAMP is a dataset of structured vulnerability fixes, providing curated mappings between vulnerable and fixed code."
permalink: /
---

# Structured Weakness and Mitigation Patches (SWAMP)
{: .fs-9 }

SWAMP provides a structured collection of vulnerability fixes, enabling researchers and developers to study security patches systematically across multiple programming languages.
{: .fs-6 .fw-300 }


---

{: .warning }
> This website documents the latest version of SWAMP. See [the CHANGELOG]({% link CHANGELOG.md %}) for release notes, new features, and updates.

SWAMP is an open dataset designed for security research, vulnerability detection, and software security enhancement. The dataset consolidates structured vulnerability fixes sourced from reliable repositories such as:
- **[CVEfixes Database](https://github.com/secureIT-project/CVEfixes){:target="_blank"}**
- **[CWE-Mitre Repository](https://cwe.mitre.org/data/downloads.html){:target="_blank"}**
- **[SAP’s Project Knowledge Base](https://zenodo.org/records/5855085){:target="_blank"}**

{: .note}
>  The dataset provides mappings
to Common Vulnerabilities and Exposures (CVEs) and Common Weakness Enumerations (CWEs) and covers 3581 fixes of susceptible code snippets across 38
programming languages.

## Getting started

The [SWAMP API GitHub Repository](https://github.com/szolnoki-szte-sed/swamp-api) provides everything needed to use the dataset. The repository includes:
- Documentation on how to use and extend the dataset.
- Python scripts for processing and analyzing the data.

The [SWAMP Dataset GitHub Repository](https://github.com/szolnoki-szte-sed/swamp-dataset) has the data standalone, if you would like to bould your own system to work with them, this reposotory includes:
- Metadata files and the corresponding git diffs and code chunks

{: .note }
To contribute to the SWAMP project, please fork the repository and submit pull requests.

You can use SWAMP locally by cloning the repository and installing the required dependencies.

```bash
git clone https://github.com/szolnoki-szte-sed/swamp-api.git
cd swamp
pip install -r requirements.txt
```