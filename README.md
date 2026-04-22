# MobiHoc 2026 - Adaptive Sampling for Federated Learning
This is the open source code for the paper "Adaptive Data Admission and Retention for Streaming Federated Learning".

## 📁 Repository Structure

```
MOBIHOC2026_AdaSampling_GitHub/
├── MNIST/
│   └── run_streaming_mnist.py      # MNIST experiments
├── CIFAR/
│   └── run_streaming_cifar.py      # CIFAR-10 experiments
├── ImageNette/
│   └── run_streaming_cifar.py      # ImageNette experiments
└── README.md
```

## 🚀 Quick Start

### MNIST
```bash
cd MNIST
python3 run_streaming_mnist.py --policy optimal --epochs 100 --local_epochs 10
```

### CIFAR-10
```bash
cd CIFAR
python3 run_streaming_cifar.py --policy optimal --epochs 100 --local_epochs 10
```

### ImageNette
```bash
cd ImageNette
python3 run_streaming_cifar.py --policy optimal --epochs 100 --local_epochs 10
```

## 🎯 Supported Policies

1. **optimal**: K-Step Optimal constant admission Policy (K=10)
2. **dpp**: ACDPP Policy
3. **oracle**: K=1 Oracle Policy
4. **hybrid**: 5 Dynamic + 5 Static Policy

## ⚙️ Key Parameters

### MNIST
- Model: Multinomial Logistic Regression (7,850 params)
- Buffer sizes: [8, 9, 10, 11, 12, 8, 9, 10, 11, 12]
- Cost budget: 55.0
- Cost range: [1, 10]

### CIFAR-10
- Model: ResNet-9 (~6.58M params)
- Buffer sizes: [16, 18, 20, 22, 24, 16, 18, 20, 22, 24]
- Cost budget: 110.0
- Cost range: [1, 10]

### ImageNette
- Model: ResNet-9 (~6.58M params)
- Buffer sizes: [32, 36, 40, 44, 48, 32, 36, 40, 44, 48]
- Cost budget: 220.0
- Cost range: [1, 10]

## 📊 Output

Results are saved to:
- `~/Desktop/MobiHoc26_*/experiment_outputs/`
  - `*_optimal_run1.pth`: Trained model
  - `history_optimal_run1.json`: Training history
  - `config_optimal_run1.json`: Configuration

## 📝 Citation

```bibtex
@inproceedings{mobihoc2026_adasampling,
  title={Adaptive Sampling for Federated Learning with Streaming Data},
  booktitle={MobiHoc 2026},
  year={2026}
}
```

## 📧 Contact

For questions or issues, please open an issue on GitHub.
