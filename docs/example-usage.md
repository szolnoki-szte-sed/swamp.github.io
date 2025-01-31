---
title: Example Usage
nav_order: 2
---

# Example Usage of `DatasetManager`
{: .fs-9 }

This page provides an overview of how to use the `DatasetManager` module for handling, processing, and retrieving structured vulnerability fix data from the SWAMP dataset.
{: .fs-6 .fw-300 }

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## `dataset_manager`

The `dataset_manager` module provides the `DatasetManager` class, which is responsible for downloading, extracting, and processing datasets of CVEs and their corresponding fixes. It also offers utilities for working with the dataset as a **knowledge base** or **DataFrame**.

### Classes:
- **`DatasetManager`**: Manages the dataset and provides data retrieval utilities.

### Constants:
- **`DATASET_URL`**: URL for downloading the dataset.
- **`ENV_VAR`**: Environment variable for setting the dataset's base directory.
- **`DATA_DIR`**: Default directory for storing the dataset.

---

## Example Usage

### Import the Required Modules
```python
from VulnFixLib.data_model.enum.programming_language import ProgrammingLanguage
from VulnFixLib.dataset_manager import DatasetManager
```
### Initialize the manager
```python
manager = DatasetManager()
knowledge_base = manager.load_knowledge_base()
```
### Get all items about JAVA language
```python
java_entries = manager.get_entries_by_language(knowledge_base, ProgrammingLanguage.JAVA)
```
### Get the fixdiff of the first item of the entries
```python
entry_text = manager.read_fix_diff(java_entries[0].relative_path)
```
### Get the cve of the first item of the entried
```python
cve = java_entries[0].metadata.related_vulnerability_entry.cve
print(cve)
```