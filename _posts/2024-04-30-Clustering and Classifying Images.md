---
title: "Clustering and Classifying Images"
excerpt_separator: "<!--more-->"

tags:
  - Assignment

toc: true
toc_label: "VEHICLES AND CAPTCHA"
toc_sticky: true
toc_icon: "car"
  
---
## **VEHICLES AND CAPTCHA**

For the assignment, I will be working with images of vehicles. Given the diverse array of vehicle types, colors, and designs, I believe it presents an intriguing challenge for computer algorithms tasked with image analysis and classification. While algorithms are often trained to recognize and categorize common objects like animals or household items, vehicles introduce a unique complexity due to their varied shapes, sizes, and contextual settings. Unlike more standardized objects, from sleek sports cars to rugged trucks, each vehicle exhibits a distinct visual profile, ranging from subtle curves to intricate detailing. This variability makes the task of classification especially intricate for algorithms, as they must navigate through a multitude of visual features to accurately categorize vehicles. I'm particularly interested in exploring how these algorithms prioritize features such as vehicle shape, color, or context when attempting to accurately classify them. Moreover, I'm drawn to the potential synergy between vehicle classification and CAPTCHA challenges. The ability to distinguish between vehicles and non-vehicles or even distinguishing between the different types of vehicles holds promise for enhancing CAPTCHA mechanisms, offering a novel approach to human verification. By leveraging the intersection of computer vision and security measures, we can uncover new avenues for safeguarding digital systems against automated bots and ensuring user authenticity. In essence, this convergence of computer vision and security measures adds an additional layer of complexity and relevance to the study of vehicle classification algorithms. Through this investigation, I aim to understand the intricacies of image analysis while exploring innovative applications in the realm of digital security.

In compiling the dataset for my assignment, I actively searched various online platforms, prioritizing [Kaggle](https://www.kaggle.com/datasets/kaggleashwin/vehicle-type-recognition) for its extensive repository of image datasets. Eventually, I discovered a dataset on a website featuring numerous vehicle images labeled with numerical identifiers. Initially vast and encompassing a wide array of vehicle types sourced from diverse locations, this dataset presented a significant challenge for analysis. To streamline the process, I selected a subset of images from each vehicle category, ensuring a balanced representation across the dataset. This methodical curation aimed to facilitate more precise and effective classification tasks in subsequent stages. As I progressed with classification tasks, I found myself in need of additional examples for certain vehicle categories. To address this, I adopted a flexible approach, augmenting the dataset by selectively incorporating additional images from the broader collection. This iterative process allowed for ongoing refinement and expansion of the dataset, ensuring its relevance and comprehensiveness throughout the classification endeavors.

### ***Part 1: Clustering - Analysis and Interpretation***
In my assignment, I employed [Orange data mining software](https://orangedatamining.com/) to explore the realm of computer vision algorithms for my vehicle classification. Through this comprehensive analysis, I sought to gain a deeper understanding of how these algorithms can effectively categorize and identify various vehicle types based on their visual attributes. Employing a diverse range of algorithms including Inception, Painters, and SqueezeNet, I carefully examined their performance and observed intriguing variations in clustering outcomes. This divergence in results may stem from the unique methodologies and feature extraction techniques employed by each algorithm.


##### ***SqueezeNet***

> Image grid for SqueezeNet (Clustering)

<img src="/assets/images/assignment_4/SqueezeNet/SqueezeNet.png" style="zoom:300%;" />

In my project, the SqueezeNet algorithm demonstrated remarkable effectiveness in grouping vehicles based on their **types**. Notably, motorcycles were clustered on the far right of the grid, while trucks occupied the top left corner. This positioning indicates a clear distinction between these vehicle categories, showcasing the algorithm's ability to discern between different vehicle types accurately. Conversely, cars were predominantly situated in the bottom left quadrant, further highlighting the algorithm's proficiency in categorizing vehicles based on their distinct visual features. Interestingly, it didn't seem that the algorithm used the color of the vehicles as a metric for the clustering. Instead, it likely relied on other visual cues such as **shape and size** to perform the clustering. This suggests that the algorithm's classification approach is multifaceted, considering various aspects of vehicle appearance to accurately categorize them. Moreover, the systematic clustering observed in the results shows the algorithm's capability to effectively classify vehicles according to their unique characteristics.
Overall, the SqueezeNet algorithm's performance in grouping vehicles by type offers valuable insights into the underlying patterns and structures within the dataset. By effectively distinguishing between motorcycles, trucks, and cars, the algorithm provides a comprehensive understanding of the visual features that differentiate these vehicle categories.

> The images below show a portion of the categorization done by the SqueezeNet algorithm

<img src="/assets/images/assignment_4/SqueezeNet/Cluster heirachy.png" style="zoom:300%;" />
<img src="/assets/images/assignment_4/SqueezeNet/Cluster image view.png" style="zoom:300%;" />



##### ***Inception v3***

> Image grid for Inception v3 (Clustering)

<img src="/assets/images/assignment_4/Inception v3/Inception v3.png" style="zoom:300%;" />

In the analysis using the Inception v3 algorithm, similar levels of efficiency were achieved compared to the SqueezeNet algorithm. Motorcycles were clustered on the right side of the grid, while buses were predominantly positioned on the left. Trucks were primarily clustered at the bottom, while sports cars occupied the top portion of the grid. This clustering pattern suggests a clear differentiation between various vehicle types, showcasing the algorithm's effectiveness in categorizing vehicles based on their visual characteristics.
Furthermore, similar to the observations with the SqueezeNet algorithm, it appears that the color of the vehicles was not a significant factor in the clustering process. Instead, the algorithm likely prioritized other visual features such as shape and size to perform the clustering. This multidimensional approach to classification highlights the robustness of the Inception v3 algorithm in accurately categorizing vehicles across different types.

> The images below show a portion of the categorization done by the Inception v3 algorithm

<img src="/assets/images/assignment_4/Inception v3/Cluster heirachy.png" style="zoom:300%;" />
<img src="/assets/images/assignment_4/Inception v3/Cluster image view.png" style="zoom:300%;" />


##### ***Deeploc***

> Image grid for Deeploc (Clustering)

<img src="/assets/images/assignment_4/Deeploc/deeploc.png" style="zoom:300%;" />

In contrast to the previous algorithms, the Deeploc algorithm employed a different approach in classifying vehicles. Rather than categorizing vehicles based on their types, the algorithm seemed to prioritize color as the primary clustering metric. Brighter and warmer-colored vehicles were predominantly clustered at the bottom of the grid, while darker and cooler-colored vehicles tended to be positioned towards the top. This clustering pattern suggests that the Deeploc algorithm relied heavily on color cues to group vehicles, with varying hues and intensities influencing the clustering outcomes. Interestingly, this color-centric classification approach offers a unique perspective on the dataset, highlighting the algorithm's ability to discern visual patterns and distinctions based on color characteristics. While it may not have classified vehicles according to their types, the Deeploc algorithm's focus on color clustering provides valuable insights into the diverse visual attributes present within the dataset.

> The images below show a portion of the categorization done by the Deeploc algorithm

<img src="/assets/images/assignment_4/Deeploc/Cluster heirachy.png" style="zoom:300%;" />
<img src="/assets/images/assignment_4/Deeploc/Cluster_image_viewer.png" style="zoom:300%;" />


#### Comparative Analysis (SqueezeNet vs Inception v3 vs Deeploc)

Firstly, in terms of clustering efficiency, both the SqueezeNet and Inception v3 algorithms demonstrated similar levels of effectiveness in categorizing vehicles based on their types. They successfully differentiated between motorcycles, trucks, buses, and sports cars, with distinct clusters forming on the grid. This suggests that both algorithms were adept at recognizing and classifying vehicles according to their visual characteristics, such as shape, size, and texture.

However, the Deeploc algorithm diverged from this approach by prioritizing color as the primary clustering metric. While it did not classify vehicles according to their types, it effectively grouped vehicles based on their color characteristics. Brighter and warmer-colored vehicles tended to cluster towards the bottom of the grid, while darker and cooler-colored vehicles were positioned towards the top. This color-centric classification approach offers a unique perspective on the dataset, highlighting the algorithm's ability to discern visual patterns and distinctions based on color features.

Another notable difference lies in the clustering criteria employed by each algorithm. While the SqueezeNet and Inception v3 algorithms focused on a multifaceted approach, considering various visual features such as shape, size, and texture, the Deeploc algorithm primarily relied on color cues for clustering. This difference in clustering criteria hints at the versatility and adaptability of each algorithm in handling different types of datasets and classification tasks.

In summary, while all three algorithms demonstrated effectiveness in clustering vehicles, they differed in their approaches and criteria for classification. The SqueezeNet and Inception v3 algorithms excelled in categorizing vehicles based on their types, while the Deeploc algorithm prioritized color clustering. 


<img src="/assets/images/assignment_4/SqueezeNet/matrix.png" style="zoom:300%;" />
<img src="/assets/images/assignment_4/Inception v3/matrix.png" style="zoom:300%;" />
<img src="/assets/images/assignment_4/Deeploc/matrix.png" style="zoom:300%;" />
<img src="/assets/images/assignment_4/Inception v3/matrix.png" style="zoom:300%;" />