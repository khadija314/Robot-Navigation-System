# Warehouse Robot Navigation System Using Machine Learning

An intelligent, autonomous warehouse robot navigation system that utilizes a **Decision Tree Classifier** to make real-time movement decisions based on obstacle distance data from front, left, and right ultrasonic sensors.

---

##  Project Overview
Manual programming for every possible navigation situation in dynamic industrial environments is highly inefficient. This project addresses that challenge by training a machine learning model on historical sensor readings to predict the most appropriate movement actions for the robot without explicit human control. 

The model achieves **100% accuracy** on the test dataset, ensuring safe and optimal pathfinding inside a simulated warehouse environment.

---

##  Dataset Description
The dataset consists of 20 balanced observations (5 examples per movement class) to ensure an unbiased training phase. All sensor readings are recorded in centimeters (cm).

### Input Features (Sensors)
* **Front Sensor:** Measures distance to the obstacle directly in front.
* **Left Sensor:** Measures distance to the obstacle on the left side.
* **Right Sensor:** Measures distance to the obstacle on the right side.

### Output Labels (Actions)
* `0`: **Move Forward** — Space is clear ahead.
* `1`: **Stop** — Obstacles are too close, risking a collision.
* `2`: **Turn Left** — Obstacle ahead; left path is open/safer.
* `3`: **Turn Right** — Obstacle ahead; right path is open/safer.

---

##  Model & Performance
A **Decision Tree Classifier** was chosen due to its clear, rule-based logic structure which perfectly mirrors navigation decision trees. 

### Evaluation Metrics:
* **Accuracy:** 100%
* **F1-Score:** 1.00 across all classes

### Confusion Matrix
The model successfully classified all test samples without a single false positive or false negative:

Predicted 0   Predicted 1
Actual 0 [Move]     2             0
Actual 1 [Stop]     0             2


---

##  Tech Stack & Tools
* **Language:** Python
* **Libraries:** Pandas, Scikit-learn, Matplotlib, Seaborn
* **Environment:** Kaggle / Jupyter Notebook

---

##  Future Enhancements
* Scaling up with larger and noisy real-world datasets.
* Testing ensemble methods like Random Forests and Neural Networks.
* Implementing Deep Reinforcement Learning for dynamic obstacle avoidance.
* Deploying the trained model onto physical robot hardware.

---

##  Authors
* **Dua Ghafoor** (24-SE-082)
* **Khadija Ashraf** (24-SE-040)
* **Laiba Fatima** (24-SE-019)

*Submitted to Mr. Abdul Hadee Anwaar — Department of Computer Sciences, HITEC University, Taxila.*
