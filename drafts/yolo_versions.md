#---
#title: "Understanding YOLO: Exploring the Evolution of Object Detection Frameworks"
#date: 2024-12-12
#description: "A deep dive into YOLO (You Only Look Once), its various versions, implementations, and licenses. Learn which versions are suitable for commercial use and well-maintained."
#tags: ["YOLO", "Object Detection", "Computer Vision", "Deep Learning"]
#---

# DRAFT DRAFT DRAFT DRAFT


# YOLO: A Journey Through Its Versions

Object detection is one of the most exciting tasks in computer vision, and **YOLO (You Only Look Once)** has been at the forefront of this domain for years. YOLO is known for its real-time object detection capabilities, simplicity, and speed, which makes it ideal for many applications, from self-driving cars to video surveillance systems. Over time, several versions and forks of YOLO have emerged, each offering improvements and trade-offs. However, with so many versions and implementations, finding the right one for your project—especially for commercial use—can be overwhelming.

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

Even today, these core ideas—processing the image in one pass, dividing it into a grid, and predicting bounding boxes and class probabilities simultaneously—are present in every version of YOLO, no matter how advanced or modified they’ve become.

---

### Joseph Redmon's Exit from YOLO Development

In 2020, Joseph Redmon made the decision to withdraw from computer vision research. As he explained in a twitter statement, the ethical implications of his work, particularly its use in military applications and the growing concerns around privacy, were impossible for him to ignore:

> "I stopped doing CV research because I saw the impact my work was having. I loved the work but the military applications and privacy concerns eventually became impossible to ignore."

His withdrawal marked the end of his direct contributions to YOLO, but the framework lives on, thanks to the open-source community and researchers who continue to develop and extend it.

Joseph Redmon not only made YOLO freely available but also showcased his playful and humorous personality by licensing YOLO (or more specifically, its underlying library **Darknet**) under the **"DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE"**. This license epitomized the open-source ethos of YOLO's origins and emphasized complete freedom for users. However, as the YOLO framework evolved through different contributors, subsequent versions adopted a variety of licenses, some of which impose more restrictions—something we’ll explore as we look at the newer YOLO implementations.

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
   Ultralytics or more precisely it's founder [:octocat: Glenn Jocher](https://github.com/glenn-jocher), initially released their own PyTorch implementation of YOLOv3. This version started as a fork of Erik Lindernoren's PyTorch implementation but quickly evolved into a more polished and user-friendly framework, offering features like pre-trained models and support for custom training. A mention of Linder-Norén's version this was based on, can still be found in [old commits of the project's readme](https://github.com/ultralytics/yolov3/commit/c3731591aff0e65aeb375a2b0f756bb87a03ccd8#diff-b335630551682c19a781afebcf4d07bf978fb1f8ac04c6bf87428ed5106870f5).
   - **Implementation:** [Ultralytics YOLOv3 GitHub Repository](https://github.com/ultralytics/yolov3)  
   - **License:** [GPL-3.0](https://github.com/ultralytics/yolov3/blob/master/LICENSE)  
     *(Less permissive, restricts commercial use unless derivative works are also open-sourced)*  


---

## YOLO v4 (2020)

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

YOLOv5 is a controversial version because it was not developed by the original authors or maintainers of YOLO. Instead, it was released by the company [Ultralytics](https://www.ultralytics.com/). Despite the controversy, YOLOv5 became highly popular due to its PyTorch implementation, ease of use, and active maintenance. Ultralytics has since developed several newer YOLO versions and it can be said, that their framework hosts the most popular and best maintained YOLO implementation as of today. However, their versions are also the first ones which require a paid license for commercial usage.

**Highlights:**
- Implemented in PyTorch, making it more accessible for researchers.
- Smaller, faster models for mobile and embedded devices.
- Regularly updated with new features.

**Implementation:** [YOLOv5 GitHub Repository](https://github.com/ultralytics/yolov5)  
**License:** [GNU Affero General Public License v3.0](https://github.com/ultralytics/yolov5/blob/master/LICENSE) (AGPL-3.0)  
*Note: AGPL-3.0 requires that modifications to the codebase be shared, even in SaaS applications.*

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

## Conclusion

YOLO's journey has been remarkable, with each version pushing the boundaries of what real-time object detection can achieve. Choosing the right version depends on your project's needs, the desired trade-off between speed and accuracy, and licensing requirements for commercial use. If you're looking for a well-maintained, permissively licensed version, YOLOv6, YOLOv7, or YOLO-NAS may be the best choices.

Which YOLO version are you using for your project? Let us know
