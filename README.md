# Covid19_livercancer
### Problem statement
Since the start of the COVID-19 pandemic there have been over 290 million confirmed infections and 5 million deaths reported worldwide. 
Because of the unprecedented burden on healthcare resources, many healthcare activities such as chronic disease management, 
cancer screening and cancer treatments have been cancelled or delayed. 
Consequently, referrals of suspected new cancers have reduced, with increases in cancer-related deaths predicted.

The full impact of the COVID-19 pandemic on patients with primary liver cancer (PLC) has yet to be determined, 
although European data reported a disruption to hepatocellular carcinoma (HCC) services, 
a reduction in incident cases and an impact on management during the first wave of the pandemic (February 2020 to May 2020).

The data was prospectively collected on all patients referredto the Newcastle-upon-Tyne NHS Foundation Trust (NUTH) 
hepatopancreatobiliary multidisciplinary team (HPB MDT) in the first 12 months of the pandemic (March 2020-February 2021), 
comparing to a retrospective observational cohort of consecutive patients presenting in the 12 months immediately preceding it (March 2019-February 2020). 
All new cases with a diagnosis of hepatocellular carcinoma (HCC) or intrahepatic cholangiocarcinoma (ICC) confirmed radiologically or histologically, following international guidelines, were included.

The objective is to assess the impact of the COVID-19 pandemic on patients with newly diagnosed liver cancer.
I choose models for training: 'LogisticRegression',
                              'AdaBoostClassifier',
                              'RandomForestClassifier', 
                              'SVC', 
                              'XGBClassifier', 
                              'KNeighborsClassifier',
                              'GaussianNB'.


### I. Conclusions on data analysis:
      1. Before the pandemic, 59.11% were diagnosed with liver cancer than during the pandemic. 
      This is explained by the fact that during the pandemic almost all medical institutions specializing in a subspecialty, their work was suspended or postponed. 
      So, the liver cancer detection rates are lower.
      2. According to the etiology of liver cancer, NAFLD is more common - 39% of cases of non-alcoholic fatty liver disease, 
      also Liver cancer is more likely to be diagnosed if the patient has cirrhosis and it is considered the underlying disease
      3. The youngest age in men with liver cancer is 27 years, the oldest 96 years. In women, the youngest age of liver cancer patients is 41 years old, the oldest is 87 years old. 
      4. 45% are symptomatically detected with liver cancer, 32% are incidentally detected, and 23% are observed. Those who were observed with other liver diseases, 
      liver cancer was diagnosed more often - 96 cases. 120 times there is accidental detection of liver cancer. 107 cases had symptoms of liver cancer but was not diagnosed 
      5. During the pandemic, symptomatic detection of liver cancer is lower than before the pandemic. This is because, firstly, 
      other hospitals were closed and people only went to the infectious disease department. Secondly, all symptoms of liver cancer could be attributed to COVID-19 symptoms.  
     6. Most patients died of liver cancer before the pandemic.
     7. The higher the stage of the disease, the greater the risk of death.
     8. Most patients received supportive care. 
     9.  According to the results of this dataset: The pandemic had a very strong impact on the detection of liver cancer, at that time most people did not receive specialized medical care. All forces were directed to fight COVID-19. 

     
### II. Conclusions after data training:
1. This dataset has 450 rows × 27 columns, which is considered small for analysis. 
2. Dataset has very many Nan values, which some of them will be deleted or replaced after processing, resulting in data   reduction.
3. For data training, I chose models: 'LogisticRegression',
                                       'AdaBoostClassifier',
                                      'RandomForestClassifier', 
                                       'SVC', 
                                       'XGBClassifier', 
                                       'KNeighborsClassifier',
                                       'GaussianNB'.
4.  The best and most stable result is: AdaBoostClassifier - train 0.86, test 0.81. Predicts results well before the pandemic than during the pandemic because more data is available before the pandemic. Also SVC performs better - train - 0.86, test 0.80. 
 LogisticRegression train 0.73, test 0.72 gives normal but weak predictions.
 XGBClassifier predicts pre-pandemic results better, train 0.91, test 0.79 - this is very overfit. RandomForestClassifier shows a similar result.
'KNeighborsClassifier', 'GaussianNB' perform worst, but maybe they are not suitable for this dataset.


