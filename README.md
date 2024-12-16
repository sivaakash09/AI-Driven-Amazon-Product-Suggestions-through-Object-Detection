# Project Details
## Topic: AI-Driven-Amazon-Product-Suggestions-through-Object-Detection

 ## Team Members:

 ## Siva Akash Ramini - 121301796
 ## LakshmiSaiVenkataSivaNagamaniCharan Kankanala - 120983184
 ## Roshan Syed - 121293565
 ## Rasagna Tirumani - 120984075
 ## Ankan Mandal - 121332455

## Project Overview

Introduction

In this project, we aim to integrate advanced machine learning and computer vision techniques to extract meaningful insights from a structured dataset and analyze visual content using YOLO (You Only Look Once). With the rapid evolution of technology, object detection and structured data processing have become integral for solving real-world problems across domains like e-commerce, healthcare, and autonomous systems. This project focuses on cleaning, preprocessing, and analyzing data while also deploying a YOLO-based object detection system to classify and identify visual elements effectively.

What is your topic?
The topic of this project revolves around data-driven insights and object detection. It combines structured data preprocessing with real-time computer vision models to build a holistic system for analyzing textual and visual information.

What is the main motivation for your work?
The motivation for this project arises from the growing demand for systems capable of processing complex datasets and visual inputs simultaneously. For instance, e-commerce platforms require streamlined methods to manage product data while leveraging visual models to enhance user experiences. This project contributes to building an end-to-end pipeline for structured data analysis and YOLO-based object detection, highlighting its applicability in various industries.

Project Workflow
This project is organized into the following steps:

Data Loading and Preprocessing

Cleaning and structuring raw data for analysis.
Exploratory Data Analysis (EDA)

Exploring patterns, trends, and relationships within the dataset.
YOLO-based Object Detection

Setting up YOLO models with pre-trained weights and classifying visual inputs.
Model Integration and EvaluationC

Combining structured data insights with object detection results.
Visualization and Results Interpretation

Presenting findings through visualizations and detailed analysis.
Through this workflow, we aim to demonstrate the synergy between structured data analysis and advanced computer vision techniques, creating solutions applicable to a variety of real-world scenarios.

## Contributions
A: Project Idea
•	Ankan Mandal — Conceptualized the idea of integrating YOLO for real-time object detection to link products with curated Amazon datasets. Coordinated with the team to refine the project scope and objectives.
B: Dataset Curation and Preprocessing
•	Lakshmi Sai Venkata Charan Kankanala — Collected and curated the Amazon product dataset, ensuring its cleanliness and relevance by removing duplicates, handling null values, and standardizing entries for consistency. Used Python libraries for preprocessing and verified dataset quality.
C: Data Exploration and Summary Statistics
•	Siva Akash Ramini — Conducted exploratory data analysis to uncover trends in pricing and category distribution. Visualized key metrics using histograms, bar charts, and boxplots. Analyzed correlations between product attributes to derive actionable insights.
D: ML Algorithm Design/Development
•	Roshan Syed/ Siva Akash Ramini — Designed and implemented YOLO-based object detection. Pre-processed image inputs for YOLO inference, optimized non-max suppression parameters, and created mechanisms for matching detected objects to product entries. Integrated pre-trained YOLO weights and customized detection thresholds for improved performance.
E: ML Algorithm Training and Test Data Analysis
•	Roshan Syed/ Ankan Mandal — Tuned YOLO hyperparameters for accuracy, precision, and recall. Analyzed training loss curves and evaluated model performance using intersection over union (IoU) metrics. Tested object mapping efficacy with a subset of the dataset.
•	Rasagna Tirumani — Performed comprehensive evaluation of prediction outputs, verifying accuracy in matching detected objects to corresponding products. Documented test results and created confusion matrices.
F: Visualization, Result Analysis, and Conclusion
•	Rasagna Tirumani — Created and analyzed visualizations, including training accuracy curves, category-based bar charts, and correlation heatmaps. Summarized key findings and insights from EDA and model evaluation.
G: Final Tutorial Report Creation
•	Lakshmi Sai Venkata Charan Kankanala — Compiled the final project report and created a step-by-step GitHub tutorial for implementing the project. Contributed to documenting model architecture, data pipeline, and results.

Visualization Analysis
1. Distribution of Selling Prices
•	Purpose: To understand the pricing structure of products in the dataset.
•	Description:
o	A histogram was used to plot the selling prices, with a kernel density estimate (KDE) overlay for smooth visualization.
o	This visualization provides a clear understanding of the most common price ranges.
•	Insights:
o	The majority of products are priced between $10 and $100, indicating affordability for a wide audience.
o	High-priced products ($200 and above) are rare, representing less than 10% of the dataset.
•	Usage:
o	Helps in setting price range filters for e-commerce applications.
o	Guides product segmentation for marketing strategies.
•	Visualization: 


![image](https://github.com/user-attachments/assets/0749a585-14f8-4e0b-9f03-fc0817fa30f8)



2. Count of Products by Category
•	Purpose: To identify the most frequent product categories in the dataset.
•	Description:
o	A count plot was created to display the number of products in each category, ordered by frequency. This provides a clear view of product distribution across different categories.
•	Insights:
o	Toys & Games and Electronics are the top categories, accounting for over 60% of the products. Categories such as Home & Kitchen are less frequent but offer significant potential for targeted recommendations.
•	Usage:
o	Useful for prioritizing categories in the recommendation system. Helps in tailoring category-specific promotions.
•	Visualization: 
 ![image](https://github.com/user-attachments/assets/6a315cbe-f3b4-4186-b4da-aa7810d4be04)

3. Boxplot of Selling Prices by Category
•	Purpose: To analyze price variability within each product category.
•	Description:
o	A boxplot was used to depict the distribution of selling prices across categories, highlighting median values, interquartile ranges, and outliers. This visualization identifies categories with wide price ranges and those with consistent pricing.
•	Insights:
o	Electronics exhibits the widest price variability, with several high-priced items as outliers. Categories like Home & Kitchen and Toys & Games show more consistent pricing.
•	Usage:
o	Guides inventory pricing strategies and promotional activities. Helps in understanding consumer preferences within each category.
•	Visualization:
![image](https://github.com/user-attachments/assets/ee5e25d4-4884-483c-912f-4eab3a8a8a79)

5. Pie Chart of Product Categories
•	Purpose: To visualize the proportional distribution of products across categories.
•	Description:
o	A pie chart was generated to display the percentage share of each category in the dataset. The visualization provides a clear representation of dominant and minor categories.
•	Insights:
o	Toys & Games and Electronics dominate the dataset, accounting for over 50% of the total products. Smaller categories like Office Supplies and Sports Equipment represent niche markets.
•	Usage:
o	Useful for identifying focus areas for marketing and inventory planning. Helps in understanding category-specific demand.
•	Visualization:
![image](https://github.com/user-attachments/assets/bb622062-7240-4208-92ea-bb01293c747f)

 
Model Execution and Evaluation
The YOLOv3 (You Only Look Once) model was executed for real-time object detection, leveraging its Darknet-53 backbone and three-scale detection approach. During model execution, the TensorFlow framework and associated libraries were employed for efficient training and inference. The input image was resized to 416x416, and YOLOv3 generated bounding boxes with confidence scores for detected objects.
Execution Workflow
1.	Data Preprocessing:
o	The input images were preprocessed using OpenCV, resized, and converted into blob format for YOLO inference. The YOLOv3 model then used its three output scales to predict objects of varying sizes.
2.	Inference:
o	YOLOv3 generated bounding box coordinates, confidence scores, and class probabilities. Boxes with confidence scores below a threshold of 0.5 were filtered out, while remaining overlapping boxes were refined using Non-Max Suppression (NMS) to retain the most relevant detections.
3.	Product Matching:
o	The detected class labels (e.g., "bottle") were used to filter relevant product entries from the provided dataset using string matching techniques. For example, a detected "bottle" was mapped to products such as "TAL Water Bottle" with relevant information like price, category, and product URL.
Model Evaluation
The training process spanned 10 epochs, with key performance metrics such as accuracy, precision, and recall monitored for each epoch.
•	Accuracy: Started at 76.02% in Epoch 1, peaked at 94.75% during Epoch 6, and stabilized at 86.93% by Epoch 10.
•	Precision: Improved consistently, reaching 0.95 in certain epochs, indicating minimal false positives.
•	Recall: Started high at 0.92 and stabilized at 0.94, showing the model's ability to detect most relevant objects.
The training accuracy over epochs graph reflects periodic fluctuations, likely due to learning rate adjustments, while the overall trend showcases significant improvement across training iterations.
Visualization and Results
The following visualizations were generated to evaluate model performance:
1.	Training Accuracy Over Epochs:
A line graph illustrates the accuracy progression, showing peaks and dips as the model optimizes over the epochs.
2.	Training Metrics Log:
The detailed epoch-wise logs display accuracy, precision, and recall, providing insights into the model's convergence and stability.
![image](https://github.com/user-attachments/assets/3e2ad98a-a5fd-4a0b-be94-114de8d83579)
![image](https://github.com/user-attachments/assets/24861bee-0795-418f-b057-1a085357f266)



Insights
1. Object Detection and Dataset Integration
•	By utilizing Yolo, the system demonstrated a high accuracy in detecting objects from images and linking them with relevant Amazon products.
•	Detected objects like bottles and earphones were successfully matched to specific product entries in the dataset, emphasizing the efficiency of the keyword-matching process.
2. EDA Highlights
•	Price Distribution: Most products were priced between $10 and $100, confirming that the dataset represents an affordable product range.
•	Category Analysis: The dominance of categories like Toys & Games and Electronics provides a broad range of detection and mapping possibilities.
•	Correlation Analysis: A moderate negative correlation was observed between Selling Price and Quantity, indicating that higher-priced products are less frequently stocked.
3. Visualization Insights
•	Visuals like histograms and boxplots clarified product price trends and category distributions.
•	Heatmaps revealed significant correlations that can inform inventory and pricing strategies.
4. System Performance
•	Real-time detection and mapping were achieved with Yolo, ensuring scalability for practical deployment.
•	Confidence thresholds and Non-Max Suppression optimized the bounding box accuracy, minimizing false positives.
•	
Conclusions
The project demonstrates significant outcomes by bridging visual recognition and e-commerce applications, effectively detecting objects and linking them to curated product datasets to provide personalized shopping experiences. Real-world object detection was successfully solved by utilizing the YOLO algorithm, and the system's dependability and interpretability were improved by combining data preprocessing, keyword matching, and visualization. This creative method offers a fundamental framework for incorporating AI into e-commerce systems, enhancing customer personalization and engagement while providing insights for more effective inventory control and focused marketing campaigns. The project intends to demonstrate scalability and potential for wider applications in the developing field of AI-driven e-commerce by expanding its dataset to include a wider range of product categories and price ranges and incorporating user feedback to improve the accuracy and relevance of product suggestions.



