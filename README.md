# RGB-to-Grayscale Performance Analysis

## Comparative Analysis of the Computational Performance of Three RGB-to-Grayscale Conversion Algorithms

This repository contains the experimental implementation and evaluation of three RGB-to-grayscale image conversion algorithms using Python, NumPy, and OpenCV.

The study compares the computational performance and visual characteristics of the following methods:

1. **Simple Average:** Calculates the arithmetic mean of the red, green, and blue channels.
2. **Luma Weighted Method:** Applies weighted coefficients to the RGB channels according to their contribution to perceived brightness.
3. **Desaturation Method:** Calculates the average between the maximum and minimum values of the RGB channels.

## Research Objective

The objective of this study is to compare the computational performance of three grayscale conversion algorithms under equivalent experimental conditions, considering their execution times and the visual characteristics of the resulting images.

## Experimental Setup

The experiment was conducted using the following conditions:

- **Platform:** Google Colab.
- **Programming language:** Python 3.13.18.
- **NumPy:** 2.4.6.
- **OpenCV:** 5.0.0.
- **Operating system:** Linux, 64-bit.
- **Available computational resources:** 2 logical CPUs.
- **Dataset:** 10 RGB images.
- **Image resolution:** 1920 × 1080 pixels.
- **Repetitions:** 50 executions per image and method.
- **Timing function:** `time.perf_counter_ns()`.

Each algorithm was executed independently for every image. One preliminary execution was performed before recording the 50 measurements.

## Repository Structure

```text
RGB-to-Grayscale-Performance-Analysis/
│
├── data/
│   ├── README.md
│   └── 10 original RGB images
│
├── notebooks/
│   ├── README.md
│   └── RGB_to_Grayscale_Experiment.ipynb
│
├── results/
│   ├── README.md
│   ├── resultados_por_imagen.csv
│   ├── resumen_general.csv
│   └── Figura_3_tiempo_ejecucion.png
│
└── README.md
```

## Experimental Results

The original experimental measurements produced the following average execution times:

| Conversion Method | Average Execution Time |
|---|---:|
| Simple Average | 15.37 ms |
| Luma Weighted Method | 18.85 ms |
| Desaturation Method | 168.77 ms |

The Simple Average method presented the lowest average execution time, followed by the Luma Weighted Method. The Desaturation Method required substantially more processing time in the tested implementation.

The complete measurements and statistical results are available in the `results/` directory.

## How to Reproduce the Experiment

1. Open the Jupyter notebook located in the `notebooks/` directory using Google Colab.
2. Download the ten original RGB images from the `data/` directory.
3. Execute the image upload cell and select the ten JPEG files.
4. Run the notebook cells sequentially.
5. The images will be resized to 1920 × 1080 pixels.
6. The three conversion algorithms will be evaluated using 50 repetitions per image and method.
7. The notebook will generate the experimental CSV files and comparison plots.

**Note:** The original experimental measurements are preserved in the `results/` directory. Repeating the experiment may produce slightly different execution times depending on the computational resources assigned by Google Colab.

## Data Availability and Reproducibility

The original RGB images, Python implementation, experimental measurements, statistical summaries, and comparative figure are provided in this repository to facilitate inspection and reproduction of the experiment.

## Technologies Used

- Python
- Google Colab
- NumPy
- OpenCV
- Pandas
- Matplotlib

## Author

Ulises Santos López

## License

Please refer to the repository license for information about the use and distribution of the materials.
