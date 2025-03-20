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
1. **Satellite System**: GPS-only, GPS + GLONASS + Galileo + Beidou.
2. **Positioning Method**: Static Positioning, DGPS (Differential GPS).
3. **Filter Combination**: Forward Filter only, Forward + Backward Filter.

---

## **Comparison of Positioning Results**

### **1. Satellite System Comparison**

| **Satellite System**       | **Accuracy** | **Processing Speed** | **Robustness**       |
|----------------------------|--------------|----------------------|----------------------|
| GPS-only                            | Low          | Fast                 | Low                  |
| GPS + GLONASS + Galileo + Beidou    | High         | Slow                 | High                 |
![ONLY GPS](https://github.com/user-attachments/assets/88c632b4-5300-453b-816e-74b28dcac440)
![full constellation](https://github.com/user-attachments/assets/3467e209-48da-4986-9db2-4e096d5cf72e)

### **2. Positioning Method Comparison**

| **Positioning Method**     | **Accuracy** | **Processing Speed** | **Robustness**       |
|----------------------------|--------------|----------------------|----------------------|
| Static Positioning         | Medium       | Moderate             | Moderate (stationary only) |
| DGPS                       | High         | Slow                 | High                 |
![STATIC](https://github.com/user-attachments/assets/0c6257ff-0128-4468-bc5a-2002c791bb14)
![DGPS](https://github.com/user-attachments/assets/15f9b33b-bd6a-4188-8865-59c9baab3741)

### **3. Filter Combination Comparison**

| **Filter Combination**      | **Accuracy** | **Processing Speed** | **Robustness**       |
|-----------------------------|--------------|----------------------|----------------------|
| Forward Filter only         | Medium       | Fast                 | Moderate             |
| Forward + Backward Filter   | High         | Slow                 | High                 |
![full constellation](https://github.com/user-attachments/assets/a9edf31a-f8a5-4f37-8067-cee4a918705b)
![COMBINEDFILTER](https://github.com/user-attachments/assets/1fc71598-20f0-4e7c-9dfa-76601955bb99)

The result of more iterations of filter, much more processing time, little gains:
![ITERATION10](https://github.com/user-attachments/assets/510ae988-6591-45db-a53b-412e0baac0d7)

---

## **Summary of Findings**

### **Optimal Parameter Settings**
The best positioning results were achieved using:
- **Satellite System**: GPS + GLONASS + Galileo + Beidou
- **Positioning Method**: DGPS
- **Filter Combination**: Forward + Backward Filter

### **Performance Metrics for Optimal Settings**
- **Accuracy**: High
- **Processing Speed**: Slow
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
