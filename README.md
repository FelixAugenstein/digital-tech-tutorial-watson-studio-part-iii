<h1 align="center" style="border-bottom: none;">:bar_chart: IBM Digital Tech Tutorial: Watson Studio Part III</h1>
<h3 align="center">In this hands-on tutorial you will graphically build and evaluate machine learning models by using the SPSS Modeler flow feature in IBM Watson Studio.</h3>

## Prerequisites

1. Sign up for an [IBM Cloud account](https://cloud.ibm.com/registration).
2. Fill in the required information and press the „Create Account“ button.
3. After you submit your registration, you will receive an e-mail from the IBM Cloud team with details about your account. In this e-mail, you will need to click the link provided to confirm your registration.
4. Now you should be able to login to your new IBM Cloud account ;-)

## Digital Tech Tutorial Watson Studio Part I to IV

This tutorial consists of 4 parts, you can start with part I or any other part, however, the necessary environment is set up in part I.<br>
[Part I - data visualization, preparation, and transformation](https://github.com/FelixAugenstein/digital-tech-tutorial-watson-studio)<br>
[Part II - build and evaluate machine learning models by using the AutoAI](https://github.com/FelixAugenstein/digital-tech-tutorial-watson-studio-part-ii/)<br>
[Part III - graphically build and evaluate machine learning models by using the SPSS Modeler flow](https://github.com/FelixAugenstein/digital-tech-tutorial-watson-studio-part-iii/)<br>
[Part IV - set up and run Jupyter Notebooks to develop a machine learning model](https://github.com/FelixAugenstein/digital-tech-tutorial-watson-studio-part-iv/)

The 4 parts of this tutorial are based on the [Learning path: Getting started with Watson Studio](https://developer.ibm.com/series/learning-path-watson-studio/).

## Create model flow

To create an initial machine learning flow:

1. From the Assets page, click Add to project.
2. In the Choose asset type page, select Modeler Flow.

![Modeler Flow](readme_images/modeler-flow.png)

3. On the Modeler page, select the ‘From File’ tab.
4. Download the model flow that is named ‘customer-churn-flow.str’ from this repository.
5. Drag the downloaded modeler flow file to the upload area or browse for it. This also sets the name for the flow.

![Upload Flow File](readme_images/upload-flow-file.png)

6. Change the name and provide a description for the machine learning flow (optional).
7. Click Create. This opens the Flow Editor that can be used to create a machine learning flow.

You have now imported an initial flow that we’ll explore in the rest of this tutorial.

![Initial Flow](readme_images/initial-flow.png)

Under the Modeling drop-down menu, you can see the various supported modeling techniques. The first one is Auto Classifier, which tries several techniques and then presents the results of the best one.

The main flow itself defines a pipeline consisting of several steps:

- A Data Asset node for importing the data set
- A Type node for defining metadata for the features, including a selection of the target attributes for the classification
- An Auto Data Prep node for preparing the data for modeling
- A Partition node for partitioning the data into a training set and a testing set
- An Auto Classifier node called ‘churn’ for creating and evaluating the model

Additional nodes have been associated with the main pipeline for viewing the input and output. These are:
- A Table output node called ‘Input Table’ for previewing the input data
- A Data Audit node called ’21 fields’ (default name) for auditing the quality of the input data set (min, max, standard, and deviation)
- An Evaluation node for evaluating the generated model
- A Table output node called ‘Result Table’ for previewing the results of the test prediction

Other input and output types can be viewed by selecting the Outputs drop-down menu.

## Assign data asset and run the flow

To run the flow, you must first connect the flow with the appropriate set of test data available in your project.

1. Select the three dots of the Data Asset node to the left of the flow (the input node).
2. Select the Open command from the menu. This shows the attributes of the node in the right part of the page. 

![Change Data Asset](readme_images/change-data-asset.png)

3. Click Change data asset to change the input file. 
4. On the next page, select your .CSV file that contains the customer churn, and click OK. 
5. Select comma(,) as a field delimiter, none as quote character and period (.) as decimal symbol.
6. Click Save.
7. Click Run (the arrow head) in the toolbar to run the flow.

![Run Flow](readme_images/run-flow.png)

Running the flow creates a number of outputs or results that can be inspected in more detail.

![Outputs](readme_images/outputs.png)

## Understanding the data

Now that you have run the flow, take a closer look at the data.

1. Select the Input Table node at the top of the flow diagram.
2. Select the three dots in the upper-right corner and invoke the Profile command from the pop-up menu.

![Profile Command](readme_images/profile-command.png)

The last interaction might run part of the flow again but has the advantage that the page provides a Profile tab for profiling the data and a Visualization tab for creating dashboards.

## Data preparation



## Training the model



## Evaluating the model



## Saving and deploying the model



## Testing the model



## If you have any questions just contact me
Felix Augenstein<br>
Digital Tech Ecosystem & Developer Representative @IBM<br>
Twitter: [@F_Augenstein](https://twitter.com/F_Augenstein)<br>
LinkedIn: [linkedin.com/in/felixaugenstein](https://www.linkedin.com/in/felixaugenstein/)
