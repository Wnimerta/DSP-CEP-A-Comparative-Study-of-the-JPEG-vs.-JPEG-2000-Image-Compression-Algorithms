# 🖼️ Efficient Storage and Transmission: A Comparative Study of JPEG vs. JPEG2000

A Python-based project comparing the **JPEG** (DCT-based) and **JPEG2000** (Wavelet-based) image compression algorithms for efficient storage and quality.

---

## 🎓 Project Info

* **University**: Sukkur IBA University
* **Department**: Computer Systems Engineering
* **Project Title**: Efficient Storage and Transmission: A Comparative Study of JPEG vs. JPEG2000
* **Submitted By**: Nimerta Wadhwani
* **Supervisor**: Dr. Junaid Ahmed Bhatti

---

## 🌎 Abstract

This project implements and compares JPEG and JPEG2000 compression techniques using Python. It evaluates compression **performance**, **image quality**, and **compression ratio** using metrics like **PSNR**, **SSIM**, and visual assessments. Results show JPEG2000 offers higher visual quality at similar or better compression ratios, while JPEG remains simpler and faster.

---

## 🚀 Objectives

* Implement JPEG and JPEG2000 compression algorithms
* Compare PSNR, SSIM, and Compression Ratio
* Visualize results and artifact patterns
* Analyze trade-offs between speed, quality, and compression

---

## 🔧 Tools & Libraries

| Tool/Library | Purpose                               |
| ------------ | ------------------------------------- |
| OpenCV       | JPEG compression and color conversion |
| PyWavelets   | Wavelet transform for JPEG2000        |
| Matplotlib   | Visualization of results              |
| Scikit-Image | SSIM, PSNR computation                |
| NumPy        | Numerical processing                  |
| os           | File size & compression ratio checks  |

---

## 🔍 Methodology

### 1. JPEG (DCT-Based)

* Image divided into 8x8 blocks
* DCT transformation applied
* Quantization based on quality factor
* Huffman encoding (via OpenCV)

### 2. JPEG2000 (Wavelet-Based)

* 3-level Haar Wavelet decomposition
* Soft thresholding simulates compression
* Reconstruction and clipping
* RGB color recovery from YCbCr

### 3. Metrics Used

* **PSNR**: Measures fidelity (higher is better)
* **SSIM**: Measures perceptual similarity (closer to 1 is better)
* **Compression Ratio (CR)**: Original size / Compressed size

---

## 🔄 Experimental Setup

* Input: Color image (PNG/JPG)
* JPEG: Quality levels tested at 10, 30, 50, 70, 90
* JPEG2000: Compression ratios of 5, 10, 20, 30
* Metrics plotted and visualized for analysis

---

## 📊 Results Summary

| Metric | JPEG (Q=50) | JPEG2000 (R=10) |
| ------ | ----------- | --------------- |
| PSNR   | 39.35 dB    | 26.81 dB        |
| SSIM   | 0.9678      | 0.7985          |
| CR     | 0.61        | 1.67            |

### 🌐 Observations

* JPEG2000 preserves more **edges and textures**
* JPEG introduces **blocking artifacts** at low quality
* JPEG2000 achieves better quality at higher compression levels

---

## 🔫 Trade-off Analysis

| Factor                   | JPEG             | JPEG2000                    |
| ------------------------ | ---------------- | --------------------------- |
| Compression Speed        | Fast             | Slower (more compute)       |
| Visual Quality @ High CR | Blocky artifacts | Smooth, edge-preserving     |
| Scalability              | Low              | High (supports progressive) |
| Support & Compatibility  | Universal        | Limited                     |
| Lossless Option          | No               | Yes                         |

---

## 🤔 Limitations & Future Work

* Use real JPEG2000 encoders with EBCOT for accuracy
* Test on multiple image types (medical, faces, text)
* Compare with modern codecs (WebP, AVIF, HEIC)
* Apply adaptive quantization and hybrid methods

---

## 📆 Implementation Flow

1. Load and preprocess image (OpenCV)
2. Apply JPEG and JPEG2000 compression functions
3. Compute PSNR, SSIM, and CR
4. Visual comparison using Matplotlib
5. Save and export results/plots

---

## 📖 References

1. Skodras et al. (2001). *JPEG2000 Standard*. IEEE SPM.
2. Pennebaker & Mitchell (1992). *JPEG Compression Standard*.
3. ResearchGate/WJARR studies on JPEG vs JPEG2000.
4. PyWavelets and scikit-image documentation.

---

> ✨ *Balancing compression, quality, and performance through transform coding.*
