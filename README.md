# monk_v1
#### Monk is a low code Deep Learning tool and a unified wrapper for Computer Vision.
[![Version](https://img.shields.io/badge/version-v1.0-lightgrey)](https://github.com/Tessellate-Imaging/monk_v1) &nbsp; &nbsp;
[![Build_Status](https://img.shields.io/badge/build-passing-green)](https://github.com/Tessellate-Imaging/monk_v1)


## Create an image classification experiment.
- Load foldered dataset
- Set number of epochs
- Run training

```python
ptf = prototype(verbose=1)
ptf.Prototype("sample-project-1", "sample-experiment-1")
ptf.Default(dataset_path="./dataset_cats_dogs_train/", 
                model_name="resnet18", freeze_base_network=True, num_epochs=2)
ptf.Train()
```

## Inference

```python
img_name = "./monk/datasets/test/0.jpg";
predictions = ptf.Infer(img_name=img_name, return_raw=True);
print(predictions)
```


## Compare Experiments

- Add created experiments with different hyperparameters
- Generate comparison plots

```python
ctf = compare(verbose=1);
ctf.Comparison("Sample-Comparison-1");
ctf.Add_Experiment("sample-project-1", "sample-experiment-1");
ctf.Add_Experiment("sample-project-1", "sample-experiment-2");
    .
    . 
    .
```

## RoadMap
- [] Incorporate pep coding standards
- [] Tackle Multiple versions of pytorch, keras, gluon
- [] Standardize folder structure for next feature additions - object detection, image segmentation
- [] Add support for tensorflow-2.0
- [] Add unit-testing


## Copyright

Copyright 2019 onwards, Tessellate Imaging Private Limited Licensed under the Apache License, Version 2.0 (the "License"); you may not use this project's files except in compliance with the License. A copy of the License is provided in the LICENSE file in this repository.