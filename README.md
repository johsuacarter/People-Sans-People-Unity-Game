# PeopleSansPeople: A Synthetic Data Generator for Human-Centric Computer Vision, [NeurIPS 2021](https://arxiv.org/abs/3940169)

<!-- Global site tag (gtag.js) - Google Analytics -->
<!--
<script async src="https://www.googletagmanager.com/gtag/js?id=G-ZCKG4HKTMK"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-ZCKG4HKTMK');
</script>
-->

<img src="./images/unity/unity-wide-whiteback.png" align="middle" width="3000"/>

[![license badge](https://img.shields.io/badge/license-Apache--2.0-green.svg)](LICENSE.md)

<img src="https://img.shields.io/badge/unity-2020.1.17f1-green.svg?style=flat-square" alt="unity 2020.1.17f1">

<p align="center">
  <img src="./images/teaser_images/rgb_1528.png" width="20%" />

  <img src="./images/teaser_images/rgb_2711.png" width="20%" />

  <img src="./images/teaser_images/rgb_8687.png" width="20%" />
</p>
<p align="center">
  <img src="./images/teaser_images/img__anns__1528.png" width="20%" />

  <img src="./images/teaser_images/img__anns__2711.png" width="20%" />

  <img src="./images/teaser_images/img__anns__8687.png" width="20%" />
</p>

<!--
 &nbsp; &nbsp;
-->

<p align="center">
  <a href="https://scholar.google.com/citations?hl=en&user=umudhIEAAAAJ">Salehe Erfanian Ebadi</a>,
  <a href="https://www.linkedin.com/in/ycjhang">You-Cyuan Jhang</a>, 
  <a href="https://scholar.google.com/citations?user=2nA9bVMAAAAJ&hl=en&oi=ao">Alex Zook</a>, 
  <a href="https://www.linkedin.com/in/sauravdhakad/">Saurav Dhakad</a>, 
  <br>
  <a href="https://www.linkedin.com/in/adam-crespi-81b1287">Adam Crespi</a>,
  <a href="https://www.linkedin.com/in/pete-parisi-81a179">Pete Parisi</a>,
  <a href="https://www.linkedin.com/in/steve-borkman-5983325">Steven Borkman</a>,
  <a href="https://www.linkedin.com/in/jonathan-hogins-1952b919">Jonathan Hogins</a>,
  <a href="https://scholar.google.com/citations?hl=en&user=4XuOFfUAAAAJ">Sujoy Ganguly</a>
  <br>
  Unity Technologies
</p>

<!--
> **Authors:** Salehe Erfanian Ebadi, You-Cyuan Jhang, Alex Zook, Saurav Dhakad, Adam Crespi, Pete Parisi, Steven Borkman, Jonathan Hogins, Sujoy Ganguly
> <br />
> **Authors' affiliation:** Unity Technologies
> <br />
> **Submitted to:** NeurIPS 2021 Track Datasets and Benchmarks Round2
> <br />
> **Paper ID:** 54
-->

## Summary
* We introduce PeopleSansPeople, a human-centric privacy-preserving synthetic data generator with highly parametrized domain randomization.
* PeopleSansPeople contains simulation-ready 3D human assets, a parameterized lighting and camera system, and generates 2D and 3D bounding box, 
instance and semantic segmentation, and COCO pose labels. 
* We use naïve ranges for the domain randomization and generate a synthetic dataset with labels. 
* We provide some guarantees and analysis of human activities, poses, and context diversity on our synthetic data.
* We found that pre-training a network using synthetic data and fine-tuning on target real-world data 
([COCO-person train](https://cocodataset.org/#home)) resulted in bbox AP of **57.44** and keypoint AP of **66.83** 
(COCO-person validation) outperforming models trained with the same real data alone (bbox AP of **56.73** and keypoint AP of **65.12**).

<details>
  <summary>Abstract</summary>
  
*In recent years, person detection and human pose estimation have made great strides, helped by large-scale labeled datasets. 
However, these datasets had no guarantees or analysis of human activities, poses, or context diversity. 
Additionally, privacy concerns may limit the ability to collect more data. 
An emerging alternative to real-world data that alleviates some of these issues is synthetic data. 
However, creation of synthetic data generators is incredibly challenging and prevents researchers from exploring their usefulness.
Therefore, we release a human-centric synthetic data generator PeopleSansPeople which contains simulation-ready 3D human assets, 
a parameterized lighting and camera system, and generates 2D and 3D bounding box, instance and semantic segmentation, and COCO pose labels. 
Using PeopleSansPeople, we performed benchmark synthetic data training using a 
[Detectron2 Keypont R-CNN variant](https://github.com/facebookresearch/detectron2). 
We found that pre-training a network using synthetic data and fine-tuning on target real-world data 
([COCO-person train](https://cocodataset.org/#home)) resulted in bbox AP of **57.44** and keypoint AP of **66.83** 
(COCO-person validation) outperforming models trained with the same real data alone (bbox AP of **56.73** and keypoint AP of **65.12**).
This freely available data generator should enable a wide range of research into the emerging field of simulation to 
real transfer learning in the critical area of human-centric computer vision.*
</details>

## Generated Data and Labels
PeopleSansPeople produces the following types of labels in COCO format: 2D bounding box, human keypoints, semantic and instance segmentation masks.
In addition PeopleSansPeople generates 3D bounding boxes which are provided in [Unity's Perception](https://github.com/Unity-Technologies/com.unity.perception) format.
<p align="center">
  <img src="./images/label_fig/1.png" width="20%" />

  <img src="./images/label_fig/2.png" width="20%" />

  <img src="./images/label_fig/3.png" width="20%" />
  
  <img src="./images/label_fig/4.png" width="20%" />
</p>

## Additional Examples
<p align="center">
  <img src="./images/more_examples/rgb_100.png" width="12%" />

  <img src="./images/more_examples/rgb_159.png" width="12%" />

  <img src="./images/more_examples/rgb_168.png" width="12%" />
  
  <img src="./images/more_examples/rgb_392.png" width="12%" />
  
  <img src="./images/more_examples/rgb_582.png" width="12%" />
  
  <img src="./images/more_examples/rgb_801.png" width="12%" /> 
</p>
<p align="center">
  <img src="./images/more_examples/rgb_978.png" width="12%" />

  <img src="./images/more_examples/rgb_1281.png" width="12%" />

  <img src="./images/more_examples/rgb_1462.png" width="12%" />
  
  <img src="./images/more_examples/rgb_2178.png" width="12%" />
  
  <img src="./images/more_examples/rgb_2243.png" width="12%" />
  
  <img src="./images/more_examples/rgb_2291.png" width="12%" /> 
</p>
<p align="center">
  <img src="./images/more_examples/rgb_2881.png" width="12%" />

  <img src="./images/more_examples/rgb_3099.png" width="12%" />

  <img src="./images/more_examples/rgb_3335.png" width="12%" />
  
  <img src="./images/more_examples/rgb_3877.png" width="12%" />
  
  <img src="./images/more_examples/rgb_4257.png" width="12%" />
  
  <img src="./images/more_examples/rgb_4531.png" width="12%" /> 
</p>
<p align="center">
  <img src="./images/more_examples/rgb_5420.png" width="12%" />

  <img src="./images/more_examples/rgb_5789.png" width="12%" />

  <img src="./images/more_examples/rgb_5935.png" width="12%" />
  
  <img src="./images/more_examples/rgb_5944.png" width="12%" />
  
  <img src="./images/more_examples/rgb_6339.png" width="12%" />
  
  <img src="./images/more_examples/rgb_6352.png" width="12%" /> 
</p>
<p align="center">
  <img src="./images/more_examples/rgb_7491.png" width="12%" />

  <img src="./images/more_examples/rgb_7638.png" width="12%" />

  <img src="./images/more_examples/rgb_7763.png" width="12%" />
  
  <img src="./images/more_examples/rgb_8023.png" width="12%" />
  
  <img src="./images/more_examples/rgb_8867.png" width="12%" />
  
  <img src="./images/more_examples/rgb_8981.png" width="12%" /> 
</p>
<p align="center">
  <img src="./images/more_examples/rgb_9265.png" width="12%" />

  <img src="./images/more_examples/rgb_9383.png" width="12%" />

  <img src="./images/more_examples/rgb_9471.png" width="12%" />
  
  <img src="./images/more_examples/rgb_9480.png" width="12%" />
  
  <img src="./images/more_examples/rgb_9591.png" width="12%" />
  
  <img src="./images/more_examples/rgb_9983.png" width="12%" /> 
</p>



## Citation
```
@article{ebadi2021peoplesanspeople,
    title={PeopleSansPeople: A Synthetic Data Generator for Human-Centric Computer Vision},
    author={Salehe Erfanian Ebadi and You-Cyuan Jhang and Alex Zook and Saurav Dhakad 
            and Adam Crespi and Pete Parisi and Steven Borkman and Jonathan Hogins and Sujoy Ganguly},
    journal={arXiv},
    year={2021}
}
```

## Source code
Code is available [here](<https://github.com/Unity-Technologies/PeopleSansPeople/>)

## Related links
- [Unity's Perception Package](https://github.com/Unity-Technologies/com.unity.perception)
- [Unity Computer Vision](https://unity.com/products/computer-vision)
- [Unity's Perception Tutorial](https://github.com/Unity-Technologies/com.unity.perception/blob/master/com.unity.perception/Documentation~/Tutorial/TUTORIAL.md)
- [Unity's Human Pose Labeling and Randomization Tutorial](https://github.com/Unity-Technologies/com.unity.perception/blob/master/com.unity.perception/Documentation~/HPTutorial/TUTORIAL.md)
- [SynthDet Project](https://github.com/Unity-Technologies/SynthDet)
- [Robotics Object Pose Estimation Demo](https://github.com/Unity-Technologies/Robotics-Object-Pose-Estimation)
- [Unity Simulation Smart Camera Outdoor Example](https://github.com/Unity-Technologies/Unity-Simulation-Smart-Camera-Outdoor)


## License

PeopleSansPeople is licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE.md) for the full license text.
