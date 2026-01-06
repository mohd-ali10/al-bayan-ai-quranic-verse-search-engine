# Dataset Splitting Guide

## Overview

This repository contains a large Quran dataset that exceeds GitHub’s single-file size limit (25 MB). To comply with this restriction while preserving data integrity, the dataset has been **split into two nearly equal-size JSON files**.

The split is performed **by actual file size (MB)** rather than by record count, ensuring both files remain uploadable and balanced.

---

## Why the Dataset Is Split

* GitHub does not allow files larger than **25 MB**
* The original dataset (`quran_complete.json`) is approximately **37 MB**
* Splitting by size ensures:

  * GitHub compatibility
  * No data loss
  * Easy reconstruction
  * Academic and viva-friendly justification

---

## Dataset Structure

The original JSON file has the following structure:

```json
{
  "metadata": { ... },
  "verses": [ ... ]
}
```

* `metadata` remains identical in both files
* Only the large `verses` list is split

---

## Files Included

```
data/
 ├── quran_part_1.json
 ├── quran_part_2.json
```

Each file is **below 25 MB** and contains a portion of the verses along with full metadata.

---

## How the Split Was Performed

* Executed using **Python in Google Colab**
* Split based on **serialized JSON size in bytes**
* Ensures both output files are approximately equal in size

This approach is robust, reversible, and suitable for research and production use.

---

## Reconstructing the Original Dataset

To merge the two files back into a single dataset:

```python
import json

with open("quran_part_1.json", "r", encoding="utf-8") as f1, \
     open("quran_part_2.json", "r", encoding="utf-8") as f2:
    d1 = json.load(f1)
    d2 = json.load(f2)

d1["verses"].extend(d2["verses"])
full_dataset = d1
```

After merging, `full_dataset` will be identical to the original `quran_complete.json`.

---


