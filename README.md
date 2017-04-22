### This code base is no longer maintained and exists as a historical artifact to supplement our CVPR 2016 paper. For more recent work, please see [craftGBD](https://github.com/craftGBD/craftGBD).

# Factors in Finetuning Deep Model for object detection

by Wanli Ouyang, Xiaogang Wang, Cong Zhang, Xiaokang Yang

## Introduction

We cluster objects into visually similar class groups and learn deep representations for these groups separately. A hierarchical feature learning scheme is proposed. In this scheme, the knowledge from the group with large number of classes is transferred for learning features in its sub-groups. For more details, please refer to our [arXiv paper](http://arxiv.org/abs/1601.05150).

### Citation

If you find the code or the models useful, please cite this paper:
```
@inproceedings{wanli2016factors,
	author    = {Wanli Ouyang, Xiaogang Wang, Cong Zhang, Xiaokang Yang},
	title     = {Factors in Finetuning Deep Model for object detection},
	booktitle = {CVPR},
	year      = {2016},
}
```

## Installation

### Caffe

The [caffe with multi-GPU support](https://github.com/yjxiong/caffe) is recommended for fine-tuning the model. You can build and run the code by the following commands.

```
mkdir build && cd build
cmake .. -DUSE_MPI=ON
make && make install
mpirun -np 4 ./install/bin/caffe train --solver=<Your Solver File> [--weights=<Pretrained caffemodel>]
```

### Proposals

We are using the [CRAFT Objects from Images](http://arxiv.org/abs/1604.03239) for generating proposals.

* 13val1 + 14val download: [link](http://pan.baidu.com/s/1csmEkA)
* 13train_positive download: [link](http://pan.baidu.com/s/1nv4b6lj)
