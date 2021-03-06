## Project Details
Pipeline based on Open-MMLAB MM-Detection project - https://github.com/open-mmlab/mmdetection
<br />
<br />
<br />

# Supported Models
  - mask_rcnn_r50_fpn
  - mask_rcnn_r101_fpn
  - mask_rcnn_x101_32x4d_fpn
  - mask_rcnn_x101_32x4d_fpn
  - cascade_mask_rcnn_r50_fpn
  - cascade_mask_rcnn_r101_fpn
  - cascade_mask_rcnn_r101_32x4d_fpn_coco
  - cascade_mask_rcnn_r101_64x4d_fpn_coco
   

<br />
<br />


## Installation

Supports 
- Python 3.6
- Cuda 9.0, 10.0 (Other cuda version support is experimental)
    
`cd installation`

`chmod +x install.sh && ./install.sh`

<br />
<br />
<br />


## Pipeline

- Load Dataset

`gtf.Train_Dataset(img_dir, annofile, class_file);`

`gtf.Dataset_Params(batch_size=2, num_workers=2);`

- Load Model

`gtf.Model_Params(model_name="faster_rcnn_x101_64x4d_fpn");`

- Set Hyper Parameters

`gtf.Hyper_Params(lr=0.02, momentum=0.9, weight_decay=0.0001);`

`gtf.Training_Params(num_epochs=2, val_interval=1);`

- Train

`gtf.Train();`



<br />
<br />
<br />

## TODO

- [x] Add support for Coco-Type Annotated Datasets
- [ ] Add support for VOC-Type Annotated Dataset
- [x] Test on Kaggle and Colab 
- [x] Add validation feature & data pipeline
- [ ] Add Optimizer selection feature
- [ ] Enable Learning-Rate Scheduler Support
- [ ] Enable Layer Freezing
- [ ] Set Verbosity Levels
- [ ] Add Project management and version control support (Similar to Monk Classification)
- [ ] Add Graph Visualization Support
- [ ] Enable batch proessing at inference
- [ ] Add feature for top-k output visualization
- [x] Add Multi-GPU training
- [ ] Auto correct missing or corrupt images - Currently skips them
- [ ] Add Experimental Data Analysis Feature


<br />
<br />
<br />
