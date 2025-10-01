# 📊 Decline Curve Analysis with Machine Learning

An interactive web-based tool for analyzing oil and gas production decline curves using both traditional petroleum engineering methods and advanced machine learning techniques. Built entirely with JavaScript, this tool runs directly in your browser without requiring any backend servers or Python installations.

## 🔗 Live Demo

**[Try it live here!](https://mpaydayesh.github.io/Decline-Curve-Analysis-with-Machine-Learning/)**

## 🌟 Features

### Traditional Decline Models
- **Exponential Decline** - Constant percentage decline rate
- **Hyperbolic Decline** - Variable decline rate with b-factor
- **Harmonic Decline** - Special case of hyperbolic (b=1)
- Adjustable parameters (qi, Di, b) with real-time visualization

### Machine Learning Models
- **Exponential Decay (ML-Optimized)** - Gradient descent parameter optimization
- **Power Law (ML-Optimized)** - Automated parameter tuning for shale/tight reservoirs
- **Polynomial Regression** - With monotonic decline constraints and regularization
- **Physics-Guided Neural Network** - Combines ML flexibility with domain physics
- **Ensemble Method** - Weighted voting from multiple models
- **ARIMA Time Series** - Statistical forecasting with trend damping
- **Support Vector Regression** - RBF kernel with decline-aware extrapolation
- **Random Forest** - Tree ensemble with exponential extrapolation
- **Gradient Boosting** - Sequential ensemble for high accuracy
- **Neural Network** - Multi-layer perceptron with hidden layers
- **LSTM** - Recurrent network for time series patterns

### Interactive Features
- 🎛️ Real-time parameter adjustment with sliders
- 📈 Dynamic visualization with D3.js
- 🏷️ Train/test data split visualization
- 📊 Performance metrics (RMSE, MAE, R², EUR)
- 🔮 Forecasting up to 60 months
- 📉 Side-by-side comparison of traditional vs ML predictions
- 💾 Built-in sample data for 4 wells
- 📋 CSV data import capability

## 🚀 Quick Start

### Online Version
Visit the deployed application at: https://mpaydayesh.github.io/Decline-Curve-Analysis-with-Machine-Learning/

### Local Installation
```bash
# Clone the repository
git clone https://github.com/mpaydayesh/Decline-Curve-Analysis-with-Machine-Learning.git

# Navigate to the project directory
cd Decline-Curve-Analysis-with-Machine-Learning

# Open index.html in your browser
# On Mac:
open index.html
# On Windows:
start index.html
# On Linux:
xdg-open index.html
```

### Usage Instructions
1. **Load Data**
   - Click "Use Sample Data" to load built-in production data for 4 wells
   - Or click "Paste CSV Data" to use your own data

2. **Select ML Technique**
   - Choose from dropdown menu (Polynomial recommended for beginners)
   
3. **Train Model**
   - Adjust training parameters if needed
   - Click "Train ML Model" button
   
4. **Generate Predictions**
   - Adjust forecast period slider
   - Click "Predict" to see results
   
5. **Compare Models**
   - Try different ML techniques
   - Compare ML predictions (green dashed) vs traditional (red solid)

## 💻 Technologies Used

### Frontend
- **HTML5/CSS3** - Modern, responsive design with gradients and animations
- **JavaScript (ES6+)** - Pure client-side implementation, no backend required
- **D3.js v7.8.5** - Interactive data visualization
- **Math.js v11.11.0** - Matrix operations for polynomial regression

### ML Implementation
All machine learning algorithms are implemented from scratch in JavaScript:
- Custom gradient descent optimization
- Manual backpropagation for neural networks
- Matrix operations using Math.js
- No Python or server dependencies required

## 📁 Project Structure

```
Decline-Curve-Analysis-with-Machine-Learning/
│
├── index.html          # Complete application (HTML, CSS, JS, and sample data)
├── README.md           # Documentation (this file)
└── LICENSE            # MIT License
```

**Note:** The entire application is contained in a single `index.html` file, including:
- HTML structure
- CSS styling
- JavaScript code for all ML algorithms
- Embedded sample production data
- D3.js visualizations

## 🧮 Mathematical Models

### Traditional Hyperbolic Decline
```
q(t) = qi / (1 + b × Di × t)^(1/b)
```
Where:
- `qi` = Initial production rate
- `Di` = Initial decline rate
- `b` = Decline exponent (0-1)
- `t` = Time

### ML-Optimized Exponential
```
q(t) = a × exp(-b × t) + c
```
Parameters optimized using gradient descent with adaptive learning rate.

### Physics-Guided Neural Network
Combines neural network predictions with physical decline models:
```
prediction = w × physics_model + (1-w) × neural_network
```

## 📊 Built-in Sample Data

The application includes sample production data for 4 wells embedded directly in the code:
- **Well 1**: 500 E3m3 initial production, smooth decline pattern
- **Well 2**: 700 E3m3 initial production, erratic decline pattern  
- **Well 3**: 800 E3m3 initial production, stepped decline pattern
- **Well 4**: 600 E3m3 initial production, seasonal variations

## 📋 Using Your Own Data

### Data Format Requirements
Your CSV should have these columns:
```csv
Prod Date,Unformatted_UWI,Monthly Gas (E3m3)
2012-01-09,w1,450
2012-02-09,w1,420
2012-03-11,w1,395
...
```

### How to Import
1. Prepare your CSV file with the required columns
2. Open the CSV in a text editor and copy all content
3. Click "Paste CSV Data" in the application
4. Paste your data in the text area
5. Click "Load Pasted Data"

## 🎓 Educational Value

This tool is designed for:
- **Petroleum Engineers** learning ML applications in reservoir engineering
- **Data Scientists** interested in time series forecasting for energy
- **Students** studying decline curve analysis
- **Researchers** exploring hybrid physics-ML models
- **Industry Professionals** needing quick decline curve analysis

## 🔧 Configuration

### Adjustable Parameters

#### Traditional Models
- Initial Production (qi): 100-1500 E3m3
- Decline Rate (Di): 0.01-0.20 /year
- Decline Exponent (b): 0-1

#### ML Settings
- Training Data Split: 50-95%
- Learning Rate: 0.001-0.1
- Epochs/Iterations: 10-500
- Polynomial Degree: 2-8
- Forecast Period: 0-60 months

## 📈 Performance Metrics

The tool calculates and displays:
- **RMSE** (Root Mean Square Error) - Average prediction error
- **MAE** (Mean Absolute Error) - Average absolute difference
- **R²** (Coefficient of Determination) - Goodness of fit (1.0 is perfect)
- **EUR** (Estimated Ultimate Recovery) - 30-year cumulative production

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Areas for Improvement
- Add more ML models (XGBoost, Prophet)
- Implement uncertainty quantification
- Add oil production support (currently gas only)
- Export results to Excel/CSV
- Add more visualization options
- Implement cross-validation
- Add API support for real-time data
- Mobile responsive design improvements
- Add unit selection (metric/imperial)

## 📈 Performance Considerations

- **Dataset Size**: Optimized for wells with 10-500 data points
- **Browser Compatibility**: Chrome, Firefox, Safari, Edge (latest versions)
- **Memory Usage**: ~50MB for typical datasets
- **Training Time**: <1 second for most models
- **No Installation Required**: Runs entirely in browser

## 🐛 Known Issues

1. File upload API not available in some environments - use paste option instead
2. Tree-based models (Random Forest, Gradient Boosting) use exponential extrapolation for forecasting as trees cannot naturally extrapolate
3. LSTM implementation is simplified for browser performance
4. Very large datasets (>1000 points) may cause browser slowdown

## 📚 References

- Arps, J.J. (1945). "Analysis of Decline Curves." Transactions of the AIME, 160(01), 228-247.
- Fetkovich, M.J. (1980). "Decline Curve Analysis Using Type Curves." JPT, 32(06), 1065-1077.
- Valkó, P.P., & Lee, W.J. (2010). "A Better Way to Forecast Production from Unconventional Gas Wells." SPE Annual Technical Conference.
- Machine Learning implementations based on standard algorithms from scikit-learn documentation

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Author

**M. Paydayesh** - [GitHub Profile](https://github.com/mpaydayesh)

## 🙏 Acknowledgments

- Thanks to the D3.js community for excellent visualization tools
- Math.js team for matrix operation support
- Petroleum engineering community for domain knowledge
- Open source ML community for algorithm references
- Claude AI for implementation assistance

## 📞 Contact

- **Repository**: [https://github.com/mpaydayesh/Decline-Curve-Analysis-with-Machine-Learning](https://github.com/mpaydayesh/Decline-Curve-Analysis-with-Machine-Learning)
- **Live Demo**: [https://mpaydayesh.github.io/Decline-Curve-Analysis-with-Machine-Learning/](https://mpaydayesh.github.io/Decline-Curve-Analysis-with-Machine-Learning/)
- **Issues**: [Report bugs or request features](https://github.com/mpaydayesh/Decline-Curve-Analysis-with-Machine-Learning/issues)

For questions or support, please open an issue on GitHub.

---

**⚡ Fun Fact:** This entire application runs in your browser without any server calls, making it perfect for confidential production data analysis!

**🌐 Browser-Based ML:** All machine learning algorithms are implemented in pure JavaScript - no Python, no servers, just your browser doing the heavy lifting!

**📦 Single File Application:** The entire tool is contained in one HTML file - no dependencies to install, no build process required!
