# LiDAR-based Object Detection with YOLO
This project implements a YOLO-based object detection system utilizing LiDAR data represented as BEV images. The KITTI dataset, featuring 3D bounding boxes (BBs) as ground truth, was used for evaluation across 20 scenes. 

The system evaluates the model's performance using precision and recall metrics, with detections highlighted in red and ground truth in green. Judgments were made based on Intersection over Union (IoU) thresholds, reflecting detection accuracy.

**Methodology**
The evaluation criteria hinge on IoU thresholds: detections are true positives (TP) when IoU ≥ 0.5, while IoU < 0.5 results in false positives (FP) or false negatives (FN). The thresholds were refined to λ values (0.5, 0.75, and 0.95), demanding higher accuracy for tighter thresholds. The Shapely library and Matplotlib were employed for visualizing bounding boxes in Python.

The project's precision and recall metrics were computed as:

<img width="387" alt="image" src="https://github.com/user-attachments/assets/a768bb66-8b25-4543-be4b-63f3aa177b09" />

Precision focuses on reducing false positives, while recall emphasizes minimizing false negatives, critical in safety-centric applications.

**Results**
The object detector's performance was visually and quantitatively analyzed. The outputs depicted varied scenes with TP, FP, and FN counts. For example:

TP = 5, FP = 11, FN = 1 — A challenging scenario with multiple false detections.

TP = 6, FP = 0, FN = 0 — High precision in simpler environments.

TP = 8, FP = 5, FN = 0 — Moderate complexity with some false positives.

The detector performed admirably in uncluttered environments but struggled in dense or ambiguous scenes, often producing overlapping bounding boxes or phantom object detections.

**Conclusion**
The object detection system demonstrated strong performance in straightforward scenarios, achieving high precision and recall. However, its efficacy diminished in complex scenes with dense or ambiguous object distributions. Improvements could involve enhancing the algorithm's robustness to varying scene complexities and refining bounding box predictions to minimize overlaps and false positives.


![image](https://github.com/user-attachments/assets/d09c737a-1357-4a9d-8e1e-df565687d803)
![image](https://github.com/user-attachments/assets/83242165-1c3b-49d2-9611-20cee5c44050)
![image](https://github.com/user-attachments/assets/5e186eda-47b5-458d-998c-6316a8bed155)
![image](https://github.com/user-attachments/assets/9b7670d9-f747-49d1-b616-e80f26d70b19)
![image](https://github.com/user-attachments/assets/6e89285f-e1a1-46a3-bdb4-971ba538734d)
![image](https://github.com/user-attachments/assets/7968cbf8-0624-4e5c-b774-14f67c30e366)
![image](https://github.com/user-attachments/assets/187d4b8d-a36c-42ad-8e79-a87940caab46)


