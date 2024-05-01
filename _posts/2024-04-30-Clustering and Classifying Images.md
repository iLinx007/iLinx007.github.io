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


<img src="/assets/images/assignment_4/SqueezeNet/SqueezeNet.png" style="zoom:300%;" />
> Image grid for SqueezeNet (Clustering)

In my project, the SqueezeNet algorithm demonstrated remarkable effectiveness in grouping vehicles based on their **types**. Notably, motorcycles were clustered on the far right of the grid, while trucks occupied the top left corner. This positioning indicates a clear distinction between these vehicle categories, showcasing the algorithm's ability to discern between different vehicle types accurately. Conversely, cars were predominantly situated in the bottom left quadrant, further highlighting the algorithm's proficiency in categorizing vehicles based on their distinct visual features. Interestingly, it didn't seem that the algorithm used the color of the vehicles as a metric for the clustering. Instead, it likely relied on other visual cues such as **shape and size** to perform the clustering. This suggests that the algorithm's classification approach is multifaceted, considering various aspects of vehicle appearance to accurately categorize them. Moreover, the systematic clustering observed in the results shows the algorithm's capability to effectively classify vehicles according to their unique characteristics.
Overall, the SqueezeNet algorithm's performance in grouping vehicles by type offers valuable insights into the underlying patterns and structures within the dataset. By effectively distinguishing between motorcycles, trucks, and cars, the algorithm provides a comprehensive understanding of the visual features that differentiate these vehicle categories.

<img src="/assets/images/assignment_4/SqueezeNet/cluster_heirachy.png" style="zoom:300%;" />
<img src="/assets/images/assignment_4/SqueezeNet/cluster_image_view.png" style="zoom:300%;" />

