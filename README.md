# Overview
Artificial intelligence (AI) can provide the basis for tools that improve global health care, bringing us closer to the realization of the third sustainable development goal: good health and well-being for all. 

However, before AI-based tools are integrated in medical practice and applied to patients, it must be demonstrated that they serve the intended purpose without unintended effects. Of the AI-based tools that are currently used in medical practice, most were developed and regulated for a limited (e.g., national) public. Consequently, the adoption of AI-based tools is fragmented across the globe. As health is an issue that transcends borders, ITU/WHO FG-AI4H encourages a collective effort among stakeholders (including developers, regulators, healthcare practitioners, and public health institutes) from across the globe to ensure the safety and trustworthiness of AI-based tools and to permit their widespread implementation. 

This Open Code Project aims to produce the digital building blocks (six software packages) that compose the FG-AI4H Assessment Platform. The assessment platform, which can be distinguished from AI “challenge” platforms through its consideration of regulatory guidelines and the needs of other AI for health stakeholders, supports the end-to-end assessment of AI for health algorithms. 
 

# Goals
The life cycle of AI for health has several steps. First, annotated health data are compiled. Then, an AI for health model is developed and carefully evaluated. At each step, medical, technological, and regulatory considerations play a critical role. Within this life cycle, we have identified two opportunities to advance the field of AI for health:

1. The Arbiter Problem: 
   a. Challenge: Companies do not want to share their data and solution; both are opaque to regulators.
b. Opportunity: The software platform can serve as a safe and neutral arbiter between parties.
2. Health AIs at Scale: 
   a. Challenge: Regulatory compliance of AI for health is a country-dependent process, which brings considerable costs.
b. Opportunity: Map country requirements to automated tests.

The Open Code Project capitalizes on these opportunities to make AI for health usable at scale. 


Our product vision is the following:

<p style="text-align: center;line-height: 25px;">For health AI companies and regulators,
who need to proof that a health AI product is fit for purpose,
the AI4H Assessment Platform is a software platform
that supports the end-to-end process for assessing health AI algorithms on a global level.
Unlike e.g. EvalAI and other existing AI assessment platform products
our platform focuses specifically on healthcare and covers all additional aspects, including ground truth annotation, data & metadata management and reporting for health AI regulators.</p>


# Scope
The Open Code Project produces software comprising the foundation of the FG-AI4H Assessment Platform and addressing the aforementioned—and other—challenges in the field of AI for health. These are: Data Acquisition Package (DAP), Data Storage Package (DP), an Annotation Package (AP), a Prediction Package (PP), an Evaluation Package (EP), and a Reporting Package (RP). The following table highlights the purpose, functionalities, and target groups for each package.

# Components

| Component | Description and Purpose | Functionalities | Target Groups |
|--|--|--|--|
| [DAP](/Data-Acquisition-Package-\(DAP\)) | High-quality data are required to train and evaluate AI solutions. DAP coordinates the compilation of such data and ensures the availability of metadata and (where relevant) patient consent information. | Facilitates data compilation for many modalities; registers data and metadata; ingests data from DP; and manages patient consent information. | Manufacturers and medical experts
| [DP](/Data-Storage-Package-\(DP\)) | The basis for all subsequent packages is an orderly processing and storage of data and metadata. Medical data storage requires adherence to strict guidelines that preserve the privacy and safety of patients. DP provides data storage guidelines that consider these constraints. | Provides safe and secure storage of medical data; serves as an interface for other packages (AP, PP, and EP) to access this data; and offers data governance that complies with data protection laws. |Manufacturers, medical experts, and notified regulatory bodies
| [AP](/Data-Annotation-Package-\(AP\)) | High-quality annotated data provide the basis for supervised learning. Unfortunately, production is challenging and labor intensive. Certain features must be considered when evaluating an annotation: the quality of labels, the number of expert opinions, and the handling of non-unanimous decisions. AP brings together leading health experts across the globe to produce the highest-quality annotations at maximum efficiency. | Provides an annotation interface for many modalities; includes collaboration features; develops a network of annotation experts; and creates notifications of pending annotation tasks | Manufacturers and notified regulatory bodies
| [PP](/Evaluation-Package-\(EP\)) | For many health cases (e.g., the detection of breast cancer tissue or the classification of skin irritations), multiple parameters and AI models can provide viable solutions. PP allows various models to be evaluated in parallel for a benchmarking result. | Loads AI models; manages models undergoing prediction tasks (considers versioning, meta-data, etc.); and orchestrates computations|Manufacturers and notified regulatory bodies
| [EP](/Evaluation-Package-\(EP\)) | Model performance is dependent on the choice of metric and possible parameters. Thus, it is of utmost importance to have a framework that allows for the comparison of the performance of different AI models. EP provides meaningful, state-of-the-art metrics that promise high expressibility. | Offers testing measures and methods for different quality dimensions including interpretation, bias, uncertainty, and robustness; questionnaires provide qualitative evaluation | Manufacturers, notified regulatory bodies |
| [RP](/Reporting-Package-\(RP\)) | RP delivers a standardized format for communicating and reporting the properties, features, intended use, and limitations of AI for health to help connect different stakeholders. | A customizable reporting interface that presents the results of EP | Manufacturers, notified regulatory bodies, users of AI for health (doctors, patients), and vendors of AI for health |

# Contributing
If you are interested in contributing to this project please read the [Onboarding documentation](/Onboarding)

## Join the core team
If you want to join the core team please send an email to [ml@mllab.ai](mailto:ml@mllab.ai) expressing your interest in joining a specific component development.

## FG-AI4H Resources
More information about the Focus Group can be found [here](https://www.itu.int/en/ITU-T/focusgroups/ai4h/Pages/default.aspx).

# License
The AI4H Assessment Platform is released under a [modified BSD license](/AI4H-Assessment-Platform/Open-Code-Modified-BSD-License) and follows a standard development process, which uses tracker for issues and merging pull requests into master. For any type of contribution (even something trivial), please follow the guidelines.














