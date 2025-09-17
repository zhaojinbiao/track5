# Installation

### Requirements
All the codes are tested in the following environment:
* Linux (trained on Ubuntu 22.04 / gpu RTX4090ti)
* Python 3.8
* PyTorch 2.1
* CUDA 11.8 or higher (PyTorch 2.1+ needs CUDA 11.8)
* [`spconv v2.x`](https://github.com/traveller59/spconv)


### Install `pcdet`

a. Clone this repository.
```shell
git clone https://github.com/open-mmlab/OpenPCDet.git
```

b. Install the dependent libraries as follows:

[comment]: <> (* Install the dependent python libraries: )

[comment]: <> (```)

[comment]: <> (pip install -r requirements.txt )

[comment]: <> (```)

* Install the SparseConv library, we use the implementation from [`[spconv]`](https://github.com/traveller59/spconv). 
    * You could also install latest `spconv v2.x` with pip, see the official documents of [spconv](https://github.com/traveller59/spconv).
  
c. Install this `pcdet` library and its dependent libraries by running the following command:
```shell
python setup.py develop
```
## Testing
### Test and evaluate the pretrained models
* Test with a  model: 
```shell script
python test.py --cfg_file ${CONFIG_FILE} --ckpt ${CKPT}
```
### ckpt and checkpoint file
```shell script
ckpt file:
      ./cfgs/DA/phase1_vehicle_drone/st3d/voxelrcnn_st3d.yaml
      ./cfgs/DA/phase2_vehicle_quadruped/pvrcnn_st3d.yaml    
```
