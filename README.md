---
dataset_info:
  features:
  - name: caption
    dtype: string
  - name: code
    dtype: string
  - name: image
    dtype: image
  - name: pdf
    dtype: binary
  - name: uri
    dtype: string
  - name: origin
    dtype: string
  - name: date
    dtype: timestamp[us]
  splits:
  - name: train
    num_bytes: 6626976796.75989
    num_examples: 145366
  - name: test
    num_bytes: 37202393.284
    num_examples: 542
  download_size: 6309512462
  dataset_size: 6664179190.04389
configs:
- config_name: default
  data_files:
  - split: train
    path: data/train-*
  - split: test
    path: data/test-*
license: other
pretty_name: DaTikZ-v3
size_categories:
- 100K<n<1M
---
# Dataset Card for DaTi*k*Z<sub>v3</sub>
DaTi*k*Z<sub>v3</sub> is a dataset of Ti*k*Z drawings aligned with captions. In compliance with licensing agreements, certain Ti*k*Z drawings are excluded from this public version of the dataset. Check out the [DeTi*k*Zify](https://github.com/potamides/DeTikZify) project and the [DaTi*k*Z](https://github.com/potamides/DeTikZify) repository for more information as well as tools and methods to recreate the complete dataset from scratch.

## Usage
```python
from  datasets  import  load_dataset
# full dataset
ds = load_dataset("nllg/datikz-v3")
# only the train split
ds = load_dataset("nllg/datikz-v3", split="train")
for sample in ds:
    print(sample["code"])
```