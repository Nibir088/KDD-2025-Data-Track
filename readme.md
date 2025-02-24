# IrrMap

## Overview
The **IrrMap** is designed to process satellite imagery data from LandSat and Sentinel missions for developing and training machine learning models for crop classification. This repository includes tools for data preprocessing, feature extraction, model training, and evaluation.

## Repository Structure
```
KDD-2025-Data-Track/
│── LandSat_Processing/    # Scripts for downloading and processing LandSat imagery
│── Sentinel_Processing/   # Scripts for retrieving and processing Sentinel imagery
│── Model_Training/        # Machine learning model training scripts and configurations
│── train_test_split/      # Scripts for splitting data into training and test sets
│── Crop-Groups.csv        # Crop classification mapping file
│── requirements.txt       # List of dependencies
│── README.md              # Documentation
```

## Data Processing Workflow
### LandSat Data Processing
- **Data Acquisition**: Downloading LandSat data.
- **Preprocessing**:
  - Atmospheric correction
  - Radiometric calibration
  - Resampling and reprojection
  - Cloud masking
- **Feature Extraction**:
  - Vegetation indices (NDVI, EVI)
  - Texture features
  - Spectral band combinations

### Sentinel Data Processing
- **Data Retrieval**: Fetching Sentinel-1 (SAR) and Sentinel-2 (multispectral) imagery.
- **Preprocessing**:
  - Geometric and radiometric corrections
  - Normalization and resampling
  - Cloud removal
- **Feature Engineering**:
  - Polarimetric decomposition (SAR)
  - Spectral indices calculation
  - Temporal feature stacking

## Model Training Pipeline
1. **Data Preparation**:
   - Load and merge LandSat and Sentinel data
   - Normalize and scale features
2. **Model Selection**:
   - Deep Learning: `Resnet34`
3. **Training Process**:
   - Hyperparameter tuning
   - Loss function optimization
4. **Evaluation Metrics**:
   - Accuracy, Precision, Recall, F1-Score, IoU


## Crop Classification Mapping
The `Crop-Groups.csv` file maps crop types into broader classifications:
- Specific crops (e.g., Wheat, Maize, Rice)
- Crop groups (e.g., Cereal Grains, Legumes, Fruits)

## Installation and Setup
### Clone the Repository
```bash
git clone https://github.com/Nibir088/KDD-2025-Data-Track.git
cd KDD-2025-Data-Track
```
### Install Dependencies
```bash
pip install -r requirements.txt
```
### Process Data
```bash
cd LandSat_Processing
python process_landsat.py

cd Sentinel_Processing
python process_sentinel.py
```
### Train the Model
```bash
cd Model_Training
python train_model.py
```

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch.
3. Make changes and commit with clear messages.
4. Submit a pull request.

## License

## Contact & Support
For issues or inquiries, open an issue on [GitHub Issues](https://github.com/Nibir088/KDD-2025-Data-Track/issues).

