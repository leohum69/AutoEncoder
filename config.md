# Autoencoder Configuration

## Model Setup

| Parameter | Value |
| --- | --- |
| Input dimension | 79 |
| Encoding dimension (bottleneck) | 16 |
| Compression ratio | 4.94x |
| Epochs | 100 |
| Learning rate | 1e-3 |

## Reconstruction Error Statistics (Benign Test Data)

### Mean Squared Error (MSE)

| Metric | Value |
| --- | --- |
| Mean | 0.136411 |
| Median | 0.003262 |
| Std dev | 13.737039 |
| Min | 0.001330 |
| Max | 1978.635485 |

### Mean Absolute Error (MAE)

| Metric | Value |
| --- | --- |
| Mean | 0.063631 |
| Median | 0.040562 |
| Std dev | 0.243227 |
| Min | 0.024725 |
| Max | 31.142049 |

## Anomaly Detection Thresholds

| Threshold | Value |
| --- | --- |
| 95th percentile | 0.058508 |
| 99th percentile | 0.209656 |
| Mean + 3xStd | 41.347526 |

**Recommendation:** use the 95th percentile threshold for anomaly detection.

- Reconstruction error > 0.058508 indicates a potential anomaly.

## Training Summary

### Dataset

| Item | Value |
| --- | --- |
| Total samples | 484,557 |
| Features | 79 |
| Training samples | 387,643 |
| Test samples | 96,911 |

### Model Architecture

| Item | Value |
| --- | --- |
| Input dimension | 79 |
| Encoding dimension | 16 |
| Compression ratio | 4.94x |
| Total parameters | 15,903 |

### Performance on Benign Data

| Metric | Value |
| --- | --- |
| Mean MSE | 0.136411 |
| Median MSE | 0.003262 |
| Std dev | 13.737039 |

### Anomaly Detection Threshold

- 95th percentile: 0.058508
- Use this threshold to detect malicious traffic.

## Next Steps

4. Adjust the anomaly detection threshold.
5. Use the model in your application for real-time detection.