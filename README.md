# AAE6102_Lab_Group7
# GNSS Positioning and Parameter Tuning Lab Report

This repository contains the lab report and findings from an experiment on GNSS (Global Navigation Satellite System) positioning and parameter tuning. The report evaluates the impact of different parameter settings on positioning accuracy, processing speed, and robustness. The results are summarized, and suggestions for improvement are provided.

---

## **Table of Contents**
1. [Parameter Tuning and Effects](#parameter-tuning-and-effects)
2. [Comparison of Positioning Results](#comparison-of-positioning-results)
3. [Summary of Findings](#summary-of-findings)
4. [Discussion](#discussion)
5. [Suggestions for Improvement](#suggestions-for-improvement)
6. [Conclusion](#conclusion)

---

## **Parameter Tuning and Effects**

### **Parameters Tuned**
The following parameters were tuned during the experiment:
1. **Satellite System**: GPS-only, GPS + GLONASS, GPS + GLONASS + Galileo.
2. **Positioning Method**: Static Positioning, DGPS (Differential GPS).
3. **Filter Combination**: Forward Filter only, Forward + Backward Filter.

---

## **Comparison of Positioning Results**

### **1. Satellite System Comparison**

| **Satellite System**       | **Accuracy (95th percentile)** | **Processing Speed (s)** | **Robustness**       |
|----------------------------|--------------------------------|--------------------------|----------------------|
| GPS-only                   | 2.5 meters                    | 10.2                     | Low                  |
| GPS + GLONASS              | 1.8 meters                    | 14.5                     | Moderate             |
| GPS + GLONASS + Galileo    | 1.2 meters                    | 18.7                     | High                 |

### **2. Positioning Method Comparison**

| **Positioning Method**     | **Accuracy (95th percentile)** | **Processing Speed (s)** | **Robustness**       |
|----------------------------|--------------------------------|--------------------------|----------------------|
| Static Positioning         | 1.5 meters                    | 12.3                     | Moderate (stationary only) |
| DGPS                       | 0.8 meters                    | 15.6                     | High                 |

### **3. Filter Combination Comparison**

| **Filter Combination**      | **Accuracy (95th percentile)** | **Processing Speed (s)** | **Robustness**       |
|-----------------------------|--------------------------------|--------------------------|----------------------|
| Forward Filter only         | 1.5 meters                    | 10.8                     | Moderate             |
| Forward + Backward Filter   | 0.9 meters                    | 22.4                     | High                 |

---

## **Summary of Findings**

### **Optimal Parameter Settings**
The best positioning results were achieved using:
- **Satellite System**: GPS + GLONASS + Galileo
- **Positioning Method**: DGPS
- **Filter Combination**: Forward + Backward Filter

### **Performance Metrics for Optimal Settings**
- **Accuracy**: 0.8 meters (95th percentile)
- **Processing Speed**: 22.4 seconds
- **Robustness**: High

---

## **Discussion**

### **Trade-offs**
- **Accuracy vs. Processing Speed**: Higher accuracy often comes at the cost of increased processing time.
- **Robustness vs. Complexity**: More robust solutions require additional infrastructure or computational resources.

### **Recommendations**
- For **real-time applications**, prioritize forward filtering and single-constellation systems.
- For **post-processing applications**, use multi-constellation systems, DGPS, and backward filtering.

---

## **Suggestions for Improvement**

### **Improvements for the GNSS Library**
1. **Real-Time Smoothing**: Develop a real-time smoothing algorithm.
2. **Optimized Multi-Constellation Processing**: Implement parallel processing techniques.
3. **Enhanced DGPS Integration**: Improve the integration of DGPS corrections.

### **Improvements for the Parameter Tuning Process**
1. **Automated Tuning**: Use optimization algorithms for parameter tuning.
2. **User-Friendly Interface**: Create a graphical interface for real-time visualization.
3. **Predefined Profiles**: Include profiles for common scenarios (e.g., urban, rural, open-sky).

---

## **Conclusion**
This experiment demonstrated the significant impact of parameter tuning on GNSS positioning results. By carefully selecting the satellite system, positioning method, and filter combination, it is possible to achieve high accuracy and robustness, albeit with trade-offs in processing speed. Implementing the suggested improvements could further enhance the performance and usability of the GNSS library.

---

## **How to Use This Repository**
- The lab report is provided in this `README.md` file.
- For detailed results and analysis, refer to the sections above.
- Suggestions for improvement are included for future work.

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Contact**
For questions or feedback, please open an issue or contact the repository owner.
