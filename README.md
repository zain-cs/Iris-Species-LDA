# 🌸 Iris Species Classification with LDA

A Linear Discriminant Analysis (LDA) project for dimensionality reduction and visualization of the classic Iris dataset, demonstrating class separation in a supervised learning context.

## 📋 Overview

This project applies LDA to the Iris dataset to:
- Reduce 4-dimensional feature space to 2 discriminant components
- Maximize class separability between three Iris species
- Visualize decision boundaries and species clusters
- Demonstrate supervised dimensionality reduction

## 🚀 Features

- **Automated Data Preprocessing**: Cleans column names and encodes target labels
- **LDA Transformation**: Projects data onto discriminant axes that maximize class separation
- **Species Classification**: Distinguishes between Setosa, Versicolor, and Virginica
- **Interactive Visualization**: Color-coded scatter plot showing clear species separation
- **Supervised Learning**: Utilizes class labels during dimensionality reduction

## 📊 Dataset

The code expects the **Iris dataset** with the following characteristics:

- **Format**: CSV (comma-separated values)
- **Features**: 4 numeric measurements (sepal length, sepal width, petal length, petal width)
- **Target**: Species classification (Setosa, Versicolor, Virginica)
- **Samples**: 150 observations (50 per species)

### Sample Dataset Structure
```csv
sepal_length,sepal_width,petal_length,petal_width,species
5.1,3.5,1.4,0.2,setosa
7.0,3.2,4.7,1.4,versicolor
6.3,3.3,6.0,2.5,virginica
```

## 🛠️ Installation

### Prerequisites
- Python 3.7+
- Google Colab (for file upload functionality)

### Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## 💻 Usage

### In Google Colab

1. Open the notebook in Google Colab
2. Run all cells
3. Upload your Iris CSV file when prompted
4. View the LDA visualization showing species separation

### Code Structure

```python
# 1. Upload and load Iris dataset (CSV format)
# 2. Clean column names
# 3. Encode species labels (Setosa=0, Versicolor=1, Virginica=2)
# 4. Separate features (X) and target (y)
# 5. Standardize features (zero mean, unit variance)
# 6. Apply LDA (2 components for 3 classes)
# 7. Visualize results with scatter plot
```

## 📈 Output

### Printed Results
- Dataset preview (first 5 rows)
- Confirmation of successful data loading

### Visualization
A scatter plot showing:
- **LD1 vs LD2**: First two linear discriminants
- **Color coding**: Three Iris species (Setosa, Versicolor, Virginica)
- **Clear separation**: Species clusters with minimal overlap
- **Decision boundaries**: Implicit class separation in discriminant space

## 🔍 Methodology

### 1. Data Preprocessing
- Strip whitespace from column names
- Encode species labels using `LabelEncoder`
- Separate features from target variable

### 2. Standardization
```python
StandardScaler()  # Mean=0, Std=1
```

### 3. LDA Transformation
```python
LinearDiscriminantAnalysis(n_components=2)
# For K classes, max components = K-1
# 3 species → 2 discriminant components
```

### 4. LDA vs PCA
| Aspect | LDA | PCA |
|--------|-----|-----|
| **Type** | Supervised | Unsupervised |
| **Goal** | Maximize class separation | Maximize variance |
| **Uses Labels** | Yes | No |
| **Max Components** | K-1 classes | min(features, samples) |

## 📊 Expected Results

The LDA visualization typically shows:
- **Setosa**: Completely separable from other species (left cluster)
- **Versicolor & Virginica**: Partially overlapping (right clusters)
- **LD1**: Captures most class separation (~95%)
- **LD2**: Captures remaining separation (~5%)

## 🎯 Use Cases

- **Species Classification**: Automatic Iris species identification
- **Feature Engineering**: Reduce 4D to 2D while preserving class information
- **Data Visualization**: Plot high-dimensional labeled data in 2D
- **Model Preprocessing**: Create discriminant features for classifiers

## 🧪 Experiment Ideas

1. **Compare with PCA**: Run PCA on same dataset and compare class separation
2. **Add Noise**: Introduce outliers to test robustness
3. **Train Classifier**: Use LDA components as input for SVM/Random Forest
4. **Cross-Validation**: Evaluate classification accuracy using LDA features

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Muhammad Zain**
- GitHub: [@zain-cs](https://github.com/zain-cs)

## 🙏 Acknowledgments

- R.A. Fisher for the Iris dataset (1936)
- scikit-learn for LDA implementation
- seaborn for elegant visualizations
- UCI Machine Learning Repository

## 📚 Further Reading

- [Linear Discriminant Analysis - Wikipedia](https://en.wikipedia.org/wiki/Linear_discriminant_analysis)
- [scikit-learn LDA Documentation](https://scikit-learn.org/stable/modules/lda_qda.html)
- [Fisher's Linear Discriminant](https://en.wikipedia.org/wiki/Linear_discriminant_analysis#Fisher's_linear_discriminant)

## 📧 Contact

For questions or feedback, please open an issue in the repository.

---

⭐ If you found this project helpful, please consider giving it a star!
