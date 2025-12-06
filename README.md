# mbb-cc66v-1-assignment-1

multimodal modeling task using a tweet classification dataset

## autors

- Manuel Bórquez Basáez
- Paola Rioseco

## hardware

### opción 1

```json
CPU info:
{
  "processor": "Intel64 Family 6 Model 63 Stepping 2, GenuineIntel",
  "physical_cores": 18,
  "logical_cores": 36,
  "max_freq_mhz": 2301.0,
  "current_freq_mhz": 1200.0,
  "architecture": "AMD64",
  "platform": "Windows-10-10.0.26100-SP0"
}

GPU info:
[
  {
    "name": "NVIDIA GeForce RTX 3090",
    "memory_total_mb": "24576 MiB",
    "driver_version": "581.80",
    "cuda_version": "13.0",
    "temperature": "32 C"
  }
]
```

### opción 2

- **Model**: MacBook Pro 14" (2023)  
- **Chip**: Apple M2 Max (12-core CPU, 38-core GPU, 16-core Neural Engine)  
- **Architecture**: arm64 (Apple Silicon)  
- **Memory**: 32 GB unified RAM  
- **Graphics**: Integrated Apple GPU with full Metal 4 support  
- **OS**: macOS 26.0 (Build 25A354)  

## conda environment setup

```bash
# definición de entorno conda
conda env create -f environment.yml

# activación del entorno
conda activate mbb-cc66v-1-assignment-1

# registro del kernel
python -m ipykernel install --user --name mbb-cc66v-1-assignment-1 --display-name "Python (mbb-cc66v-1-assignment-1)"

# actualizar el entorno
conda env update --file environment.yml --prune 

# reinicio / limpieza
conda deactivate
conda clean --all --yes
conda remove -n mbb-cc66v-1-assignment-1 --all
```

## gpu

```bash
# verificación de acceso a GPU integrada al mac
python -c "import torch; print('PyTorch:', torch.__version__); print('Torchvision:', __import__('torchvision').__version__); print('MPS available:', torch.backends.mps.is_available())"
```
