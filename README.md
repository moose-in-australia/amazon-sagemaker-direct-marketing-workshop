# Amazon SageMaker Workshop - Direct Marketing with XGBoost
_A basic Amazon SageMaker workshop demonstrating the machine learning workflow from data preparation to model deployment using direct marketing data._

This workshop covers the basics of data preparation, model training, hyperparameter tuning, and model deployment in Amazon SageMaker. It guides participants through the process of building an [XGBoost](https://docs.aws.amazon.com/sagemaker/latest/dg/xgboost.html) model to predict if direct marketing calls will result in a customer signing up for a term deposit at a bank. 

It takes around 2 hours to complete this workshop.

## Prerequisites

If you are completing this workshop as part of an event hosted by AWS, you might be provided with temporary access to an AWS account for the duration of the event.

Alternatively, you can complete this workshop using your own AWS account. The workshop has been designed to work within the resources limitations of a brand new AWS account. You will need access to AWS Identity and Access Management (IAM), Amazon Simple Storage Service (Amazon S3), and Amazon SageMaker. It is optional to use AWS CloudFormation.

## Setup

There are two methods for setting up this workshop: by using AWS CloudFormation with the template provided in this repository, or by manually creating an Amazon SageMaker notebook instance with the contents of this repository. 

### CloudFormation

Follow the instructions below to set up the workshop using AWS CloudFormation.

1. Log in to your AWS account.
1. Navigate to the AWS CloudFormation service.
1. Click the "Create stack" button.
1. Set "Template is ready" in the Prepare template section.
1. Set "Upload a template file" in the Template source section.
1. Upload the `cf_direct_marketing_workshop.json` file provided in the cloudformation folder of this repository.
1. Click the "Next" button.
1. Enter a Stack name.
1. Click the "Next" button twice.
1. Check the box "I acknowledge that AWS CloudFormation might create IAM resources".
1. Click the "Create stack" button.

### Manual Setup

Follow the instructions below to set up the workshop manually in your AWS account.

1. Log in to your AWS account.
1. Navigate to the Amazon SageMaker service.
1. Using the menu on the left side of the page, navigate to the "Notebook instances" page under the "Notebook" section.
1. Click the "Create notebook instance" button.
1. Choose a name for the notebook instance, e.g. direct-marketing-workshop.
1. Choose instance type "ml.t2.medium".
1. Leave the rest of the notebook instance settings as default.
1. Choose an IAM role for the notebook
  * Feel free to reuse an existing IAM role if one exists in your account.
  * Choose "Create a new role" from the drop-down menu, then choose the "Any S3 bucket" option in the corresponding menu.
1. Expand the "Github repositories - optional" tab.
1. Choose "Clone a public Git repository to this notebook instance only" from the drop-down menu.
1. Insert `https://github.com/aws-samples/amazon-sagemaker-workshop-direct-marketing-xgboost.git` as the Git repository URL.
1. Finish by clicking the "Create notebook instance" button.

You may need to wait a couple of minutes for the notebook to be created. Once the status shows "InService", click on "Open Jupyter". This will open a new Jupyter tab showing the contents of this repository. Open the `notebooks/participant_workshop_long_version.ipynb` file to get started on the full workshop, or open the `notebooks/participant_workshop_short_version.ipynb` file to work through the minimal version.

## For Instructors

To encourage active learning, the participant notebooks (`notebooks/participant_workshop_[long/short]_version.ipynb`) contains cells which require the user to write or fix code before running successfully. The see the correct answers, or suggestions where no single answer is correct, please open the instructor notebook (`notebooks/instructor_workshop.ipynb`).