# Module 1 — Image Formation, Sampling & Filtering

**Author:** Mirkomil Mirzohidov  
**Course:** Computer Vision – Module 1  
**Instructors:** Dr. Atadjanov & Dr. Kiani  

This repository contains four practical notebooks (Task 1–4) demonstrating key concepts in **image formation, sampling, filtering, edge detection,** and **geometric transformations**.  
All experiments use the same base image (`img/car.jpg`) and follow the official assignment brief.

---

## 📁 Repository Structure

```bash
├── Document.docx                     # Report with explanations, results & conclusions
├── img/
│   └── car.jpg                       # Source image used for all tasks
│
├── Task1/
│   ├── Task1.ipynb                   # Image sampling, aliasing & prefiltering
│   └── task1_outputs/                # Output figures from Task 1
│
├── Task2/
│   ├── Task2.ipynb                   # Linear filters & manual convolution
│   └── task2_outputs/                # Output figures from Task 2
│
├── Task3/
│   ├── Task3.ipynb                   # Edge detection (Sobel, Prewitt, Canny)
│   └── task3_outputs/                # Output figures from Task 3
│
└── Task4/
    ├── Task4.ipynb                   # Geometric & affine transformations
    └── task4_outputs/                # Output figures from Task 4
```

Each notebook automatically saves its generated images and figures into the corresponding `task*_outputs/` folder.  
The **report (`Document.docx`)** consolidates all theoretical background, methodology, and visual results.

---

## ⚙️ Environment Setup

**Recommended:** Python 3.10 or newer.

```bash
# Create and activate a virtual environment (optional)
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

# Install dependencies
pip install numpy scipy matplotlib scikit-image opencv-python jupyter
```

Alternatively, you can open any notebook directly in **Google Colab** — just upload the repository and ensure the relative image path (`img/car.jpg`) remains correct.

---

## ▶️ How to Run

1. Open the desired folder (e.g., `Task1/`).  
2. Launch the notebook (`Task1.ipynb`) in **Jupyter Notebook** or **Google Colab**.  
3. Run all cells in order.  

Each notebook will:
- Load the image `img/car.jpg`
- Perform the task-specific processing
- Save all figures and outputs into its corresponding `task*_outputs/` folder

---

## 🧪 Task Summaries

### 🟦 Task 1 — Image Formation & Sampling (Aliasing)
- Downsampling by factors 2, 4, and 8  
- Two methods: **Naïve** (direct subsampling) and **Prefiltered** (Gaussian blur before sampling)  
- Computes 2D FFT magnitude spectra for each case  
- Demonstrates aliasing effects and the importance of Gaussian prefiltering  

### 🟦 Task 2 — Linear Filters & Manual Convolution
- Implements custom 2D convolution function without OpenCV  
- Applies **Box filters** (3×3, 5×5) and **Gaussian filters** (σ = 1, 2)  
- Compares manual results with OpenCV filtering (`cv2.filter2D`)  
- Verifies **commutativity** and reports filter smoothness quantitatively  

### 🟦 Task 3 — Edge Detection
- Uses **Sobel** and **Prewitt** filters to compute gradient magnitude and direction  
- Applies **Canny** edge detector with different thresholds  
- Demonstrates sensitivity of edges to threshold values  
- Compares edge density and gradient orientation  

### 🟦 Task 4 — Geometric Transformations
- Implements **translation**, **rotation**, **scaling**, and **affine transformations**  
- Applies **perspective (homography)** and its inverse  
- Shows the impact of transformation order (rotate → translate vs translate → rotate)  
- Discusses when a projective transform behaves like an affine one  

---

## 📊 Expected Outputs

- **task1_outputs/** → Original, downsampled images & FFT spectra  
- **task2_outputs/** → Box & Gaussian filtered images and comparison maps  
- **task3_outputs/** → Sobel/Prewitt/Canny edge detection results  
- **task4_outputs/** → Transformed images (translation, rotation, scaling, perspective)  

Each output folder includes visual results used in the final report.

---

## 📝 Report

The complete written analysis is provided in **Document.docx**, which includes:
- Theoretical background for each topic  
- Explanations of implementation and formulas  
- Experimental results and visual comparisons  
- Key conclusions for all four tasks  

---

## 📚 References

- Szeliski, R. *Computer Vision: Algorithms and Applications*, Chapters 2–3  
- OpenCV Documentation — Image Filtering and Transformations  
- Central Asian University — Computer Vision Module 1 Assignment Brief  

---

## ✅ Learning Outcomes

| Task | Focus Area | Learning Outcome |
|:----|:------------|:-----------------|
| 1 | Sampling & Aliasing | Understand Nyquist limit and importance of prefiltering |
| 2 | Linear Filtering | Master convolution and filter properties |
| 3 | Edge Detection | Compare gradient-based and multi-stage edge methods |
| 4 | Geometric Transformations | Apply affine and projective transformations correctly |

---

## 📄 License

This project is developed for **academic use** under the Computer Vision course at **Central Asian University**.
