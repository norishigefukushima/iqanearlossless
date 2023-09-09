# MIDD: Meikoudai Image Distortion Dataset
Subjective assessment of JND for IQA of near-lossless compression (JPEG, WebP, HIEF)

* [Web](https://norishigefukushima.github.io/iqanearlossless/)
* [Github](https://github.com/norishigefukushima/iqanearlossless)
* [direct download link](./MIDD.zip)

Meikoudai is an abbreviation of Nagoya Institute of Technology in Japanese.

# Paper
Soichiro Honda, Yoshihiro Maeda, and Norishige Fukushima,
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
  doi={10.1109/QoMEX58391.2023.10178524}}
```

# Specification
* Number of images: 10
* Resolution: 512x512 (grayscale)
* Number of dpi types: 2 (512x512(1x1), 1024x1024(2x2))
* Coding types: 4 (JPEG, WebP without DF (off), WebP with DF (on), HEIF)
	* DF: deblocking filter
* Number of distortions (QPs): 5 for each distortion and size
  
|Codec    |Size     |QPs                |
|---------|:-------:|-------------------|  
|JPEG     |  512x512| 70, 60, 50, 35, 20|
|JPEG     |1024x1024| 90, 80, 70, 60, 50|
|WebP(on) |  512x512| 70, 60, 50, 35, 20|
|WebP(on) |1024x1024| 90, 80, 70, 60, 50|
|WebP(off)|  512x512| 70, 60, 50, 35, 20|
|WebP(off)|1024x1024| 90, 80, 70, 60, 50|
|HEIF     |  512x512| 45, 40, 35, 30, 25|
|HEIF     |1024x1024| 55, 50, 45, 40, 35|

* Number of subjects: 30 per distortion image
* Total number of judgments: 10x2x4x5x30=12,000
* Condition: controlled laboratory environment
* Display: EIZO CS 270 (27inch  2560x1440 / IPS)
* Viewing distance: 0.5m

# Protocol
* Showing side-by-side original and distorted images at random from 200 distortion images.
	* no dependency on images, distortion types, or distortion levels.
	* naive test without acceleration: bi-selection, adjustment, etc.
	* dependency for dpi: 512x512 image test and then 1024 x 1024 image test.
* Subjects have up to 12 seconds for a judgment.
* The judgment is a binary decision: same or not.
* Experiment time: 2 hours per subject for 400 images with 3 breaking terms.

# Explanation of directory structure
## source image
The 10 source images are contained in the following directory.
```
source_image/kodim(image number).png
```
Source images are losslessly compressed by OptiPNG.

## compression image
The distorted images are contained in the following directory.
```
compression_image/kodim(image number)\_(quality rate)\_(compression metrix).(filename extention)
```

HEIF images are decoded and then lossless compressed by OptiPNG for usability.
JPEG and WebP are their own formats.

## identification\_ratios\_data
The identification ratios between the original and compressed images are listed.
The unit of identification ratios values are %.

* data.xlsx: 512x512
* data200.xlsx: 1024x1024

## data\_per\_participants
The data for each of the 30 participants is listed individually.
The images that participants judged to be the same are marked as "1", and those judged to be different are marked as "0".

* data\_individual.xlsx: 512x512
* data200\_individual.xlsx: 1024x1024
