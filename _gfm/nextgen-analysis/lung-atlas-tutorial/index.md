# Exploring single-cell RNA sequencing using COVID-19 lung data
Pranav Kumar Mishra
Wednesday, October 11, 2023

# Exploring single-cell RNA sequencing using COVID-19 lung data

## About

This repository is following an excellent tutorial created by Mark
Sanborn ([@Sanbiomics](https://www.youtube.com/@sanbomics)) on
YouTube<sup>1</sup>. scRNA-seq data is provided by<sup>2</sup>

## Data source

Melms JC, Biermann J, Huang H, Wang Y et al. A molecular single-cell
lung atlas of lethal COVID-19. Nature 2021 Jul;595(7865):114-119. PMID:
33915568

``` sh
# Download the data from GEO Accession
wget https://ftp.ncbi.nlm.nih.gov/geo/series/GSE171nnn/GSE171524/suppl/GSE171524_RAW.tar

# Extract the files
tar -xf GSE171524_RAW.tar -C ./data/
cd data
gunzip *gz
```

## Python packages required

I prefer the python package manager `mamba`, which is a faster form of
the ubiquitous `conda`.

``` sh
# Install dependencies / libaries
mamba env update --file ./python/environment.yaml  --prune
```

## CPU vs. GPU vs. TPU

Using a GPU substantially increases the computational speed of Single
Cell Variation Interface Tools (`scvi-tools`). 8 core CPUs perform about
7 times slower than a Google Colab notebook’s free GPU. I have also
attempted to run the code on a Google Colab TPU-based environment, as
well. However, in my initial tests, the TPU was not detected, and
pytorch (via sc)

### Limitations of Google Colab (Free)

Though it is a great service to explore python code, Google Colab does
not offer enough computer memory (RAM) to successfully run this dataset,
with all samples loaded into adata. In my trial, I was able to combine
together 4 lung donor scRNAseq data files into one `adata` variable
before running out of memory

### My setup

I am running this code on two separate machines for testing purposes.

#### HP Z820

CPU: 16 core, 32 threads RAM: 128 GB GPU: nVidia GeForce RTX 3060

Hypervisor: Windows 10 Pro Virtual Machine: Ubuntu 22.04, with 14 cores,
80GB RAM passed in

<div>

> **Note**
>
> I am currently having difficulty passing in the GPU into the VM. I
> plan to evaluate Proxmox as a hypervisor for an easier GPU passthrough

</div>

### Tiny Machine

CPU: i5-8500 CPU @ 3.00GHz RAM: 16 GB

Hypervisor: Proxmox 7.4 Virtual Machine: Ubuntu 22.04,

<div>

> **Note**
>
> ``` sh
> You can check your machine's hardware with
> cat /proc/cpuinfo
>
> sudo dmidecode --type memory | less
> ```

</div>

## SCVI

### Recommendations from developers

- For scVI, we recommend anywhere from 1,000 to 10,000 HVGs, but it will
  be context-dependent.

<div id="refs" class="references csl-bib-body">

<div id="ref-sanborn2022" class="csl-entry">

<span class="csl-left-margin">1.
</span><span class="csl-right-inline">Sanborn M. Complete single-cell
RNAseq analysis walkthrough \| advanced introduction. Published 2022.
<https://www.youtube.com/watch?v=uvyG9yLuNSE></span>

</div>

<div id="ref-melms2021" class="csl-entry">

<span class="csl-left-margin">2.
</span><span class="csl-right-inline">Melms JC, Biermann J, Huang H, et
al. A molecular single-cell lung atlas of lethal COVID-19. *Nature*.
2021;595(7865):114-119.
doi:[10.1038/s41586-021-03569-1](https://doi.org/10.1038/s41586-021-03569-1)</span>

</div>

</div>
