# Multimodal Fusion of microCT and Histology Using X-Ray Contrast-Adjustable 3D Printing

This repository contains code, CAD files, and STL files associated with the publication **"X-Ray contrast-adjustable 3D printing for multimodal fusion of microCT and histology"**.

The project provides tools for aligning microCT volumes with histological images using custom 3D-printed registration cones, along with auxiliary workflows for data processing, cone detection, machine learning–based annotation, and segmentation.

---

## Main Workflow

### **`Multimodal_registration.ipynb`**

This is the primary notebook of the repository. It performs:

* Alignment of microCT data with histological images
* Utilization of the 3D‑printed cones as registration landmarks
* Visualization and validation of fused modalities

---

## Supporting Notebooks

### **`data_exploration.ipynb`**

* Visualization of microCT stacks
* Pre- and post‑processing of images for stitching

### **`stack_image_processing.ipynb`**

* Detection of registration cones in the microCT stack
* Image processing pipeline for cone localization

### **`create_yolo_dataset.ipynb`**

* Generation of image annotations based on the detection pipeline
* Preparation of datasets for YOLO training

### **`yolo_train.ipynb`**

* Training of a YOLO model for cone detection
* Comparison of YOLO performance to the manual detection pipeline

### **`yolo_val.ipynb`**

* Validation of the trained YOLO model on a separate validation set

### **`yolo_cone_workflow.ipynb`**

* Post-processing and cleaning of YOLO detection outputs

### **`SAM_workflow.ipynb`**

* Use of the Segment Anything Model (SAM) to create binary masks of cones
* Mask generation based on YOLO bounding box detections

### **`SAM_HvW.ipynb`**

* Construction of a height‑versus‑width lookup table
* Used for improved alignment accuracy in the main multimodal workflow

---

## Data

Generated CSV files required for the workflows are stored in the **`CSV/`** directory for clearer organization.

---

## Structure

* `*.ipynb` – Processing, training, segmentation, and registration workflows
* `CAD and STL/` – Combined folder containing CAD models and 3D-printable STL files used in the publication
* `CSV/` – Generated datasets used during various notebook executions

---

## Resources

* YOLO annotation tool used: [ybat](https://github.com/drainingsun/ybat)
* Segment Anything Model (SAM): [SAM2](https://github.com/facebookresearch/sam2)

## Citation

If you use this repository, please cite the associated publication:

> *[Add citation once available]*

---

For questions or contributions, feel free to open an issue or submit a pull request.
