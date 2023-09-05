# Diving with Penguins: Detecting Penguins and their Prey in Animal-borne Underwater Videos via Deep Learning
Appear at 3rd International Workshop on Camera Traps, AI and Ecology, September 2023  
Paper Link: [Arxiv PDF](https://arxiv.org/abs/2308.07267)

## Abstract
African penguins (Spheniscus demersus) are an endangered species. Little is known regarding their underwater hunting strategies and associated predation success rates, yet this is essential for guiding conservation. Modern bio-logging technology has the potential to provide valuable insights, but manually analysing large amounts of data from animal-borne video recorders (AVRs) is time-consuming. In this paper, we publish an animal-borne underwater video dataset of penguins and introduce a ready-to-deploy deep learning system capable of robustly detecting penguins (mAP50@98.0%) and instances of fish (mAP50@73.3%). We note that the detectors benefit explicitly from air-bubble learning to improve accuracy. Extending this detector towards a dual-stream behaviour recognition network, we also provide the first results for identifying predation behaviour in penguin underwater videos. Whilst results are promising, further work is required for the useful applicability of predation behaviour detection in field scenarios. In summary, we provide a highly reliable underwater penguin detector, a fish detector, and a valuable first attempt towards automated visual detection of complex behaviours in a marine predator. We publish the networks, the ’DivingWithPenguins’ video dataset, annotations, splits, and weights for full reproducibility and immediate usability by practitioners.

## Dataset
The links to these repositories below contain all the datasets used in this project.

### DATA VIEW A: Penguin Detection in Stills
[Single Frame Object Detection Dataset.](https://github.com/Kejia928/local-detection-dataset) 602 underwater images at a resolution of 640 × 640 pixels with a training portion of 418 images and a test portion of 184 images are designed to be utilised to train an underwater penguin detector. Following the requirements of YOLOv5 standards, this dataset view contains full bounding box annotations for penguins, fish, and bubbles in underwater images.

### DATA VIEW B: Content Classification
[Whole Frame Classification Dataset.](https://github.com/Kejia928/global-detection-dataset) 797 underwater images at a resolution of 640 × 640 pixels with binary classification labels indicating the existence or absence of fish. In this data view, there are 370 images labelled as “Have Fish” and 427 images labelled as “No Fish”. 558 images from the training portion and 239 images from the test portion.

### DATA VIEW C: Behaviour Recognition
[Short Behavioural Video Dataset. The link will be coming soon.....]() 188 predation events are annotated across 85 short videos and stored in a JSON file. Penguin feeding behaviours are fast actions that occur across about ten to twenty frames in the 30fps content. Hence, annotation uses milliseconds to pinpoint events accurately. Training and test instances are provided.

## Code Repo
The code repo below contains everything implemented in this project.

* YOLOv5 - Penguin, Fish, and Bubble Detector: [Github](https://github.com/Kejia928/PenguinDetector)
* ResNet - Whole Frame Fish Classifier: [Github](https://github.com/Kejia928/FishDetector)
* Dual Stream Network - Spatio&Temporal Predation Behaviour Detector: [Github](https://github.com/Kejia928/PredationDetector)

## Visualisation Results

## Author
- **Kejia Zhang:** Department of Computer Science, University of Bristol, Bristol, UK  
- **Mingyu Yang:** Department of Computer Science, University of Bristol, Bristol, UK  
- **Stephen D. J. Lang:** Centre for Ecology and Conservation, University of Exeter, Penryn, Cornwall, UK  
- **Alistair M. McInnes:** BirdLife South Africa, Cape Town, South Africa  
- **Richard B. Sherley:** Centre for Ecology and Conservation, University of Exeter, Penryn, Cornwall, UK  
- [**Tilo Burghardt**](http://people.cs.bris.ac.uk/~burghard/): Department of Computer Science, University of Bristol, Bristol, UK  

E-mail: zhangkejia2019@163.com

## Citation
This project was submitted and presented at the Camera Traps, AI and Ecology workshop. If you want to use this work as part of your research, please cite [Diving with Penguins: Detecting Penguins and their Prey in Animal-borne Underwater Videos via Deep Learning](https://arxiv.org/abs/2308.07267).

```text
@misc{zhang2023diving,
      title={Diving with Penguins: Detecting Penguins and their Prey in Animal-borne Underwater Videos via Deep Learning}, 
      author={Kejia Zhang and Mingyu Yang and Stephen D. J. Lang and Alistair M. McInnes and Richard B. Sherley and Tilo Burghardt},
      year={2023},
      eprint={2308.07267},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

## Acknowledgement
This work utilised the Blue Crystal Phase 4 supercomputer at the University of Bristol, UK. We thank BirdLife South Africa and all the people involved in the data-gathering efforts for their hard work.
