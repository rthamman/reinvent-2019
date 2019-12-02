### To start the workshop, create an Amazon SageMaker Notebook Instance.

An Amazon SageMaker notebook instance is a fully managed machine learning compute instance that runs a Jupyter notebook server. You can use the notebook instance to prototype building, training and testing machine learning models. 


**To create an Amazon SageMaker notebook instance**

1. Go to https://dashboard.eventengine.run

2. Enter the hash provided by the workshop administrator and click on Proceed

3. Click on AWS Console

4. Click on Open Console. This will launch AWS Console. Note - you can disregard the credential information

5. Navigate to "Amazon SageMaker" under Services
    
6. Choose **Notebook instances**, then choose **Create notebook instance**
    
7. On the **Create notebook instance** page, provide the following information (if a field is not mentioned below, leave it default):
    
    a. For **Notebook instance name**, enter a name for your notebook instance
        
    b. For **Instance type**, choose `ml.m5.xlarge`
        
    c. For **IAM role**, choose **Create a new role**, then choose **Create role**. In 'create IAM Role' pop up window, select 'Any S3 bucket' 
        
    d. For Git repositories, select 'clone public git repo ***' and provide the following repository: ``https://github.com/rthamman/reinvent-2019``
        
    e. Choose **Create notebook instance**. In a few minutes, Amazon SageMaker will launch a notebook instance with a preconfigured Jupyter notebook server and a set of Anaconda libraries. 

8. In few minutes, the notebook instance will be in the running state. Click **Open Jupyter** to continue. This will open the Jupyter interface in your browser window. 

9. In the Jupyter notebook console, in the Files tab, you will see the following. We will run through the notebooks cell by cell. The order in which you run the notebooks isn't mandated.  However, it is recommended to follow the notebooks in the order listed below because they demonstrate different workflows from simple to more complex: 
    
   a. Lab 1 (sentiment-analysis.ipynb) - this notebook demonstrates the following features:
	- A textCNN Natural Language Processing (NLP) model
	- Script Mode with Git integration:  use your own training scripts version contolled in GitHub, no Docker needed!
	- Hosted Training Mode
	- Batch Prediction

   b. Lab 2 (tf-boston-housing.ipynb) - this notebook demonstrates the following features:
	- A Multilayer Perceptron (MLP) regression model
	- Local Mode Training
	- Local Mode Endpoint
	- Hosted Training Mode with model extraction for running it elsewhere
	- Hosted Endpoint
	- Automatic Model Tuning

   c. Lab 3 (tf-distributed-training.ipynb) - this notebook demonstrates the following features:
	- Distributed Training using Parameter Servers
	- Distributed Training using Horovod
	- TensorFlow Serving conveniences in SageMaker, including pre/post-processing scripts for inference
   
10. For each lab, click on the related Jupyter notebook (.ipynb) and follow the instructions when the notebook opens. 
