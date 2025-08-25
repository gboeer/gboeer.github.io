---
layout: publications
permalink: /publications/
title: Scientific Publications
tags: [Publications, Research, Science]
---

<p>Below is a selection of my scientific publications. Each entry includes the abstract and a BibTeX citation for reference.</p>

<h2>First Author Publications</h2>

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
    <h3>Semantic Segmentation of Marine Species in an Unconstrained Underwater Environment</h3>
    <p><strong>Authors:</strong> Böer, Gordon Böer and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> Robotics, Computer Vision and Intelligent Systems: First International Conference, ROBOVIS 2020, Virtual Event, November 4-6, 2020, and Second International Conference, ROBOVIS 2021, Virtual Event, October 27-28, 2021, Revised Selected Papers</p>
    <p><strong>DOI:</strong> <a href="https://link.springer.com/chapter/10.1007/978-3-031-19650-8_7" target="_blank">https://link.springer.com/chapter/10.1007/978-3-031-19650-8_7</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        A non-invasive Underwater Fish Observatory (UFO) was developed and deployed on the seafloor to perform continuous recording of stereo video and sonar data as well as various oceanic parameters at a high temporal sampling rate. The acquired image data is processed to automatically detect, classify and measure the size of passing aquatic organisms. An important subtask in this pro-cessing chain is the semantic segmentation of the previously detected animals. Within this publication, a former segmentation system, that only considered a binary classification of fish and background, is extended to a multi-class seg-mentation system by including an additional species. Since the images usually contain a lot of background, the semantic segmentation is a problem with a high class imbalance, which demands special care in the choice of loss functions and evaluation metrics. Therefore, three different loss functions, namely Dice loss, Focal loss and Lovasz loss, which are well suited for class-imbalance problems, are investigated and their effect on the final mean intersection-over-union (IoU) on a separate test set is explored. For the given dataset, the model trained with a Focal loss performed best achieving an average, class specific IoU of 0.982 for the background class, 0.828 for the Aurelia aurita and 0.678 for the Gadus morhua.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{boer2022semantic,
  title={Semantic Segmentation of Marine Species},
  author={B{\"o}er, Gordon and Schramm, Hauke},
  booktitle={Robotics, Computer Vision and Intelligent Systems: First International Conference, ROBOVIS 2020, Virtual Event, November 4-6, 2020, and Second International Conference, ROBOVIS 2021, Virtual Event, October 27-28, 2021, Revised Selected Papers},
  pages={131},
  year={2022},
  organization={Springer Nature}
}
 </pre>
</details>
</div>

<div class="publication-entry">
    <h3>Segmentation of Fish in Realistic Underwater Scenes using Lightweight Deep Learning Models</h3>
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

<div class="publication-entry">
    <h3>Detection of Facial Landmarks in 3D Face Scans Using the Discriminative Generalized Hough Transform (DGHT)</h3>
    <p><strong>Authors:</strong> Böer, Gordon and Hahmann, Ferdinand and Buhr, Ines and Essig, Harald and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> Bildverarbeitung für die Medizin 2015: Algorithmen-Systeme-Anwendungen. Proceedings des Workshops vom 15. bis 17. März 2015 in Lübeck (pp. 299-304)</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.1007/978-3-662-46224-9_52" target="_blank">https://doi.org/10.1007/978-3-662-46224-9_52</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        This paper presents the Discriminative Generalized Hough Transform (DGHT) as a technique to localize landmarks in 3D face scans. While the DGHT has been successfully used for the detection of landmarks in 2D and 3D images this work extends the framework to be used with triangle meshes for the first time. Instead of edge features and their respective gradient direction, the relative positions and orientations of the mesh faces are utilized to describe the geometric structures which are relevant for the detection of a specific landmark. Implementing a coarse-to-fine strategy at first a decimated version of the mesh is used to locate the global region of the point of interest, followed by more detailed localizations on higher resolution meshes. The utilized shape models are created in an automated, discriminative training process which assigns individual weights to the single model points, aiming at an increased localization rate. The technique has been applied to detect 38 anthropometric facial landmarks on 99 3D face scans. With an average error of 1.9mm, the most accurate detection was performed for the right alare, the average error when considering all landmarks amounts to 5.1 mm.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{boer2015detection,
  title={Detection of Facial Landmarks in 3D Face Scans Using the Discriminative Generalized Hough Transform (DGHT)},
  author={B{\"o}er, Gordon and Hahmann, Ferdinand and Buhr, Ines and Essig, Harald and Schramm, Hauke},
  booktitle={Bildverarbeitung f{\"u}r die Medizin 2015: Algorithmen-Systeme-Anwendungen. Proceedings des Workshops vom 15. bis 17. M{\"a}rz 2015 in L{\"u}beck},
  pages={299--304},
  year={2015},
  organization={Springer}
}
 </pre>

    </details>
    </div>

</div>

<h2>Co-Author Publications</h2>

<div class="publications-list">

<div class="publication-entry">
    <h3>Development and operation of a novel non-invasive opto-acoustic underwater fish observatory in Kiel Bight, Southwestern Baltic Sea</h3>
    <p><strong>Authors:</strong> Gröger, Joachim P.  and Cisewski, Boris  and Badri-Hoeher, Sabah  and Böer, Gordon  and Boos, Karin  and Clemmesen, Catriona  and Cojocaru, Ala  and Dauben, Verena  and Hoeher, Peter A.  and Lehmann, Andreas  and Matz, Sebastian  and Mehrtens, Hela  and Mittermayer, Felix  and Renkewitz, Helge  and Schramm, Hauke  and Strickmann, Tobias  and Westphalen, Jonni  and Wilts, Thomas  and Winkler, Julian  and Wolf, Dennis  and Zenk, Oliver</p>
    <p><strong>Journal/Conference:</strong> Frontiers in Marine Science 11 (2024): 1425259</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.3389/fmars.2024.1425259" target="_blank">https://doi.org/10.3389/fmars.2024.1425259</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        This study presents a trilateral test array of new opto-acoustic Underwater Fish Observatories (UFOs) that were operated and tested in Kiel Bight as part of the "UFOTriNet" project. While hydroacoustic and optical techniques have so far been used individually to observe and monitor fish stocks, we present a coupled hybrid system consisting of an optical device intended to scan the near-field as a subsample of a spatially larger medium-to-far-field, scanned by an acoustical device. The optical device consists of two residual light amplifying camera modules able to detect and classify various marine species at a high resolution in the range of at max 4 meters in the study area. To compensate for this spatial limitation, the acoustical component consists of a 2D imaging sonar with a maximum range of 50 m, albeit with a lower resolution. Species affiliation, morphometric characteristics of fish and other marine organisms were stereo-optically detected and classified in the nearfield, blended with acoustical activity in medium to far range, and projected onto the entire insonified area using a hybrid algorithm. Through the synchronous acquisition of multiparametric abiotic and biotic data, UFO allows an automatic, continuous, and non-invasive long-term monitoring of various fish and other marine species and their habitats at regional hotspots. An 86-day multiparametric sample revealing an abrupt shift from a clupeid fish to a gelatinous plankton dominated regime in summer / autumn 2021 in Kiel Fjord is used to demonstrate the potential of UFO for various applications.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@article{groger2024development,
  title={Development and operation of a novel non-invasive opto-acoustic underwater fish observatory in Kiel Bight, Southwestern Baltic Sea},
  author={Gr{\"o}ger, Joachim P and Cisewski, Boris and Badri-Hoeher, Sabah and B{\"o}er, Gordon and Boos, Karin and Clemmesen, Catriona and Cojocaru, Ala and Dauben, Verena and Hoeher, Peter A and Lehmann, Andreas and others},
  journal={Frontiers in Marine Science},
  volume={11},
  pages={1425259},
  year={2024},
  publisher={Frontiers Media SA}
}
 </pre>
</details>
</div>

<div class="publication-entry">
    <h3>Self-attention and generative adversarial networks for algae monitoring</h3>
    <p><strong>Authors:</strong> Huynh, Nhut Hai and Böer, Gordon and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> European Journal of Remote Sensing 55.1 (2022): 10-22.</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.1080/22797254.2021.2010605" target="_blank">https://doi.org/10.1080/22797254.2021.2010605</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        Water is important for the natural environment and human health. Monitoring algae concentrations yield information on the water quality. Compared with in situ measurements of water quality parameters, which are often complex and expensive, remote sensing techniques, using hyperspectral data analysis, are fast and cost-effective. The objectives of this study are (1) to estimate the algae concentrations from hyperspectral data using deep learning techniques, (2) to investigate the applicability of attention mechanisms in the analysis of hyperspectral data, and (3) to augment the training data using generative adversarial networks (GANs). The results show that the accuracy of deep learning techniques is 7.6% higher than that of simpler artificial neural networks. Compared to noise injection and principal component analysis-based data augmentation, the use of a GAN-based data augmentation method significantly improves the accuracy of algae concentration estimates (>5%). In addition, models with added attention mechanisms yield an on average 3.13% higher accuracy than those without attention techniques. This result demonstrates the improvement of spectral features of artificial hyperspectral data based on the self-attention approach, revealing the potential of attention techniques in hyperspectral remote sensing.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@article{huynh2022self,
  title={Self-attention and generative adversarial networks for algae monitoring},
  author={Huynh, Nhut Hai and B{\"o}er, Gordon and Schramm, Hauke},
  journal={European Journal of Remote Sensing},
  volume={55},
  number={1},
  pages={10--22},
  year={2022},
  publisher={Taylor \& Francis}
}
 </pre>

    </details>
    </div>



<div class="publication-entry">
    <h3>Classification of voting patterns to improve the generalized Hough transform for epiphyses localization</h3>
    <p><strong>Authors:</strong> Hahmann, Ferdinand and Böer, Gordon and Gabriel, Eric and Deserno, Thomas M and Meyer, Carsten and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> Medical Imaging 2016: Computer-Aided Diagnosis (Vol. 9785, pp. 47-57)</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.1117/12.2216173" target="_blank">https://doi.org/10.1117/12.2216173</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        This paper presents a general framework for object localization in medical (and non-medical) images. In particular, we focus on objects of well-defined shape, like epiphyseal regions in hand-radiographs, which are localized based on a voting framework using the Generalized Hough Transform (GHT). We suggest to combine the GHT voting with a classifier which rates the voting characteristics of the GHT model at individual Hough cells. Specifically, a Random Forest Classifier rates whether the model points, voting for an object position, constitute a regular shape or not, and this measure is combined with the GHT votes. With this technique, we achieve a success rate of 99.4% for localizing 12 epiphyseal regions of interest in 412 hand- radiographs. The mean error is 6.6 pixels on images with a mean resolution of 1185×2006 pixels. Furthermore, we analyze the influence of the radius of the local neighborhood which is considered in analyzing the voting characteristics of a Hough cell.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{hahmann2016classification,
  title={Classification of voting patterns to improve the generalized Hough transform for epiphyses localization},
  author={Hahmann, Ferdinand and B{\"o}er, Gordon and Gabriel, Eric and Deserno, Thomas M and Meyer, Carsten and Schramm, Hauke},
  booktitle={Medical Imaging 2016: Computer-Aided Diagnosis},
  volume={9785},
  pages={47--57},
  year={2016},
  organization={SPIE}
}
 </pre>

    </details>
    </div>

<div class="publication-entry">
    <h3>Structured edge detection for improved object localization using the discriminative generalized Hough transform</h3>
    <p><strong>Authors:</strong> Gabriel, Eric and Hahmann, Ferdinand and Böer, Gordon and Schramm, Hauke and Meyer, Carsten</p>
    <p><strong>Journal/Conference:</strong> International Conference on Computer Vision Theory and Applications (Vol. 5, pp. 393-402).</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.5220/0005722803930402" target="_blank">https://doi.org/10.5220/0005722803930402</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        Automatic localization of target objects in digital images is an important task in Computer Vision. The Generalized Hough Transform (GHT) and its variant, the Discriminative Generalized Hough Transform (DGHT), are model-based object localization algorithms which determine the most likely object position based on accumulated votes in the so-called Hough space. Many automatic localization algorithms - including the GHT and the DGHT - operate on edge images, using e.g. the Canny or the Sobel Edge Detector. However, if the image contains many edges not belonging to the object of interest (e.g. from other objects, background clutter, noise etc.), these edges cause misleading votes which increase the probability of localization errors. In this paper we investigate the effect of a more sophisticated edge detection algorithm, called Structured Edge Detector, on the performance of a DGHT-based object localization approach. This method utilizes information on the shape of the target object to substantially reduce the amount of non-object edges. Combining this technique with the DGHT leads to a significant localization performance improvement for automatic pedestrian and car detection.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{gabriel2016structured,
  title={Structured edge detection for improved object localization using the discriminative generalized Hough transform},
  author={Gabriel, Eric and Hahmann, Ferdinand and B{\"o}er, Gordon and Schramm, Hauke and Meyer, Carsten},
  booktitle={International Conference on Computer Vision Theory and Applications},
  volume={5},
  pages={393--402},
  year={2016},
  organization={SCITEPRESS}
}
 </pre>

    </details>
    </div>



<div class="publication-entry">
    <h3>A shape consistency measure for improving the generalized Hough transform</h3>
    <p><strong>Authors:</strong> Hahmann, Ferdinand and Böer, Gordon and Gabriel, Eric and Meyer, Carsten and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> Proceedings VISAPP (2015)</p>
    <p><strong>URL:</strong> <a href="http://fhahmann.de/onewebmedia/papers/visapp2015.pdf" target="_blank">http://fhahmann.de/onewebmedia/papers/visapp2015.pdf</a></p>
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        The Discriminative Generalized Hough Transform (DGHT) is a general object localization approach. Based on a training corpus with annotated target point locations it employs a discriminative training technique to generate weighted shape models for usage in a standard GHT voting procedure. The method has shown to successfully cover medium target object variability by aggregating model points, representing the different variants, in a single model. However, due to the independent treatment of model points in the GHT voting, mutually exclusive variations may support the same localization hypothesis, leading to false positives. The problem is addressed by analyzing the spatial pattern of model points, voting for a specific Hough cell, and learning the structural differences between successful and unsuccessful localizations. Random Forests are utilized to rate the regularity of model point patterns to provide the probability of a “regular shape”, indicating a successful localization. The approach is evaluated on a public corpus containing 3830 portrait images with strong head pose variation with a localization success rate of 99.2% for the iris of both eyes. This is an improvement of 2% compared to the DGHT baseline system which demonstrates the potential of the novel method to eliminatve an important source of mislocalizations.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@article{hahmann2015shape,
  title={A shape consistency measure for improving the generalized Hough transform},
  author={Hahmann, Ferdinand and B{\"o}er, Gordon and Gabriel, Eric and Meyer, Carsten and Schramm, Hauke},
  journal={Proc. VISAPP},
  year={2015}
}
 </pre>

    </details>
    </div>

<div class="publication-entry">
    <h3>Epiphyses localization for bone age assessment using the discriminative generalized hough transform</h3>
    <p><strong>Authors:</strong> Hahmann, Ferdinand and Böer, Gordon and Deserno, Thomas M and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> Bildverarbeitung für die Medizin 2014: Algorithmen-Systeme-Anwendungen Proceedings des Workshops vom 16. bis 18. März 2014 in Aachen</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.1007/978-3-642-54111-7_17" target="_blank">https://doi.org/10.1007/978-3-642-54111-7_17</a></p>
    
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        This paper presents the Discriminative Generalized Hough Transform (DGHT) as a robust and accurate method for the localization of epiphyseal regions in radiographs of the left hand. The technique utilizes a discriminative training approach to generate shape models with individual positive and negative model point weights for the Generalized Hough Transform. The framework incorporates a multi-level approach which reduces the searched region in two zooming steps, using specifically trained DGHT shape models. In addition to the standard method, a novel landmark combination approach is presented. Here, the N-best lists of individual landmark localizations are combined with anatomical constraints to achieve a globally optimal localization result for all 12 considered epiphyseal regions of interest. The technique has been applied to extract 12 epiphyseal regions of interest for a subsequent automatic bone age assessment. It achieved a localization success rate of 98.1% on a corpus with 412 left hand radiographs covering the age range from 3 to 19 years.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{hahmann2014epiphyses,
  title={Epiphyses localization for bone age assessment using the discriminative generalized hough transform},
  author={Hahmann, Ferdinand and B{\"o}er, Gordon and Deserno, Thomas M and Schramm, Hauke},
  booktitle={Bildverarbeitung f{\"u}r die Medizin 2014: Algorithmen-Systeme-Anwendungen Proceedings des Workshops vom 16. bis 18. M{\"a}rz 2014 in Aachen},
  pages={66--71},
  year={2014},
  organization={Springer}
}
 </pre>

    </details>
    </div>

<div class="publication-entry">
    <h3>Combination of facial landmarks for robust eye localization using the Discriminative Generalized Hough Transform</h3>
    <p><strong>Authors:</strong> Hahmann, Ferdinand and Böer, Gordon and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> International Conference of the BIOSIG Special Interest Group (BIOSIG). IEEE, 2013.</p>
    <p><strong>URL:</strong> <a href="https://cs.emis.de/LNI/Proceedings/Proceedings196/159.pdf" target="_blank">https://cs.emis.de/LNI/Proceedings/Proceedings196/159.pdf</a></p>
    
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        The Discriminative Generalized Hough Transform (DGHT) is a general and robust automated object localization method, which has been shown to achieve state-of-the-art success rates in different application areas like medical image analysis and person localization. In this contribution the framework is enhanced by a novel fa-ciallandmark combination technique which is theoretically introduced and evaluated for an eye localization task on a public database. The technique applies individually trained DGHT models for the localization of different facial landmarks, combines the obtained Hough spaces into a 3D feature matrix and applies a specifically trained higher-level DGHT model for the final localization based on the given features. In addition to that, the framework is further improved by a task-specific multi-level approach which adjusts the zooming-in strategy with respect to relevant structures and confusable objects. With the new system it was possible to increase the iris localization rate from 96.6% to 97.9% on 3830 evaluation images. This result is promising, since the variation of the head pose in the database is quite large and the applied error measure considers the worst of a left and right eye localization attempt.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{hahmann2013combination,
  title={Combination of facial landmarks for robust eye localization using the Discriminative Generalized Hough Transform},
  author={Hahmann, Ferdinand and B{\"o}er, Gordon and Schramm, Hauke},
  booktitle={2013 International Conference of the BIOSIG Special Interest Group (BIOSIG)},
  pages={1--12},
  year={2013},
  organization={IEEE}
}
 </pre>

    </details>
    </div>

<div class="publication-entry">
    <h3>Model interpolation for eye localization using the Discriminative Generalized Hough Transform</h3>
    <p><strong>Authors:</strong> Hahmann, Ferdinand and Ruppertshofen, Heike and Böer, Gordon and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> 2012 BIOSIG-Proceedings of the International Conference of Biometrics Special Interest Group (BIOSIG). IEEE, 2012.</p>
    <p><strong>URL:</strong> <a href="https://ieeexplore.ieee.org/abstract/document/6313546" target="_blank">https://ieeexplore.ieee.org/abstract/document/6313546</a></p>
    
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        The Discriminative Generalized Hough Transform (DGHT) is a general method for the localization of arbitrary objects with well-defined shape, which has been successfully applied in medical image processing. In this contribution, the framework is used for eye localization in the public PUT face database. The DGHT combines the Generalized Hough Transform (GHT) with a discriminative training procedure to generate GHT shape models with individual positive and negative model point weights. Based on a set of training images with annotated target points, the individual votes of model points in the Hough space are combined in a maximum-entropy probability distribution and the free parameters are optimized with respect to the training error rate. The estimated model point specific weights reflect the important model structures to distinguish the target object from other confusable image parts. Additionally, the point weights allow for a determination of irrelevant parts in the model, which can be eliminated to make space for new model point candidates from training images with high localization error. The iterative training procedure of weight estimation, point elimination, testing on training images, and incorporation of new model point candidates is repeated until a stopping criterion is reached. Furthermore, the DGHT framework incorporates a multi-level approach, in which the searched region is reduced in 6 zooming steps, using individually trained shape models. In order to further enhance the robustness of the method, the DGHT framework is, for the first time, extended by a linear model interpolation for the trained left and right eye model. An evaluation on the PUT face database has shown a success rate of 99% for iris detection in frontal-view images and 97% if the test set contains a large head pose variability.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{hahmann2012model,
  title={Model interpolation for eye localization using the Discriminative Generalized Hough Transform},
  author={Hahmann, Ferdinand and Ruppertshofen, Heike and B{\"o}er, Gordon and Schramm, Hauke},
  booktitle={2012 BIOSIG-Proceedings of the International Conference of Biometrics Special Interest Group (BIOSIG)},
  pages={1--12},
  year={2012},
  organization={IEEE}
}
 </pre>

    </details>
    </div>

<div class="publication-entry">
    <h3>Eye localization using the discriminative generalized hough transform</h3>
    <p><strong>Authors:</strong> Hahmann, Ferdinand and Ruppertshofen, Heike and Böer, Gordon and Stannarius, Ralf and Schramm, Hauke</p>
    <p><strong>Journal/Conference:</strong> Joint DAGM (German Association for Pattern Recognition) and OAGM Symposium (pp. 155-164). Berlin, Heidelberg: Springer Berlin Heidelberg.</p>
    <p><strong>DOI:</strong> <a href="https://doi.org/10.1007/978-3-642-32717-9_16" target="_blank">https://doi.org/10.1007/978-3-642-32717-9_16</a></p>
    
    <details>
      <summary><strong>Abstract</strong></summary>
      <p>
        The Discriminative Generalized Hough Transform (DGHT) has been successfully introduced as a general method for the localization of arbitrary objects with well-defined shape in medical images. In this contribution, the framework is, for the first time, applied to the localization of eyes in a public face database. Based on a set of training images with annotated target points, the training procedure combines the Hough space votes of individual shape model points into a probability distribution of the maximum-entropy family and optimizes the free parameters of this distribution with respect to the training error rate. This assigns individual positive and negative weights to the shape model points, reflecting important structures of the target object and confusable shapes, respectively. Additionally, the estimated weights allow to determine irrelevant parts in order to eliminate them from the model, making space for the incorporation of new model point candidates. These candidates are in turn identified from training images with remaining high localization error. The whole procedure of weight estimation, point elimination, testing on training images and incorporation of new model point hypotheses is iterated several times until a stopping criterion is met. The method is further enhanced by applying a multi-level approach, in which the searched region is reduced in 6 zooming steps, using individually trained shape models on each level. An evaluation on the PUT face database has shown that the system achieves a state-of-the-art success rate of 99% for iris detection in frontal-view images and 95% if the test set contains the full head pose variability.
      </p>
    </details>
    <details>
      <summary><strong>BibTeX Citation</strong></summary>
      <pre>
@inproceedings{hahmann2012eye,
  title={Eye localization using the discriminative generalized hough transform},
  author={Hahmann, Ferdinand and Ruppertshofen, Heike and B{\"o}er, Gordon and Stannarius, Ralf and Schramm, Hauke},
  booktitle={Joint DAGM (German Association for Pattern Recognition) and OAGM Symposium},
  pages={155--164},
  year={2012},
  organization={Springer}
}
 </pre>

    </details>
    </div>

  <!-- Add more publication entries below -->
</div>
