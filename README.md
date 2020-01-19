# Denoising 3D scanned data

*Technologies:* Python, NumPy, Plotly. <br>
*Topics:* time-series, FFT, denoising by filtering. <br>

## Description

<img src="docs/marble-path.png?raw=true" width="350"/>

In this project, I denoise a series of three-dimensional scanned data to determine the path of a marble ingested by a dog.
I accomplish this by converting the data into the frequency domain using an FFT, averaging the spectra over time, and using
the average spectrum to construct a Gaussian filter. I then denoise the data in the frequency domain using the Gaussian filter,
and convert it back into the spatial domain. The location of the marble can then be found by looking for the peak density in the
spatial data.

You can find more details in the <a href="https://1drv.ms/b/s!AiCY1Uw6PbEfhdxWL0lSvCZrnEAEBA?e=Gcdrud">report</a> for this project.

## Running

To run this project:

```sh
conda env create -f environment.yml
conda activate denoising-3D-scans
python main.py
```