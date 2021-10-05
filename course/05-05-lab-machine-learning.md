---
topic:
    module: ''
    title: 'Lab: Get started with machine learning'
---

# Lab: Get started with machine learning

In this lab, you'll explore *Azure Machine Learning*, a cloud-based service for training and managing machine learning models. Specifically, you'll use the *Automated machine learning* capabilities of the service to train a model using existing data.

## Before you start

Before starting this lab, you'll need a Microsoft Azure subscription.

If you don't already have an Azure subscription, sign up for a free trial using your Microsoft account at <a href="https://azure.microsoft.com/free/" target="_blank" rel="noopener noreferrer">https://azure.microsoft.com/free</a>.

## Lab overview

Rosie Reeves has been selling lemonade for a while, and has collected data for each day on which she sold lemonade. Now she wants to use that data to create a model that will predict how much lemonade she is likely to sell on a given day, which will help her ensure that she makes the right amount of lemonade to meet demand.

## Exercise 1: Prepare Azure Machine Learning resources

Before you can use Azure Machine learning to train and test a predictive model, you need to prepare a few resources in your Azure subscription.

### Create an Azure Machine Learning workspace

As its name suggests, a workspace is a centralized place to manage all of the Azure ML assets you need to work on a machine learning project.

1. Sign into the the <a href="https://portal.azure.com" target="_blank" rel="noopener noreferrer">Azure portal</a> and on the **Home** page, click the **&#65291; Create a resource** button and search for *Machine Learning*. Then create a new **Machine Learning** resource, specifying the following settings:

    - **Subscription**: *Your Azure subscription*
    - **Resource group**: *Create a resource group with a suitable name, such as **azure-ml-resources***
    - **Workspace name**: *Enter a unique name for your workspace*
    - **Region**: *Select the geographical region closest to you*
    - **Storage account**: *Note the default new storage account that will be created for your workspace*
    - **Key vault**: *Note the default new key vault that will be created for your workspace*
    - **Application insights**: *Note the default new application insights resource that will be created for your workspace*
    - **Container registry**: None

    ![Creating an Azure Machine Learning workspace in the Azure portal](./images/create-aml-workspace.png)

2. Click **Review + create** to validate the settings for your workspace, and then click **Create** to create it. Deployment of the new workspace may take a minute or so.
3. When the workspace and its associated resources have been deployed, use the **Go to resource** button to view the deployed workspace, which should look like this:

    ![An Azure Machine Learning workspace in the Azure portal](./images/azure-ml-workspace-resource.png)

### Create compute resources in Azure Machine Learning Studio

Now that you have created an Azure Machine Learning workspace, you can use *Azure Machine Learning Studio* to manage it.

1. In the Azure portal, on the page for your Azure Machine Learning workspace, click **Launch studio**. This open Azure Machine Learning Studio in a new browser tab. (If prompted, sign in using the Microsoft account you used in the previous task and select your Azure subscription and workspace.)

    ![Azure Machine Learning Studio](./images/azure-ml-studio.png)

2. On the home page in Azure Machine Learning studio, under **Automated ML**, click **Start now**.
3. On the **Automated ML** page, click **&#65291; New Automated ML run**.