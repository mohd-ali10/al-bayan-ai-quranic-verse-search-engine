Due to GitHub’s 25 MB limit, the dataset is split into two nearly equal-sized files.

To reconstruct:
python
Copy code
import json

with open("quran_part_1.json") as f1, open("quran_part_2.json") as f2:
    d1 = json.load(f1)
    d2 = json.load(f2)

d1["verses"].extend(d2["verses"])
dataset = d1
