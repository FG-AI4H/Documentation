# Overview
Artificial intelligence has the potential to create new tools that can be used towards better global health conditions. It is, however, important to have controlled tools and regulated rules to prevent an avalanche of AI technologies that do not reach certain standards, or, are even harmful.
There exist many AI technologies that serve the goal to improve the health condition of patients. These are mostly developed (and regulated) within a limited area, on a country by country basis. This is often due to limited scope, resources, data and experts availability. This leads to a fragmented structure of the global healthcare situation. Health is, however, not a local issue and it requires a connected structure of stakeholders that are based on joint principles to create universal solutions.
In order to satisfy the needs to improve health globally across borders, the following tool aims to combine efforts and maximize the potential, the efficiency and the strengths of each stakeholder.

# Goals
The life-cycle of an AI technology in health involves several steps. It starts from the collection of (annotated) data, goes to the development of an AI model and is followed by a careful evaluation. Each step requires multiple resources such as medical expertise, technology experts, and regulatory bodies, to annotate the data, develop the model and evaluate its performance. Based on our work over the last two years, we identified two opportunities to move the field of health AIs forward:
1. The Arbiter Problem: 
   a. Challenge: Companies do not want to give away data and solution, regulators cannot see them
   b. Idea: Software platform as a safe and neutral arbiter between distrusting parties
2. Health AIs at Scale: 
   a. Challenge: Regulatory compliance in health is an expensive process
   b. Idea: Map country requirements to automated tests
We propose to develop an open source software platform that seizes on these opportunities to make health AIs usable at scale. This software tool is to include packages for the storage and annotation of data, prediction of diagnoses and evaluation as well as the reporting of the performance.

# Scope
More specifically the software includes the following aspects: a Data Acquisition Package (DAP), Data Storage Package (DP), an Annotation Package (AP), a Prediction Package (PP), an Evaluation Package (EP) and a Reporting Package (RP). Below we give a summary of the purpose, functionalities and target groups for each of the components. 

# Component

| Component | Description and Purpose | Functionalities | Target Groups |
|--|--|--|--|
| Data Acquisition Package (DAP) | In order to have sufficient data for training and evaluation of the AI solution, the data acquisition package will facilitate the intake of this data. It assures that a certain quality of the submitted data and assures the required meta-data is collected. Additionally, it needs to be ensured that patient consent information are submitted along with the data, if required. | Facilitation of ordered data intake for many data modalities - Registration of data and meta-data collection - Ingestion of data in Data Storage Package (DP) - Management of informed patient consent | Manufacturers, medical experts |
| Data Storage Package (DP) | Orderly processing and storage of data is a prerequisite for all other components. Health AI evaluation requires  rich meta-data of the used datasets. The storage of medical data mandates respect for strict rules related to privacy and safety of patients. The data storage package (DP) will provide a system that allows for data storage and serving under the above constraints. | Safe and secure storage for medical data Access interface for the other components (AP, PP, EP) to the storage Date Governance and Compliance to Data Protection Laws | Manufacturers, medical experts, notified regulatory bodies |
| Annotation Package (AP) | The annotation of data is necessary, yet, highly challenging and demanding. There needs to be terms that regulate the conditions under which the data should be annotated. This includes the quality of the labels, the number of expert opinions, as well as the handling of non-unanimous decisions. The software should allow to include the best experts all over the world, for different health problems, so that the potential that is spread globally can be exploited far more effectively. | Annotation interface for many data modalities Pool of annotation experts, including collaboration features Notification of pending annotation tasks | Manufacturers, notified regulatory bodies |
| Prediction Package (PP) | In many cases, there is no single AI solution for a particular health problem. May it be the detection of breast cancer or the classification of skin irritations, there is often more than one choice for the number of parameters or choice of AI model in general. If different methods can be proposed, the methods have to be evaluated. The software should allow to load different models to generate a benchmarking result. | Loading AI models Prediction tasks Model management (versioning, meta-data, etc.) Computation orchestration | Manufacturers, notified regulatory bodies |
| Evaluation Package (EP) | The evaluation package should allow to compare the performance of different AI models. The performance of a model strongly depends on the choice of the metric and its possible parameters. It is therefore of utmost importance to have a framework that allows for comparisons. The software should provide meaningful metrics that are agreed to be state-of-the-art and have the strongest expressibility. | Package of testing measures and methods for different quality dimensions including interpretation, bias, uncertainty and robustness Package of questionnaires for qualitative evaluation | Manufacturers, notified regulatory bodies |
| Reporting Package (RP) | A unified structure to communicate and report the properties, features, intended use and limitations of health AIs  helps connect different stakeholders. | A customizable reporting interface in which results of the EP component are presented | Manufacturers, notified regulatory bodies, health AI users (doctors, patients), health AI vendors |















