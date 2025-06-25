#---
#title: "Understanding YOLO: Exploring the Evolution of Object Detection Frameworks"
#date: 2024-12-12
#description: "A deep dive into YOLO (You Only Look Once), its various versions, implementations, and licenses. Learn which versions are suitable for commercial use and well-maintained."
#tags: ["YOLO", "Object Detection", "Computer Vision", "Deep Learning"]
#---

# DRAFT DRAFT DRAFT DRAFT


# YOLO: A Journey Through Its Versions

Object detection is one of the most exciting tasks in computer vision, and **YOLO (You Only Look Once)** has been at the forefront of this domain for years. YOLO is known for its real-time object detection capabilities, simplicity, and speed, which makes it ideal for many applications, from self-driving cars to video surveillance systems. Over time, several versions and forks of YOLO have emerged, each offering improvements and trade-offs. However, with so many versions and implementations, finding the right one for your project, especially for commercial use, can be overwhelming.

In this blog post, we'll explore:

1. What makes YOLO unique.
2. The evolution of YOLO, highlighting key features of each version.
3. A comprehensive list of YOLO versions, their GitHub implementations, and their licenses.
4. How to identify versions that are well-maintained and suitable for commercial applications.

---

## The Foundations of YOLO: Joseph Redmon’s Contributions

The YOLO story begins with [Joseph Redmon](https://www.pjreddie.com/), who introduced the framework in 2016 with his paper ["You Only Look Once: Unified, Real-Time Object Detection"](https://arxiv.org/abs/1506.02640). Over the course of three major iterations, Redmon established the foundation of YOLO’s design and philosophy, which continues to influence all subsequent versions.

### Key Ideas That Define YOLO

What makes YOLO unique is its **single-shot detection approach**. Instead of breaking the image into regions or running multiple passes, YOLO processes the entire image in one go, framing object detection as a regression problem. This method allows YOLO to be incredibly fast and efficient, making it ideal for real-time applications.

Even today, these core ideas, processing the image in one pass, dividing it into a grid, and predicting bounding boxes and class probabilities simultaneously, are present in every version of YOLO, no matter how advanced or modified they’ve become.

---

### Joseph Redmon's Exit from YOLO Development

In 2020, Joseph Redmon made the decision to withdraw from computer vision research. As he explained in a twitter statement, the ethical implications of his work, particularly its use in military applications and the growing concerns around privacy, were impossible for him to ignore:

> "I stopped doing CV research because I saw the impact my work was having. I loved the work but the military applications and privacy concerns eventually became impossible to ignore." [[src]](https://x.com/pjreddie/status/1230524770350817280)

His withdrawal marked the end of his direct contributions to YOLO, but the framework lives on, thanks to the open-source community and researchers who continue to develop and extend it.

Joseph Redmon not only made YOLO freely available but also showcased his playful and humorous personality by licensing YOLO (or more specifically, its underlying library **Darknet**) under the **"DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE"**. This license epitomized the open-source ethos of YOLO's origins and emphasized complete freedom for users. However, as the YOLO framework evolved through different contributors, subsequent versions adopted a variety of licenses, some of which impose more restrictions.

---

## The first three versions

The first three YOLO versions remain **essential starting points** for anyone learning about YOLO. They encapsulate the core philosophy of YOLO—speed, simplicity, and real-time performance—and form the backbone of all subsequent developments in the framework. Even as YOLO has evolved, these foundational ideas have remained integral to most of the new version.

### YOLO v1 (2016)

The original YOLO revolutionized object detection by framing it as a single regression problem. While it was fast, YOLO v1 struggled with detecting small objects and had relatively low accuracy compared to region proposal methods like Faster R-CNN.

**Highlights:**
- Introduced the single-shot detection approach.
- Achieved 45 FPS on a standard GPU.
- Struggled with small object detection.

**Implementation:** Original [Darknet GitHub Repository](https://github.com/pjreddie/darknet)  
**Publication:** [You Only Look Once: Unified, Real-Time Object Detection](https://arxiv.org/abs/1506.02640)   
**License:** [WTFPL](https://github.com/pjreddie/darknet/blob/master/LICENSE.fuck) (do what the fuck you want to public license) (permissive, suitable for commercial use)

---

### YOLO v2 (YOLO 9000) (2017)

YOLO v2, also called YOLO 9000, brought several improvements, including batch normalization, high-resolution classifiers, and anchor boxes. It introduced the ability to detect more than 9,000 object categories by combining supervised and unsupervised learning.

**Highlights:**
- Improved accuracy and recall.
- Introduced anchor boxes for better localization.
- Can detect a wide variety of object classes (9,000+).

**Implementation:** [Darknet GitHub Repository](https://github.com/pjreddie/darknet)  
**Publication:** [YOLO9000: Better, Faster, Stronger](https://arxiv.org/abs/1612.08242)   
**License:** [WTFPL](https://github.com/pjreddie/darknet/blob/master/LICENSE.fuck) (do what the fuck you want to public license) (permissive, suitable for commercial use)

---

### YOLO v3 (2018)

YOLO v3 was a major upgrade. It used Darknet-53 as its backbone and introduced multi-scale predictions, making it much better at detecting small objects. YOLO v3 struck a balance between speed and accuracy, which made it highly popular.

**Highlights:**
- Multi-scale predictions for better small object detection.
- Improved backbone architecture (Darknet-53).
- Higher accuracy with minimal loss in speed.

#### Official Implementation by Joseph Redmon

The original implementation of YOLOv3 was released by Joseph Redmon in his Darknet framework. This version is written in C and CUDA and serves as the basis for many of the YOLO models that followed.

- **Implementation:** [Darknet GitHub Repository](https://github.com/pjreddie/darknet)  
- **Publication:** [YOLOv3: An Incremental Improvement](https://arxiv.org/abs/1804.02767)  
- **License:** [WTFPL](https://github.com/pjreddie/darknet/blob/master/LICENSE.fuck) (do what the fuck you want to public license) (permissive, suitable for commercial use)

#### Community Implementations

Over the years, YOLOv3 has been re-implemented in various frameworks to make it more accessible and easier to use. Here are some notable community-driven implementations:

1. **PyTorch YOLOv3 by Erik Linder-Norén (2019)**  
   This is an early and popular re-implementation of YOLOv3 in PyTorch, designed to simplify training and inference for researchers and developers.  
   - **Implementation:** [PyTorch-YOLOv3 GitHub Repository](https://github.com/eriklindernoren/PyTorch-YOLOv3)  
   - **License:** [GPL-3.0](https://github.com/eriklindernoren/PyTorch-YOLOv3/blob/master/LICENSE) 
     *(Less permissive, restricts commercial use unless derivative works are also open-sourced)*  

2. **Ultralytics YOLOv3 (2019)**  
   Ultralytics or more precisely it's founder [:octocat: Glenn Jocher](https://github.com/glenn-jocher), initially released their own PyTorch implementation of YOLOv3. This version started as a fork of Erik Lindernoren's PyTorch implementation but quickly evolved into a more polished and user-friendly framework, offering features like pre-trained models and support for custom training. A mention of Linder-Norén's version this was based on, can still be found in [old commits of the project's readme](https://github.com/ultralytics/yolov3/commit/c3731591aff0e65aeb375a2b0f756bb87a03ccd8#diff-b335630551682c19a781afebcf4d07bf978fb1f8ac04c6bf87428ed5106870f5R10).
   - **Implementation:** [Ultralytics YOLOv3 GitHub Repository](https://github.com/ultralytics/yolov3)  
   - **License:** [GPL-3.0](https://github.com/ultralytics/yolov3/blob/master/LICENSE)  
     *(Less permissive, restricts commercial use unless derivative works are also open-sourced)*  


---

### YOLO v4 (2020)

YOLO v4 was developed by [:octocat: Alexey Bochkovskiy](https://github.com/AlexeyAB) after Joseph Redmon stepped away from computer vision research. YOLO v4 focused on accessibility, making it easier for developers to train models on custom datasets. It added features like [mosaic augmentation](https://wiki.cloudfactory.com/docs/mp-wiki/augmentations/mosaic), CIoU loss, and CSPDarknet53 as the backbone.

**Highlights:**
- Improved training techniques and augmentation methods.
- Faster and more accurate than YOLO v3.
- Suitable for training on consumer-grade hardware (e.g., GPUs like GTX 1080Ti).

**Implementation:** [YOLOv4 GitHub Repository](https://github.com/AlexeyAB/darknet)  
**Publication**: [YOLOv4: Optimal Speed and Accuracy of Object Detection](https://arxiv.org/abs/2004.10934)  
**License:** [YOLO License](https://github.com/AlexeyAB/darknet/blob/master/LICENSE) (permissive, suitable for commercial use) 

---

### YOLO v5 (2020)

YOLOv5 was the first original Release of a YOLO version by [Ultralytics](https://www.ultralytics.com/) and has been developed by it's founder [:octocat: Glenn Jocher](https://github.com/glenn-jocher). It became highly popular due to its PyTorch implementation, ease of use, and active maintenance. Ultralytics has since developed several newer YOLO versions and it can be said, that their framework hosts the most popular and best maintained YOLO implementations as of today. Their YOLO versions in general can be used freely with an AGPL-3.0 license, which demands publishing software products which use them as open source as well. However, Ultralytics also offers a paid enterprise license for commercial usage.

**Highlights:**
- Implemented in PyTorch, making it more accessible for researchers.
- Smaller, faster models for mobile and embedded devices.
- Regularly updated with new features.

**Implementation:** [YOLOv5 GitHub Repository](https://github.com/ultralytics/yolov5)  
**License:** [GNU Affero General Public License v3.0](https://github.com/ultralytics/yolov5/blob/master/LICENSE) (AGPL-3.0)  
*Note: AGPL-3.0 requires that modifications to the codebase be shared, even in SaaS applications.*

---

### YOLOX (2021)

YOLOX, developed by **Zheng Ge, Songtao Liu, Feng Wang, Zeming Li, and Jian Sun**, represents a high-performance rethinking of the YOLO series. This anchor-free object detector integrates advanced techniques, such as decoupled heads and the SimOTA label assignment strategy, to achieve state-of-the-art results. YOLOX performs exceptionally well across various model sizes, making it suitable for a wide range of applications, from lightweight models to large-scale real-time detection.

**Key Features:**
- **Anchor-Free Design:** Moves away from anchor-based detection for simpler implementation and improved accuracy.
- **Decoupled Head:** Separates classification and regression tasks for better performance.
- **SimOTA Label Assignment:** Employs the SimOTA strategy for more efficient and accurate label assignment during training.
- **Versatility:** YOLOX supports a range of model sizes, including YOLO-Nano for ultra-lightweight applications and YOLOX-L for high-performance detection.
- **Deployment-Ready:** Pre-built support for ONNX, TensorRT, NCNN, and OpenVINO ensures easy deployment across platforms.
- **Performance Highlights:** Achieved 50.0% AP on COCO with YOLOX-L at 68.9 FPS (Tesla V100), and outperformed other YOLO models like YOLOv5-L.

**Implementation:** [YOLOX GitHub Repository](https://github.com/Megvii-BaseDetection/YOLOX)  
**Publication:** [YOLOX: Exceeding YOLO Series in 2021](https://arxiv.org/abs/2107.08430)  
**License:** [Apache 2.0](https://github.com/Megvii-BaseDetection/YOLOX/blob/main/LICENSE) *(Permissive, suitable for commercial use)*  

---

### YOLOV (2022) and YOLOV++ (2024)

YOLOV and YOLOV++ are advancements aimed specifically at **video object detection (VOD)**, developed by **Yuheng Shi et al.** These models tackle the unique challenges of VOD, such as high variation in object appearance and frame deterioration, by proposing efficient strategies for feature aggregation and selection. While YOLOV introduces the foundational ideas, YOLOV++ builds upon it to achieve record-breaking performance.

#### YOLOV (2022)

**Key Features:**
- **Feature Aggregation Across Frames:** Aggregates features across video frames to leverage temporal information, improving accuracy while keeping computational overhead low.
- **One-Stage Detector Focus:** Tailored for one-stage detectors to avoid the computational cost of two-stage approaches.
- **Performance Highlights:** Achieved 87.5% AP50 at over 30 FPS on the ImageNet VID dataset using a single NVIDIA 2080Ti GPU, making it highly suitable for real-time applications.

**Publication:** [YOLOV: Making Still Image Object Detectors Great at Video Object Detection](https://arxiv.org/abs/2208.09686)  
**Implementation:** [YOLOV GitHub Repository](https://github.com/YuHengsss/YOLOV)  
**License:** [Apache 2.0](https://github.com/YuHengsss/YOLOV/blob/master/LICENSE) *(Permissive, suitable for commercial use)*  

#### YOLOV++ (2024)

YOLOV++ enhances YOLOV with more advanced feature selection and aggregation methods, specifically designed to minimize computational expense while maximizing accuracy for video object detection.

**Key Features:**
- **Selective Feature Aggregation:** Introduces a novel strategy for selecting and aggregating features from dense prediction maps, reducing memory usage and computation costs.
- **Relationship Evaluation:** Evaluates the relationship between target and reference frames to guide feature aggregation effectively.
- **Record-Breaking Performance:** Reached 92.9% AP50 at over 30 FPS on the ImageNet VID dataset using a single NVIDIA 3090 GPU, making it a standout choice for large-scale or real-time video applications.

**Publication:** [Practical Video Object Detection via Feature Selection and Aggregation](https://arxiv.org/abs/2407.19650)  
**Implementation:** [YOLOV GitHub Repository](https://github.com/YuHengsss/YOLOV)  
**License:** [Apache 2.0](https://github.com/YuHengsss/YOLOV/blob/master/LICENSE) *(Permissive, suitable for commercial use)*  

---

### YOLO v6 (2022)

YOLOv6 was introduced by Meituan as an industrial-grade object detection framework. It focused on delivering high accuracy and performance with efficient resource usage.

**Highlights:**
- Optimized for deployment in production.
- Superior performance compared to YOLOv5 on certain benchmarks.

**Implementation:** [YOLOv6 GitHub Repository](https://github.com/meituan/YOLOv6)  
**Publication:** [YOLOv6: A Single-Stage Object Detection Framework for Industrial Applications](https://arxiv.org/abs/2209.02976)  
**License:** [GNU General Public License v3.0](https://github.com/meituan/YOLOv6/blob/main/LICENSE)

*Assessment for Commercial Use:* The GNU General Public License v3.0 (GPL-3.0) requires that any derivative works or applications using the software must also be distributed under the same license. This means that if you modify or build upon YOLOv6, you must open-source your code under GPL-3.0. For commercial use, this restriction can be limiting unless the source code of your application is also made available, which is not ideal for proprietary software. For companies seeking to keep their projects closed-source, YOLOv6 may not be a suitable choice.

---

### YOLO v7 (2022)

YOLOv7, published by Chien-Yao Wang, Alexey Bochkovskiy and Hong-Yuan Mark Liao, claims to be the fastest and most accurate real-time object detection model in the YOLO family. It introduced several innovative features like Extended Efficient Layer Aggregation Networks (E-ELAN).

**Highlights:**
- State-of-the-art accuracy on COCO dataset benchmarks.
- Optimized for real-time object detection.

**Implementation:** [YOLOv7 GitHub Repository](https://github.com/WongKinYiu/yolov7)  
**Publication:** [YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://arxiv.org/abs/2207.02696)
**License:** [GNU General Public License v3.0 ](https://github.com/WongKinYiu/yolov7/blob/main/LICENSE.md)

*Assessment for Commercial Use:* The GNU General Public License v3.0 (GPL-3.0) requires that any derivative works or applications using the software must also be distributed under the same license. This means that if you modify or build upon YOLOv7, you must open-source your code under GPL-3.0. For commercial use, this restriction can be limiting unless the source code of your application is also made available, which is not ideal for proprietary software. For companies seeking to keep their projects closed-source, YOLOv7 may not be a suitable choice.

---


### YOLO-NAS (2023)

YOLO-NAS, developed by Deci, uses neural architecture search (NAS) to optimize the model’s architecture. It offers an excellent trade-off between accuracy and speed, making it suitable for a wide range of real-world applications.
Recently, Deci has been acquired by NVIDIA, so the licensing options for using YOLO-NAS are currently in hold.

**Highlights:**
- Leverages NAS for automated architecture optimization.
- Outperforms YOLOv5 and YOLOv6 on speed and accuracy.

**Implementation:** [YOLO-NAS GitHub Repository](https://github.com/Deci-AI/super-gradients)  
**License:** [Custom YOLO-NAS License](https://github.com/Deci-AI/super-gradients/blob/master/LICENSE.YOLONAS.md) 

---
### YOLO v8 (2023)

YOLOv8 was introduced by **Ultralytics**, led by Glenn Jocher, Ayush Chaurasia, and Jing Qiu. As a significant step forward in the YOLO family, YOLOv8 focused on optimizing the trade-off between speed and accuracy while introducing architectural improvements that made it highly versatile.

**Key Features:**
- **Advanced Backbone and Neck Architectures:** YOLOv8 incorporates state-of-the-art backbone and neck designs for improved feature extraction and enhanced object detection performance.
- **Anchor-Free Ultralytics Head:** YOLOv8 utilizes an anchor-free detection head, which increases efficiency and accuracy compared to traditional anchor-based approaches.
- **Optimized Accuracy-Speed Tradeoff:** Designed for real-time applications, YOLOv8 strikes a fine balance between speed and detection accuracy, making it suitable for diverse tasks.
- **Pre-trained Models:** A variety of pre-trained models are provided, enabling users to easily adapt YOLOv8 to specific use cases without starting from scratch.

**Implementation:** [Ultralytics GitHub Repository](https://github.com/ultralytics/ultralytics)  
**License:** [GNU Affero General Public License v3.0](https://github.com/ultralytics/yolov5/blob/master/LICENSE) *(AGPL-3.0, restricts commercial use unless derivative works are also open-sourced)*  

---

### YOLO v9 (2024)

YOLOv9, developed by **Chien-Yao Wang, I-Hau Yeh, and Hong-Yuan Mark Liao**, introduced innovative concepts to overcome the challenge of information loss in deep neural networks, making it a groundbreaking step in real-time object detection.

**Key Features:**
- **Programmable Gradient Information (PGI):** Addresses the information bottleneck problem by preserving essential data across network layers, improving gradient reliability and model convergence.
- **Reversible Functions:** Allows lossless information flow throughout the network, particularly in deeper layers, mitigating data degradation.
- **Generalized Efficient Layer Aggregation Network (GELAN):** Enhances computational efficiency and parameter utilization, ensuring the architecture is adaptable to various use cases.
- **Lightweight Model Optimization:** Designed to retain performance in lightweight models by preserving crucial information, making YOLOv9 suitable for resource-constrained environments.

**Implementation:** [YOLOv9 GitHub Repository](https://github.com/WongKinYiu/yolov9)  
**Publication:** [YOLOv9: Learning What You Want to Learn Using Programmable Gradient Information](https://arxiv.org/abs/2402.13616)  
**License:** [GNU General Public License v3.0](https://github.com/WongKinYiu/yolov9/blob/main/LICENSE.md) *(GPL-3.0, restricts commercial use unless derivative works are also open-sourced)*  

---

### YOLO v10 (2024)

YOLOv10, developed by researchers from **Tsinghua University** (Ao Wang, Hui Chen, Lihao Liu, Kai Chen, Zijia Lin, Jungong Han, and Guiguang Ding), introduces a significant shift in real-time object detection by eliminating the need for non-maximum suppression (NMS).

**Key Features:**
- **NMS-Free Training:** Replaces traditional non-maximum suppression with a consistent dual-assignment approach during training, reducing inference latency and improving prediction efficiency.
- **One-to-One Detection Head:** Ensures that each object is assigned a single best prediction, further simplifying the detection pipeline.
- **Optimized Model Design:** Includes refined architectural components to achieve better performance with reduced computational overhead.

**Implementation:** [YOLOv10 GitHub Repository](https://github.com/THU-MIG/yolov10)  
**Publication:** [YOLOv10: Real-Time End-to-End Object Detection](https://arxiv.org/abs/2405.14458)  
**License:** [GNU Affero General Public License v3.0](https://github.com/THU-MIG/yolov10/blob/main/LICENSE) *(AGPL-3.0, restricts commercial use unless derivative works are also open-sourced)*  

---

### YOLO v11 (2024)

YOLOv11 is the latest release from **Ultralytics**, building on its predecessors with a strong focus on computational efficiency, accuracy, and support for a broader range of tasks. It incorporates advancements in feature extraction and training optimization.

**Key Features:**
- **Enhanced Feature Extraction:** Improved backbone and neck architectures deliver better feature extraction, enabling more precise object detection.
- **Optimized Efficiency and Speed:** Refined designs and training pipelines allow for faster inference while maintaining a strong balance between accuracy and performance.
- **Higher Accuracy with Fewer Parameters:** YOLOv11 achieves higher mean Average Precision (mAP) on benchmarks like COCO while reducing model parameters by 22% compared to YOLOv8m, making it computationally efficient.
- **Versatile Deployment:** Designed for seamless deployment across edge devices, cloud platforms, and NVIDIA GPU-powered systems.
- **Broad Task Support:** Supports diverse computer vision tasks such as object detection, instance segmentation, image classification, pose estimation, and oriented object detection (OBB).

**Implementation:** [Ultralytics GitHub Repository](https://github.com/ultralytics/ultralytics)  
**License:** [GNU Affero General Public License v3.0](https://github.com/ultralytics/yolov5/blob/master/LICENSE) *(AGPL-3.0, restricts commercial use unless derivative works are also open-sourced)*  

### YOLO v12 (2025)

**YOLOv12**, developed by **Yunjie Tian**, **Qixiang Ye**, and **David Doermann**, introduces a new attention-centric paradigm to the YOLO family. Unlike its CNN-focused predecessors, YOLOv12 integrates attention mechanisms into the core of the architecture—while still preserving the hallmark efficiency and speed that define YOLO detectors.

**Key Features:**
- **Attention-Centric Architecture:** YOLOv12 is the first in the YOLO series to be built around attention modules rather than convolution. It uses a novel *area attention* mechanism, which maintains a large receptive field while significantly reducing computation cost.
- **Residual Efficient Layer Aggregation (R-ELAN):** Improves upon traditional ELAN modules by introducing residual connections and more effective feature aggregation for stable training, especially in large models.
- **Speed-Optimized Transformer Techniques:** Incorporates optimizations like FlashAttention, removal of positional encodings, and modified MLP ratios to reduce latency and memory bottlenecks.
- **Superior Performance:** YOLOv12 consistently outperforms previous YOLO versions (v9–v11) and transformer-based detectors like RT-DETR and RT-DETRv2 across multiple model scales. For example:
  - **YOLOv12-N:** 40.6% mAP with just 1.64 ms latency.
  - **YOLOv12-S:** 48.0% mAP, beating YOLOv11-S by 1.1% with similar resource usage.
  - **YOLOv12-X:** 55.2% mAP—outperforming YOLOv11-X and RT-DETRv2-R101 while running faster and using fewer parameters.

**Implementation:** [YOLOv12 GitHub Repository](https://github.com/sunsmarterjie/yolov12)  
**Publication:** *[YOLOv12: Attention-Centric Real-Time Object Detectors](https://arxiv.org/abs/2502.12524)*  
**License:** [GNU Affero General Public License v3.0](https://github.com/sunsmarterjie/yolov12?tab=AGPL-3.0-1-ov-file) 
*Note: May require GPUs compatible with FlashAttention (Turing or newer NVIDIA architectures).*

## Understanding YOLO Licenses and Their Implications for Commercial Use

When choosing a YOLO implementation for real-world applications, especially proprietary or commercial products, it’s essential to understand the **software license** under which it is released. Different licenses come with different levels of freedom and restriction, particularly when it comes to modifying code, redistributing it, and using it in closed-source commercial products.

Here’s an overview of the most relevant licenses used in YOLO implementations, along with a summary of their impact on commercial use. *This is not legal advice—consult a legal professional for guidance on compliance in your specific context.*

---

### 🟥 GNU Affero General Public License v3.0 (AGPL-3.0)

**Used by:** YOLOv5, YOLOv8, YOLOv10, YOLOv11  
**Type:** Strong Copyleft  
**Commercial Use:** ⚠️ **Restricted**

The AGPL-3.0 is one of the most restrictive open-source licenses. It allows commercial use *only if* you make your **entire** source code (including modifications and any software it interacts with over a network) publicly available under the same license. This effectively prohibits proprietary use unless you're willing to open source your codebase. This makes it unsuitable for most closed-source or SaaS products.

---

### 🟧 GNU General Public License v3.0 (GPL-3.0)

**Used by:** YOLOv4, YOLOv6, YOLOv9  
**Type:** Strong Copyleft  
**Commercial Use:** ⚠️ **Restricted**

Like the AGPL, the GPL-3.0 requires that derivative works and linked components also be released under the same license. You can use GPL-licensed software in commercial products, *but only if* you also open source those products under GPL. This may not be compatible with proprietary or internal-use software models.

---

### 🟨 Apache License 2.0

**Used by:** YOLOX, YOLOV, YOLOV++  
**Type:** Permissive  
**Commercial Use:** ✅ **Allowed**

The Apache 2.0 license is highly permissive. You can use, modify, and distribute the software in proprietary products without releasing your own source code, provided you retain copyright and license notices. It also includes a patent grant, offering additional protection.

---

### 🟩 MIT License

**Used by:** Some YOLOv3 community implementations (e.g., by Erik Lindernoren)  
**Type:** Permissive  
**Commercial Use:** ✅ **Allowed**

Similar in spirit to Apache 2.0, the MIT License allows free commercial use, including in closed-source projects. The only requirements are to include the original license and copyright notice.

---

### 🟦 WTFPL (Do What the F*** You Want to Public License)

**Used by:** Original Darknet implementation (YOLOv1–v3)  
**Type:** Very Permissive  
**Commercial Use:** ✅ **Unrestricted**

This is perhaps the most permissive license in existence. As the name implies, it grants complete freedom to do whatever you want with the code, including using it in proprietary software, without any obligations.

---

### 🟪 YOLO License by Joseph Redmon (Darknet)

**Used by:** Darknet (Redmon’s implementation of YOLOv1–v3)  
**Type:** Public Domain / Custom  
**Commercial Use:** ✅ **Unrestricted**

This humorous license effectively places Darknet in the public domain. It explicitly states:  
> "Do whatever you want with it. Stop emailing me about it!"

There are no restrictions whatsoever, making it fully usable in commercial projects.

---

### ⛔ YOLO-NAS License by Deci.AI

**Used by:** YOLO-NAS  
**Type:** Custom, Proprietary  
**Commercial Use:** ❌ **Prohibited without explicit permission**

YOLO-NAS is **not** open source. Although the code is available for research and non-commercial use, the license **explicitly forbids** using the software in any commercial or production setting unless you have prior written permission from Deci. This includes deploying it in models used as a service, in SaaS platforms, or integrated into commercial apps.

---

### Summary Table: Licensing at a Glance

| **License**                      | **Used By**                             | **Commercial Use**      | **Closed-Source Allowed?** | **Key Notes**                                  |
|----------------------------------|------------------------------------------|--------------------------|-----------------------------|------------------------------------------------|
| AGPL-3.0                         | YOLOv5, YOLOv8, YOLOv10, YOLOv11         | ⚠️ Limited               | ❌ No                        | Must release full source, even for SaaS use    |
| GPL-3.0                          | YOLOv4, YOLOv6, YOLOv9                   | ⚠️ Limited               | ❌ No                        | Strong copyleft, all derivatives must be GPL   |
| Apache 2.0                       | YOLOX, YOLOV, YOLOV++                    | ✅ Yes                  | ✅ Yes                      | Safe for commercial/proprietary use            |
| MIT                              | Community YOLOv3 (e.g., Lindernoren)     | ✅ Yes                  | ✅ Yes                      | Very permissive                                |
| WTFPL                            | Darknet YOLOv1–v3                        | ✅ Yes                  | ✅ Yes                      | Do literally anything                          |
| YOLO License (custom, public domain) | Darknet (Redmon)                       | ✅ Yes                  | ✅ Yes                      | Public domain + humor                          |
| YOLO-NAS (Deci.AI)               | YOLO-NAS                                 | ❌ No                   | ❌ No                       | Commercial use prohibited without permission    |

---

In conclusion, if you're planning to build **proprietary** or **commercial** software products with YOLO, you’ll want to focus on versions licensed under **Apache 2.0**, **MIT**, or **public domain equivalents**. Versions under **AGPL** or **GPL** are best suited for open-source projects, academic research, or internal experimentation unless you're prepared to make your code publicly available.

Always review the specific license files in each repository, and if in doubt, seek legal advice.




## Summary: Choosing the Right YOLO Version

Here’s a quick overview of YOLO versions, their licenses, and suitability for commercial use:

| **Version**  | **Implementation**                              | **License**        | **Commercial Use**       |
|--------------|--------------------------------------------------|--------------------|--------------------------|
| YOLO v1      | [GitHub](https://github.com/pjreddie/darknet)    | MIT                | ✅ Yes                   |
| YOLO v2      | [GitHub](https://github.com/pjreddie/darknet)    | MIT                | ✅ Yes                   |
| YOLO v3      | [GitHub](https://github.com/pjreddie/darknet)    | MIT                | ✅ Yes                   |
| YOLO v4      | [GitHub](https://github.com/AlexeyAB/darknet)    | GPL-3.0            | ⚠️ Restricted            |
| YOLO v5      | [GitHub](https://github.com/ultralytics/yolov5)  | AGPL-3.0           | ⚠️ Restricted            |
| YOLO v6      | [GitHub](https://github.com/meituan/YOLOv6)      | Apache 2.0         | ✅ Yes                   |
| YOLO v7      | [GitHub](https://github.com/WongKinYiu/yolov7)   | Apache 2.0         | ✅ Yes                   |
| YOLO-NAS     | [GitHub](https://github.com/Deci-AI/yolonas)     | Apache 2.0         | ✅ Yes                   |

---

## Sources

Yolo versions overview by Ultralytics: https://docs.ultralytics.com/models/
