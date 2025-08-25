---
layout: publications
permalink: /publications/
title: Scientific Publications
tags: [Publications, Research, Science]
---

<p>Below is a selection of my scientific publications. Each entry includes the abstract and a BibTeX citation for reference.</p>

<div class="publications-list">
  <div class="publication-entry">
    <h3>A Deep-Learning Based Pipeline for Estimating the Abundance and Size of Aquatic Organisms in an Unconstrained Underwater Environment from Continuously Captured Stereo Video</h3>
    <p><strong>Authors:</strong> Böer, G.; Gröger, J.P.; Badri-Höher, S.; Cisewski, B.; Renkewitz, H.; Mittermayer, F.; Strickmann, T.; Schramm, H.</p>
    <p><strong>Journal/Conference:</strong> Sensors 2023, 23, 3311</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.3390/s23063311" target="_blank">https://doi.org/10.3390/s23063311</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        The utilization of stationary underwater cameras is a modern and well-adapted approach to provide a continuous and cost-effective long-term solution to monitor underwater habitats of particular interest. A common goal of such monitoring systems is to gain better insight into the dynamics and condition of populations of various marine organisms, such as migratory or commercially relevant fish taxa. This paper describes a complete processing pipeline to automatically determine the abundance, type and estimate the size of biological taxa from stereoscopic video data captured by the stereo camera of a stationary Underwater Fish Observatory (UFO). A calibration of the recording system was carried out in situ and, afterward, validated using the synchronously recorded sonar data. The video data were recorded continuously for nearly one year in the Kiel Fjord, an inlet of the Baltic Sea in northern Germany. It shows underwater organisms in their natural behavior, as passive low-light cameras were used instead of active lighting to dampen attraction effects and allow for the least invasive recording possible. The recorded raw data are pre-filtered by an adaptive background estimation to extract sequences with activity, which are then processed by a deep detection network, i.e., Yolov5. This provides the location and type of organisms detected in each video frame of both cameras, which are used to calculate stereo correspondences following a basic matching scheme. In a subsequent step, the size and distance of the depicted organisms are approximated using the corner coordinates of the matched bounding boxes. The Yolov5 model employed in this study was trained on a novel dataset comprising 73,144 images and 92,899 bounding box annotations for 10 categories of marine animals. The model achieved a mean detection accuracy of 92.4%, a mean average precision (mAP) of 94.8% and an F1 score of 93%.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@article{boer2023deep,
  title={A deep-learning based pipeline for estimating the abundance and size of aquatic organisms in an unconstrained underwater environment from continuously captured stereo video},
  author={B{\"o}er, Gordon and Gr{\"o}ger, Joachim Paul and Badri-H{\"o}her, Sabah and Cisewski, Boris and Renkewitz, Helge and Mittermayer, Felix and Strickmann, Tobias and Schramm, Hauke},
  journal={Sensors},
  volume={23},
  number={6},
  pages={3311},
  year={2023},
  publisher={MDPI}
}
 </pre>

    </details>
    </div>

<div class="publication-entry">
    <h3>Segmentation of Fish in Realistic Underwater Scenes using Lightweight Deep Learning Models.</h3>
    <p><strong>Authors:</strong> Böer, Gordon and Veeramalli, Rajesh and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> ROBOVIS 2021 (pp. 158-164)</p>
    <p><strong>DOI:</strong> <a href="http://dx.doi.org/10.5220/0010712700003061" target="_blank">http://dx.doi.org/10.5220/0010712700003061</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        The semantic segmentation of fish in real underwater scenes is a challenging task and an important prerequisite for various processing steps. With a good segmentation result, it becomes possible to automatically extract the fish contour and derive morphological features, both of which can be used for species identification and fish biomass assessment. In this work, two deep learning models, DeepLabV3 and PSPNet, are investigated for their applicability to fish segmentation for a fish stock monitoring application with low light cameras. By pruning these networks and employing a different encoder, they become more suitable for systems with limited hardware, such as remotely operated or autonomously operated underwater vehicles. Both segmentation models are trained and evaluated on a novel dataset of underwater images showing Gadus morhua in its natural behavior. On a challenging test set, which includes fish recorded at difficult visibility conditions, the PSPNet performs best, and achieves an average pixel accuracy of 96.8% and an intersection-over-union between the predicted and the target mask of 73.8%. It achieves this with a very limited parameter set of 94,393 trainable parameters.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{boer2021segmentation,
  title={Segmentation of Fish in Realistic Underwater Scenes using Lightweight Deep Learning Models.},
  author={B{\"o}er, Gordon and Veeramalli, Rajesh and Schramm, Hauke},
  booktitle={ROBOVIS},
  pages={158--164},
  year={2021}
}
 </pre>

    </details>
    </div>

  <!-- Add more publication entries below -->
</div>
