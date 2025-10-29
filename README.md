# CNN Hyperparameter Experimentation Script

This script systematically tests different CNN hyperparameters on the MNIST dataset to find the optimal configuration.

## 🎯 What This Script Does

1. **Automatically tests multiple configurations:**
   - Kernel sizes: [3, 5, 7]
   - Learning rates: [0.0001, 0.001, 0.01]
   - Number of convolutional layers: [2, 3]

2. **Generates comprehensive results:**
   - Training curves for each experiment
   - Comparison visualizations
   - Detailed report with all results
   - Best model saved as `.pth` file

3. **Total experiments:** 18 (3 kernel sizes × 3 learning rates × 2 layer configurations)
   - **Estimated runtime:** ~50-60 minutes on Google Colab with GPU

## 📋 How to Use
1. Open Google Colab
2. Create a new notebook
3. Copy-paste the entire content of `train_cnn_experiments.py`
4. Click "Runtime" → "Run all"
5. Wait for all experiments to complete (~50-60 minutes)
6. Download the generated files


## 📊 Generated Files

After running the script, you'll get these files in the `cnn/` directory:

| File | Description |
|------|-------------|
| `RESULTS_REPORT.md` | Complete markdown report with all results |
| `experiment_results.csv` | CSV table with all experiment results |
| `experiment_config.json` | Configuration details in JSON format |
| `best_cnn_model.pth` | Best model weights |
| `best_model_training_curves.png` | Training curves for the best model |
| `kernel_size_comparison.png` | Comparison of different kernel sizes |
| `learning_rate_comparison.png` | Comparison of different learning rates |
| `accuracy_heatmap.png` | Heatmap showing all combinations |


✅ **Short report with:**
- Plot of loss and accuracy on training and validation sets
- Tested hyperparameters (kernel size, learning rate, layers)
- Test accuracy of the best model

✅ **This script provides:**
- All required plots automatically
- Comprehensive report in markdown
- Detailed comparison of all hyperparameters
- Best model identification


## 🐛 Troubleshooting

### "Out of memory" error
- Reduce `BATCH_SIZE` to 64 or 32
- Use only 2 convolutional layers
- Ensure GPU is enabled in Colab

### "Runtime disconnected"
- The full experiment takes ~50-60 minutes
- Keep the Colab tab active
- Consider running fewer experiments

## 📚 Additional Notes

- **All comments are in English** as requested
- The script follows PyTorch best practices
- Results are reproducible (same hyperparameters = same results)
- Compatible with Google Colab's free GPU

---

**Questions?** Check the comments in the script or refer to the PyTorch documentation.
