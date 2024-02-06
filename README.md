# Olist E-Commerce Customer Clustering
Team Members:

- [Omar Charis Atthabrizi](https://github.com/atthabrizi)
- [Muhamad Aris Margono](https://github.com/muharismrgn)

# Context
**What is Olist?**

Olist is a brazillian technology company that mainly focuses on e-commerce solutions. Basically it is a large department store within marketplaces that are connected to the main e-commerces in Brazil. Olist’s solution consists of three aspects: Software, Contracts with the main marketplaces and Reputation sharing. The diagram below shows how Olist links marketplaces, consumers, and retailers.
The company main product purpose is to offers a marketplace solution (of e-commerce segment) to shopkeepers of all sizes (and for most segments) to increase their sales whether they have online presence or not.

Olist, a prominent Brazilian technology company, specializes in e-commerce solutions. Essentially, it functions as a comprehensive department store within major Brazilian online marketplaces. Olist's offerings encompass software, partnerships with key marketplaces, and a reputation-sharing system. The company's primary objective is to provide a marketplace solution for businesses of all sizes and across various sectors, enabling them to enhance their sales, irrespective of their online presence.

# Stakeholders
The main stakeholders of Olist are the sellers and the marketing team within the company. These two groups play pivotal roles in the success and growth of Olist's e-commerce platform.

- **Sellers**: Sellers are a crucial stakeholder group for Olist. They encompass various businesses of all sizes and across diverse sectors in Brazil. Sellers rely on Olist's e-commerce solution to expand their reach, increase their sales, and effectively tap into the online marketplace. The success of these sellers directly impacts Olist's performance and reputation.

- **Marketing Team**: The marketing team is responsible for customer acquisition and retention, making them indispensable stakeholders. They are entrusted with the task of developing and executing marketing strategies that attract new customers to the platform and encourage existing ones to remain loyal. The effectiveness of these strategies has a direct impact on Olist's ability to grow its user base and increase sales. The marketing team's efforts are closely aligned with the company's overarching goal of optimizing marketing and customer acquisition strategies to foster customer loyalty and sustain growth.

# Problem
The goal is to ensure productivity by effectively generating and retaining both new and existing users on the platform. Finding the most efficient method to allocate these expenses is crucial for sustained growth and success in the competitive e-commerce market.

How?
We are going to use RFM Analysis to clusters these consumer, by these clusters we hope to understand better and are going able to analyze the pattern and behaviour of each customer group. With this it is hoped that using Machine Learning and data-driven approach could generate new and loyal customers.

# Goals
The main goal of the Olist E-Commerce Customer Clustering project is to optimize marketing and customer acquisition strategies to increase sales and foster customer loyalty. To achieve this overarching goal, we have specific sub-goals:

- Customer Segmentation: Utilize RFM (Recency, Frequency, Monetary) analysis to cluster customers into distinct groups based on their shopping behavior and transaction history.

- Behavioral Insights: Gain a deep understanding of each customer segment's patterns and behaviors, allowing for targeted marketing efforts and personalized recommendations.

# Analytical Approaches
Our analytical approach involves two main steps. In the first step, we utilize descriptive analytics to analyze Periodically Income Growth, conduct product sales analysis, assess customer behavior, and examine customer retention cohorts based on their transaction data. This allows us to gain insights into various aspects of our customer base, optimize resource allocation for marketing efforts, and make data-driven decisions to enhance our business strategies.

In the second step, we employ clustering modeling techniques to group customers with similar behavior patterns. We select relevant features and apply clustering with algorithms like K-Means and Agglomerative clustering or without algorithms like RFM Segmentation. We then evaluate the quality of these clusters using the Silhouette Score and extract actionable insights for personalized marketing strategies. This approach combines descriptive analysis with modeling to enhance customer segmentation and drive data-driven marketing decisions.

# Metric Evaluation
To assess the effectiveness of our customer segmentation and machine learning models, we will use the following metrics:

- **Silhouette Score**: Silhouette score will be used to evaluate the quality of customer segmentation. A higher silhouette score indicates that customers within the same segment are more similar to each other than to those in other segments.

- **Training Time**: This metric measures the time taken to train machine learning models. It is essential to ensure that the models can be trained efficiently, especially when dealing with a large customer dataset.

# Results

| Model | Silhouette Score | Training Time(s) | 
|-|-|-|
| RFM Segmentation | 0.303 | 0.191 | 
| K-Means Clustering | 0.427 | 0.643 | 
| Agglomerative Clustering | 0.376 | 8.657 | 

Even though K-Means Clustering is the best according to the silhouette score metric with a score of 0.427, because K-Means cannot cluster frequencies that are more than 1 in more than one cluster, RFM Segmentation is used for further analysis which will be related to marketing strategy.

**On Clusters Distributions:**

---

- Using the RFM method, the whole customer are divided to 11 clusters. The cluster density however shows that the customers are mainly classified into 6 main clusters. That is:
***New Customers, Promising, About to Sleep , Cannot Losse Them, Hibernating Customers and Lost Customers*** with the rest of the clusters only showing numbers of customer below 100.

- After using the density to filter the clusters, the remaining clusters are going to be analyzed using the `monetary` metric. To understand how each of the customers in the clusters contribute to the company cash flows. This filtering conclude that in terms of monetary value there are only four clusters that has a high contributions to the overall transactions value.

- After the filtering process, the analysis are focusing on 4 main clusters: **New Customers, Promising, About to Sleep,** and **Cannot Lose Them** clusters.

**On Clusters Needs Strategy:**

---


These informations can be used to understand the right actionable decision towards investing in customer acquisition from each clusters.

- **Promising:** Offer targeted coupons and personalized advertisements to incentivize continued engagement. Utilize the customer preference data to target promotions and keep them actively involved with the platform. 

- **New Customers:** Initiate conversations through dedicated admins to welcome and guide new customers. Highlight the platform's unique value propositions, benefits, and offerings. Provide personalized benefits to demonstrate the immediate value of being a part of the platform.

- **About to Sleep:** Launch targeted advertising campaigns based on individual product interests. Conduct surveys to understand the reasons behind declining interest and tailor promotions accordingly. Use personalized communication to show that the platform values their preferences and is committed to addressing their needs.

- **Cannot Lose Them:** Allocate resources to interact with customers in this cluster. Deploy admins to engage in meaningful conversations, understand their preferences, and address any concerns. Develop exclusive promotions and product offerings to win them back. Invest time and money in making them feel valued and appreciated as recurring customers.



**Continuous monitoring and adjustment of strategies will be crucial for maintaining a healthy customer base.**

**On Clusters Products Analysis:**

---
- The analysis reveals a consistent trend with Bed Bath Table as the top-selling product across clusters, suggesting a universal appeal. However, the versatility in the top 10 products of each cluster underscores the importance of understanding diverse product preferences within specific customer segments.

- To capitalize on these findings, the company is advised to analyze preferences within each cluster for targeted marketing. Aligning promotions and discounts with identified preferences can enhance customer relevance, fostering higher engagement and potentially driving increased sales. This customer-centric approach allows the company to cater effectively to diverse preferences while leveraging the popularity of universal trends, such as the appeal of Bed Bath Table.

- For more information on the product, the company can use the function made in [Recommendation System](recommendation_system.ipynb).

# Dashboard - Tableau
[Tableau Dashboard](https://public.tableau.com/app/profile/abbe.atthabrizi/viz/OlistE-CommerceDashboard_17061788791200/Dashboard1?publish=yes)
