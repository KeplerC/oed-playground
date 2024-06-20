# Berkeley MVP Data

Basic motor control tasks (reach, push, pick) on table top and toy environments (toy kitchen, toy fridge).

**Tags**: [Open-X-Embodiment](oed-playground/tree/master/pages/tags/Open-X-Embodiment.md), [Robot:xArm](oed-playground/tree/master/pages/tags/Robot:xArm.md), [Single_Arm](oed-playground/tree/master/pages/tags/Single_Arm.md), [Human_VR](oed-playground/tree/master/pages/tags/Human_VR.md), [Scene:Table_Top](oed-playground/tree/master/pages/tags/Scene:Table_Top.md), [Scene:Kitchen](oed-playground/tree/master/pages/tags/Scene:Kitchen.md)

## Sampled Visualization



## Download


```python
# Method 1: 
import tensorflow_datasets as tfds
tfds.builder_from_directory(builder_dir="gs://gresearch/robotics/berkeley_mvp_converted_externally_to_rlds/0.1.0")
ds = b.as_dataset(split='train[:10]')

# Method 2:
import fog_x
dataset = fog_x.Dataset(
    name="demo_ds",
    path="~/test_dataset", # can be AWS S3, other Google Bucket
)  

dataset.load_rtx_episodes(
    name="gs://gresearch/robotics/berkeley_mvp_converted_externally_to_rlds/0.1.0",
)
```


## Citation

@InProceedings{Radosavovic2022,
  title = {Real-World Robot Learning with Masked Visual Pre-training},
  author = {Ilija Radosavovic and Tete Xiao and Stephen James and Pieter Abbeel and Jitendra Malik and Trevor Darrell},
  booktitle = {CoRL},
  year = {2022}
}