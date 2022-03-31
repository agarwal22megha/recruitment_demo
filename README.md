# Recruitment Demo
Leverage Vertex AI for candidate classification and candidate scoring


To get started, please have a look at [this highly recommended learning path](https://cloud.google.com/training/machinelearning-ai) to get hands-on lab experience for Vertex AI. In particular please focus on the following two tutorials: 
- [Auto ML Text Classification](https://cloud.google.com/vertex-ai/docs/tutorials/text-classification-automl)
- [Vertex AI Workbench](https://cloud.google.com/vertex-ai-workbench) 


Following your learnings, it will be great to [start setting up a playground GCP Project](https://cloud.google.com/vertex-ai/docs/start/cloud-environment) which would need Vertex AI and Google Cloud Storage services 


For playing around with the resume dataset:
- Please find the Kaggle Dataset [here](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset).
- Build  auto-ml resume classification: Please refer to this sample [hello-text project](https://cloud.google.com/vertex-ai/docs/tutorials/text-classification-automl) which walks you through e2e project setup, data import, auto-ml training, model performance evaluation and deployment steps.
  - Get the Dataset imported it into the project using Vertex AI console > Dataset. In the import section please use the upload files from your computer option.
  - For convenience, I have already cleaned the dataset which is ready to be imported into the Vertex AI project [here](https://github.com/agarwal22megha/recruitment_demo/blob/main/clean_kaggle_resume_dataset.csv).
- For building custom text embedding models for candidate scoring:
  - Within the same project, please [create a GCP Cloud storage bucket](https://cloud.google.com/storage/docs/creating-buckets) and [upload](https://cloud.google.com/storage/docs/uploading-objects) the [raw Kaggle dataset](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset)
  - On the  Vertex AI workbench, please [create a managed notebook instance](https://cloud.google.com/vertex-ai/docs/workbench/managed/create-managed-notebooks-instance-console-quickstart) and launch the JupyterLab and you can either create your own Python3 notebook or import the [sample one](https://github.com/agarwal22megha/recruitment_demo/blob/main/candidate_scoring.ipynb) in this repo .
  - If there are any libraries that are missing, please use: `!pip install library_nam` in the Jupyter notebook cell
  - Also please ensure the right path to your csv file in gcs is used while reading the data using pandas 

