# Introduction
Air quality is a critical aspect of environmental health and has a profound impact on public well-being. Understanding the dynamics of air pollution and its effects is crucial for effective environmental management and policy-making. In Portugal, as in many other countries, monitoring air quality and ensuring compliance with established standards and regulations is of utmost importance.

This study focuses on analyzing air quality data obtained through web scraping from the Portuguese Environment Agency (APA). The objective is to gain insights into the air quality conditions in Portugal between 2011 and 2021 and classify air quality based on the Portuguese legislation. By employing time series analysis and developing classification models, this research aims to provide a comprehensive understanding of air quality trends and variations.

The analysis of air quality data allows us to evaluate the overall state of air quality in Portugal during the study period. Furthermore, understanding the seasonal effects on specific air pollutants can provide valuable information for identifying patterns and sources of pollution. This knowledge can aid in developing targeted strategies and interventions to improve air quality and mitigate adverse effects.

Classification models, such as RandomForest and XGBoost, are employed to classify air quality based on the Portuguese legislation. These models can help assess the accuracy and reliability of the classification process. However, dealing with imbalanced datasets poses challenges in accurately classifying minority categories, particularly in the case of "Sufficient" and "Poor" air quality classifications. Addressing the issue of data imbalance is crucial to ensure robust and precise classification results.

The outcomes of this study have implications for environmental management and policy formulation in Portugal. By providing insights into air quality trends, identifying seasonal effects, and assessing the performance of classification models, this research contributes to a comprehensive understanding of air quality dynamics in the country. The findings can support evidence-based decision-making and guide future initiatives aimed at enhancing air quality monitoring and control efforts.

# The DataSet
The QUALAR (https://qualar.apambiente.pt/) is a web platform of APA, the Portuguese Environment Agency, that displays online air quality data sampled by on air monitoring stations in Portugal. 

Due to the fact the platform does not expose to the final user, or provides documentation on how to use the API service that was implemented for web users downloads the data was obtain by webscraping. Taking a look at the download page of QUALAR, at https://qualar.apambiente.pt/downloads, it is possibel to see a table with a list of Air Monitoring Stations, with the following columns:
* Region (Região)
* Municipality (Concelho)
* Station (Estação)
* Station type (Tipo de Estação), with categories traffic, industrial and background
* Área type (Tipo de Área), with categories urban, suburban and rural
* columns for the following pollutants: O3, NO2, CO, SO2, PM10, PM2.5, C6H6, other

By webscraping with was obtain the data about O3, NO2, PM10 and PM2.5 from every region, municipality, station , station type and area type, between 2012 and 2022. All the data for the webscraping is in the following notebook: Web Scraping.ipynb

# Results
The results of this study indicate that the air quality in Portugal, between 2011 and 2021, was generally categorized as "good" according to the Portuguese legislation. The analysis of air quality data obtained through web scraping from APA revealed that the overall air quality during this period met the established standards and regulations.

The time series analysis conducted on the air pollutants, including SO2, PM10, O3, NO2, and PM2.5, showed that these pollutants exhibited seasonal effects. Their concentrations demonstrated patterns and variations influenced by seasonal factors, potentially due to weather conditions, seasonal activities, or specific emission sources. Understanding these seasonal effects is crucial for a comprehensive analysis of air quality.

The RandomForest and XGBoost classifiers used in this study demonstrated high accuracy values overall. However, it is important to note that the dataset exhibited a highly imbalanced distribution, which presented challenges for accurately classifying the "Sufficient" and "Poor" air quality categories (Class 3).

The imbalanced nature of the data affected the classifiers' ability to distinguish the minority classes, leading to lower precision and recall for Class 3. This indicates that the models struggled to accurately classify instances belonging to the "Sufficient" and "Poor" air quality categories.

Despite the challenges with imbalanced data, the RandomForest and XGBoost classifiers showed potential for accurate air quality classification when dealing with balanced datasets. However, further refinement of the models and addressing the data imbalance issue are necessary to ensure reliable classification of air quality in accordance with the Portuguese legislation.

We can see all the code in this notebook: EDA_Classification_Model.ipynb

# Conclusions
In conclusion, this study provided valuable insights into the air quality in Portugal based on the analysis of data obtained from the Portuguese Environment Agency. The findings indicate that the overall air quality in Portugal, between 2011 and 2021, was categorized as "good" according to the Portuguese legislation. This suggests that the established air quality standards and regulations were generally met during this period.

The time series analysis conducted on various air pollutants revealed the presence of seasonal effects. Pollutants such as SO2, PM10, O3, NO2, and PM2.5 exhibited predictable patterns and variations over time, influenced by seasonal factors. Understanding these seasonal effects is crucial for a comprehensive understanding of air quality dynamics in Portugal.

The RandomForest and XGBoost classifiers utilized in this study demonstrated high accuracy values overall. However, the highly imbalanced distribution of the dataset posed challenges in accurately classifying the "Sufficient" and "Poor" air quality categories (Class 3). The models struggled to distinguish instances belonging to these minority classes, leading to lower precision and recall.

Despite the limitations associated with imbalanced data, the RandomForest and XGBoost classifiers showed promise for accurate air quality classification when applied to balanced datasets. It is important to refine the models further and address the data imbalance issue to ensure reliable classification of air quality in accordance with the Portuguese legislation.

Overall, this study contributes to the understanding of air quality in Portugal and highlights the importance of considering seasonal effects in air pollution analysis. The findings can serve as a foundation for future research and initiatives aimed at improving air quality monitoring and management in Portugal.
