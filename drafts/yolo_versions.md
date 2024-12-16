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

**Implementation:** Original [YOLO GitHub Repository](https://github.com/pjreddie/darknet)  
**Publication:** https://arxiv.org/abs/1506.02640  
**License:** [WTFPL](https://github.com/pjreddie/darknet/blob/master/LICENSE.fuck) (do what the fuck you want to public license) (permissive, suitable for commercial use)

---

### YOLO v2 (YOLO 9000) (2017)

YOLO v2, also called YOLO 9000, brought several improvements, including batch normalization, high-resolution classifiers, and anchor boxes. It introduced the ability to detect more than 9,000 object categories by combining supervised and unsupervised learning.

**Highlights:**
- Improved accuracy and recall.
- Introduced anchor boxes for better localization.
- Can detect a wide variety of object classes (9,000+).

**Implementation:** [Darknet YOLOv2 GitHub Repository](https://github.com/pjreddie/darknet)  
**Publication:** https://arxiv.org/abs/1612.08242  
**License:** [WTFPL](https://github.com/pjreddie/darknet/blob/master/LICENSE.fuck) (do what the fuck you want to public license) (permissive, suitable for commercial use)

---

### YOLO v3 (2018)

YOLO v3 was a major upgrade. It used Darknet-53 as its backbone and introduced multi-scale predictions, making it much better at detecting small objects. YOLO v3 struck a balance between speed and accuracy, which made it highly popular.

**Highlights:**
- Multi-scale predictions for better small object detection.
- Improved backbone architecture (Darknet-53).
- Higher accuracy with minimal loss in speed.

**Implementation:** [Darknet YOLOv3 GitHub Repository](https://github.com/pjreddie/darknet)  
**License:** [WTFPL](https://github.com/pjreddie/darknet/blob/master/LICENSE.fuck) (do what the fuck you want to public license) (permissive, suitable for commercial use)

---

## YOLO v4 (2020)

YOLO v4 was developed by [:octocat: Alexey Bochkovskiy](https://github.com/AlexeyAB) after Joseph Redmon stepped away from computer vision research. YOLO v4 focused on accessibility, making it easier for developers to train models on custom datasets. It added features like mosaic augmentation, CIoU loss, and CSPDarknet53 as the backbone.

**Highlights:**
- Improved training techniques and augmentation methods.
- Faster and more accurate than YOLO v3.
- Suitable for training on consumer-grade hardware (e.g., GPUs like GTX 1080Ti).

**Implementation:** [YOLOv4 GitHub Repository](https://github.com/AlexeyAB/darknet)  
**Publication**: [YOLOv4: Optimal Speed and Accuracy of Object Detection](https://arxiv.org/abs/2004.10934)  
**License:** [YOLO License](https://github.com/AlexeyAB/darknet/blob/master/LICENSE) (permissive, suitable for commercial use) 

---

### YOLO v5 (2020)

YOLOv5 is a controversial version because it was not developed by the original authors or maintainers of YOLO. Instead, it was released by Ultralytics. Despite the controversy, YOLOv5 became highly popular due to its PyTorch implementation, ease of use, and active maintenance.

**Highlights:**
- Implemented in PyTorch, making it more accessible for researchers.
- Smaller, faster models for mobile and embedded devices.
- Regularly updated with new features.

**Implementation:** [YOLOv5 GitHub Repository](https://github.com/ultralytics/yolov5)  
**License:** GNU Affero General Public License v3.0 (AGPL-3.0)  
*Note: AGPL-3.0 requires that modifications to the codebase be shared, even in SaaS applications.*

---

### YOLO v6 (2022)

YOLOv6 was introduced by Meituan as an industrial-grade object detection framework. It focused on delivering high accuracy and performance with efficient resource usage.

**Highlights:**
- Optimized for deployment in production.
- Superior performance compared to YOLOv5 on certain benchmarks.

**Implementation:** [YOLOv6 GitHub Repository](https://github.com/meituan/YOLOv6)  
**License:** Apache License 2.0 (permissive, suitable for commercial use)

---

### YOLO v7 (2022)

YOLOv7 claims to be the fastest and most accurate real-time object detection model in the YOLO family. It introduced several innovative features like Extended Efficient Layer Aggregation Networks (E-ELAN).

**Highlights:**
- State-of-the-art accuracy on COCO dataset benchmarks.
- Optimized for real-time object detection.

**Implementation:** [YOLOv7 GitHub Repository](https://github.com/WongKinYiu/yolov7)  
**License:** Apache License 2.0 (permissive, suitable for commercial use)

---

### YOLO-NAS (2023)

YOLO-NAS, developed by Deci, uses neural architecture search (NAS) to optimize the model’s architecture. It offers an excellent trade-off between accuracy and speed, making it suitable for a wide range of real-world applications.

**Highlights:**
- Leverages NAS for automated architecture optimization.
- Outperforms YOLOv5 and YOLOv6 on speed and accuracy.

**Implementation:** [YOLO-NAS GitHub Repository](https://github.com/Deci-AI/yolonas)  
**License:** Apache License 2.0 (permissive, suitable for commercial use)

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
