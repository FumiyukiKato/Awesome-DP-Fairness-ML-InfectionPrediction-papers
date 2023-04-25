## Awesome papers about DP, Fairness, ML and infection prediction

### ML x Fariness
- **Equality of Opportunity in Supervised Learning (NIPS’16)**
  - Introducing equalized odds instead of demographic parity as fairness definition. Proposing post-processing-based method. Sensitive label information is needed at the time of forecasting to adjust the predicted results.
- **A Reductions Approach to Fair Classification (ICML’18)**
  - Formalizing optimizatoin problem for accuracy and fairness in classification. Proposing ad hoc algorithm to optimize both of accuracy and fairness. Many citation and popular repository.
- **Adaptive sensitive reweighting to mitigate bias in fairness-aware classification (WWW'18)**
  - For fairness, weights are added to the predictive distribution for each data for learning.
- **Fairness-aware Classification: Criterion, Convexity, and Bounds (AAAI’19)**
  - The learning framework proposed in this paper formulates various commonly used fairness measures as convex constraints, which can be directly incorporated into classical classification models.
- **FNNC: Achieving Fairness through Neural Networks (IJCAI'20)**
  - Proposed method optimizes accuracy and fairness together. In addition to the usual loss function, adding a simple constraint term such that the fairness constraint is satisfied within a (mini)batch.


### DP x Fairness
- **On the Compatibility of Privacy and Fairness (UMAP’19)**
  - proved that strict fairness does not hold at all when DP is satisfied. Proof error is pointed out in **Trade-Offs between Fairness and Privacy in Machine Learning** in 2021.

- **Fair Decision Making using Privacy-Protected Data (FAT’20)**
  - In order to evaluate the fairness of the DP, decision-making problems (resource allocation using U.S. census data) were set up to address real-world issues. Based on this, the lack of fairness is empirically shown.

- **Decision Making with Differential Privacy under a Fairness Lens (IJCAI’21)**
  - The problem setting is based on (FAT'20). This paper theoretically analyze the previous problem setting and get general implications and proposed some mitigaion approach for the unfairness.

- **Differential Privacy and Fairness in Decisions and Learning Tasks: A Survey (IJCAI’22)**
  - Syracuse Uni and GA tech group's work. Many problem settings are common in their works, which is shown in this paper. The recent relationship between DP and Fairness is summarized.

- **Post-processing of differentially private data: A fairness perspective. (IJCAI’22)**
  - Post-processing on data with guaranteed DP creates a bias in the output data that propagates to downstream tasks. This paepr analyzes the impact from a fairness perspective.

#### DP-ML x Fairness

- **Differentially Empirical Risk Minimization under the Fairness Lens (NIPS’21)**
  - The paper analyzes how two private optimization techniques, output perturbation and DP-SGD, affect fairness for the ERM problem. Overall, the problem is difficult and the analysis is often vague, but some general suggestions are made.
- **On the Privacy Risks of Algorithmic Fairness (EUROSP’21)**
  - Dr.Shokri (popular in membership inference)'s work. Conversely, the paper considers the question of whether privacy can be sacrificed to achieve fairness. This paper focus on empirical evaluation.
- **Removing disparate impact of differentially private stochastic gradient descent on model accuracy (KDD’21)**
  - They propose DPSGD-F, a variant of DP-SGD, which corrects fairness among groups by using different clipping sizes for each group. It is designed based on the empirical hypothesis that the bias due to clipping may be different for each group. Looks a bit solid.
- **Balancing learning model privacy, fairness, and accuracy with early stopping criteria. (TNLLS’21)**
  - Their claim is that by capturing it by early stopping, we can learn a model that strikes good trade-off of privacy, accuracy, and fairness. Looks not good in real-world case.
- **Federated learning meets fairness and differential privacy. (NIPS’21)**
  - The study attempted to protect DP and Fairness at the same time in FL, but the content appears to be falling apart, in particular, in privacy part.
- **Exploring the Unfairness of DP-SGD Across Settings (workshop@AAAI"22)**
  - Empirical evaluation of fairness by DP-SGD.
- **How unfair is private learning? (UAI’22)**
  - Analyze fairness under the problem setting in the long-tail distribution. The analysis showed that if fairness is to be strictly maintained under (ε,δ)-DP, it is necessary to sacrifice accuracy.


### infection x ML
- Prediction model baseline (SOTA?)
  - **A prospective evaluation of AI-augmented epidemiology to forecast COVID-19 in the USA and Japan (npjDM’21)**
    - Proposing and evaluating infection predition model, taking differnet static and dynamic features as input and output the number infecitons, cumulative deaths and confirmed cases for each locations (such as states). The rather large, complex proposed model is evaluated on real-world data on a practical scale. All of the results look very reliable.
    - code: [google-research/covid_epidemiology at master · google-research/google-research · GitHub](https://github.com/google-research/google-research/tree/master/covid_epidemiology)
    - Fairness is discussed in [Supplementary Note 6: Model Fairness](https://static-content.springer.com/esm/art%3A10.1038%2Fs41746-021-00511-7/MediaObjects/41746_2021_511_MOESM2_ESM.pdf)


- **A Survey on Data-driven COVID-19 and Future Pandemic Management (ACM Computing Surveys 2023)**
  - Comprehensive survey paper on techniques for data-driven decision-making for COVID-19 and other infectious diseases. Below are some papers that look good for each specific tasks, especially using ML.
  - Tansmission prediction
    - **Data-driven simulation and optimization for COVID-19 exit strategies. (KDD20)**
    - **Spatiotemporal prediction of COVID-19 cases using inter- and intra-county proxies of human interactions. (Nat Commun 2021)**
    - **Into the unobservables: A multi-range encoderdecoder framework for COVID-19 prediction. (CIKM21)**
    - **Examining COVID-19 forecasting using spatio-temporal graph neural networks. arXiv preprint arXiv:2007.03113 (2020).**
    - **Mobility network models of COVID-19 explain inequities and inform reopening. (Nature21)**
  - (Medical) resouce allocation
    - **Optimal resource allocation for control of networked epidemic models. IEEE Trans. 2015**
    - **Optimal time-varying vaccine allocation amid pandemics with uncertain immunity ratios. IEEE Access 9 (2021)**
    - **Optimal policy learning for COVID-19 prevention using reinforcement learning. (2020)**
  - Contact tracing
    - **Deep learning for visual analytics of the spread of COVID-19 infection in crowded urban environments.  (2021).**


### infection x ML x fairness 
(not limited to monitoring, including other healthcare topics. few papers in CS community)
- **Bias at warp speed: How AI may contribute to disparities gap in the time of COVID-19 (JAMIA'21)**
  - General opinion, just claiming the necessity of ML fairness
- **Algorithmic fairness in pandemic forecasting: lessons from COVID-19 (npj Digital Medicine'22)**
  - Fairness analysis based on the model of "**A prospective evaluation of AI-augmented epidemiology to forecast COVID-19 in the USA and Japan (npjDM'21)**". They divided the U.S. states into subgroups for equity analysis and found no particular unfairness...
- DNN on image data for COVID diagnosis
  - **Public COVID19 X-ray datasets and their impact on model bias–A systematic review of a significant problem. (medrxiv21)**
    - Clarifying bias risks for training dataset in the model predicting COVID from CT scans.
  - **Common pitfalls and recommendations for using machine learning to detect and prognosticate for COVID-19 using chest radiographs and CT scans (Nat21)**
    - Showing most of published model for predicting COVID from CT scans are not useful, including from fairness perspective.

###### Work with Source code. To use as unfairness baselines related to COVID-19
- **A prospective evaluation of AI-augmented epidemiology to forecast COVID-19 in the USA and Japan (npjDM'21)**
  - rich resources, but too rich
- **A fairness assessment of mobility-based COVID-19 case prediction models (arxiv'22)**
- **An adversarial training framework for mitigating algorithmic biases in clinical machine learning (npj Digital Medicine'23)**
- **The Problem of Fairness in Synthetic Healthcare Data (mdpi'21)**
- **Bias and fairness assessment of a natural language processing opioid misuse classifier: detection and mitigation of electronic health record data disadvantages across racial subgroups (JAMIA'21)**
- **Biases associated with database structure for COVID-19 detection in X-ray images (Nat.Sci.Rep'23)**
- **objective framework for evaluating unrecognized bias in medical AI models predicting COVID-19 outcomes (JAMIA'22)**
- **Biases in human mobility data impact epidemic modeling (arxiv'21)**
- [**GitHub - datasets/covid-19: Novel Coronavirus 2019 time series data on cases**](https://github.com/datasets/covid-19)

### infection x ML x DP

- Helthcare area (not focusing on "infection")
  - **Chasing Your Long Tails: Differentially Private Prediction in Health Care Settings (FAccT'21)**
    - Applying DP to ML with actual medical data does not give very good performance. The increase in unfairness has not been outstandlingly confirmed in this paper.

### infection x ML x fairness x DP

- Looks no work so far

