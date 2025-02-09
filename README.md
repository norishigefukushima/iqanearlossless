# MIDD: Meikoudai Image Distortion Dataset
Subjective assessment dataset of visually lossless ratio by absolute binary decision (ABD) for IQA of visually-lossless compression.

**Dataset type**
* MIDD-GAR (Gray and Resolution, JPEG, WebP, HIEF), QoMEX2023 [1]
* MIDD-CAP (Color and Patch, JPEG), submitted 2025 [2] 

**Link**
* [Github](https://github.com/norishigefukushima/iqanearlossless)
* [Direct download link (MID-GAR 30.2 MB)](./MIDD-GAR.zip)
* [Direct download link (MID-CAP 117.2 MB)](./MIDD-CAP.zip)

Meikoudai is an abbreviation of Nagoya Institute of Technology in Japanese.

The dataset name MIDD (QoMEX2023) has been renamed to MIDD-GAR due to the addition of a new dataset (MIDD-CAP) (2/7/2025).

Meikoudai is an abbreviation of Nagoya Institute of Technology in Japanese.

The dataset name MIDD (QoMEX2023) has been renamed to MIDD-GAR due to the addition of a new dataset (MIDD-CAP) (2/7/2025).

## 1. MIDD-GAR (Gray and Resolution, JPEG, WebP, HIEF), QoMEX2023
[1] Soichiro Honda, Yoshihiro Maeda, and Norishige Fukushima,
"Dataset of Subjective Assessment for Visually Near-Lossless Image Coding based on Just Noticeable Difference,"
in Proc. International Conference on Quality of Multimedia Experience (QoMEX), 2023.
[[IEEE Xplore]](https://ieeexplore.ieee.org/document/10178524)
[[pdf]](https://fukushima.web.nitech.ac.jp/paper/2023_qomex_honda.pdf)

```
@INPROCEEDINGS{honda2023dataset,
  author={Honda, Soichiro and Maeda, Yoshihiro and Fukushima, Norishige},
  booktitle={Proceedings of International Conference on Quality of Multimedia Experience (QoMEX)}, 
  title={Dataset of Subjective Assessment for Visually Near-Lossless Image Coding based on Just Noticeable Difference}, 
  year={2023},
  pages={236-239},
  doi={10.1109/QoMEX58391.2023.10178524}
}
```
## 2. MIDD-CAP (Color and Patch, JPEG), submitted 2025.
[2] Soichiro Honda, Yoshihiro Maeda, Osamu Watanabe, and Norishige Fukushima,
"A Multi-Level Patch Dataset for JPEG Image Quality Assessment by Absolute Binary Decision,"
submitted, 2025.

```
@INPROCEEDINGS{honda2023dataset,
  author={Honda, Soichiro and Maeda, Yoshihiro and Watanabe, Osamu and Fukushima, Norishige},
  booktitle={submitted}, 
  title={A Multi-Level Patch Dataset for JPEG Image Quality Assessment by Absolute Binary Decision}, 
  year={2025},
  pages={9 page},
}
```

# Related Project

[GitHub link](https://fukushimalab.github.io/LLF/)

On this page, the results of upsampling using the same protocol and subjective assessment are published.
Rather than simple upsampling, high-resolution guided upsampling such as joint bilateral upsampling is used.
The results of subjective assessment of the approximate processing that accelerates processing speed by guided upsampling of the low-resolution image processed with the high-resolution image before processing.

[3] Teppei Tsubokawa, Hiroshi Tajima, Yoshihiro Maeda, and Norishige Fukushima “Local Look-Up Table Upsampling for Accelerating Image Processing,” Multimedia Tools and Applications, 2023.