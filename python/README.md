# AWS SDK for Python code examples

## Overview

The code examples in this topic show you how to use the AWS SDK for Python (Boto3) 
with AWS. 

The AWS SDK for Python provides a Python API for AWS infrastructure services.
Using the SDK, you can build applications on top of AWS services such as Amazon Simple 
Storage Service (Amazon S3), Amazon Elastic Compute Cloud (Amazon EC2), and Amazon DynamoDB.

## Types of code examples

* **Single-service actions** - Code examples that show you how to call individual service functions.

* **Single-service scenarios** - Code examples that show you how to accomplish a specific task by calling multiple functions within the same service.

* **Cross-service examples** - Sample applications that work across multiple AWS services.

### Finding code examples

Single-service actions and scenarios are organized by AWS service in the 
[example_code folder](example_code). A README in each folder lists and describes how 
to run the examples.

Cross-service examples are located in the [cross_service folder](cross_service). 
A README in each folder describes how to run the example.

## ⚠️ Important
* Running this code might result in charges to your AWS account. 
* Running the tests might result in charges to your AWS account.
* We recommend that you grant your code least privilege. At most, grant only the 
minimum permissions required to perform the task. For more information, see 
[Grant least privilege](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege). 
* This code is not tested in every AWS Region. For more information, see 
[AWS Regional Services](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services).

## Run the examples

### Prerequisites

* You must have an AWS account, and have your default credentials and AWS Region
configured as described in the 
[AWS Tools and SDKs Shared Configuration and
Credentials Reference Guide](https://docs.aws.amazon.com/credref/latest/refdocs/creds-config-files.html).
* [Python 3.6.0 or later](https://www.python.org/)

### Install packages

Depending on how you have Python installed and on your operating system,
the commands to install and run might vary slightly. For example, on Windows, use `py` 
in place of `python`.

Each example folder contains a `requirements.txt` file that defines the packages needed 
to run that example. To install the required packages, first navigate to the example folder
and create a virtual environment by running the following:

```
python -m venv .venv
```

This creates a virtual environment folder named `.venv`. Each virtual environment
contains an independent set of Python packages. Activate the virtual environment by
running one of the following:

```
.venv\Scripts\activate # Windows
source .venv/bin/activate # Linux, macOS, or Unix
```

Install the packages for the example by running the following:

```
python -m pip install -r requirements.txt
```

This installs all of the packages listed in the `requirements.txt` file in the current
folder.

### Run the code

Most examples have one or more files that contain a `__main__` runner. Each of these
files can be run from the command line:

```
python file_with_main.py
```

Some examples require command line arguments. In these cases, you can run the example
with a `-h` flag to get help. Each example has a README.md that describes additional 
specifics about how to run the example and any other prerequisites. 

## Tests

All tests use Pytest, and you can find them in the `test` folder for each example.
When an example has additional requirements to run tests, you can find them in the
README for that service or cross-service example.

### Unit tests

The unit tests in this module use stubbed responses from the botocore Stubber. 
This means that when the unit tests are run, requests are not sent to AWS, 
mocked responses are returned, and no charges are incurred on your account.

Run unit tests in the folder for each service or cross-service example at a command 
prompt by excluding the `integ` mark.

```
python -m pytest -m "not integ"
```

### Integration tests

⚠️ Running the integration tests might result in charges to your AWS account.

The integration tests in this module make actual requests to AWS. This means that when
the integration tests are run, they can create and destroy resources in your account. 
These tests might also incur charges. Proceed with caution.

Run integration tests in the folder for each service or cross-service example at a 
command prompt by including the `integ` mark.

```
python -m pytest -m "integ"
```

## Docker image (Beta)
This example code will soon be available in a container image
hosted on [Amazon Elastic Container Registry (ECR)](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html). This image will be pre-loaded
with all Python examples with dependencies pre-resolved, allowing you to explore
these examples in an isolated environment.

⚠️ As of January 2023, the [SDK for Python image](https://gallery.ecr.aws/b4v4v1s0/python) is available on ECR Public but is still
undergoing active development. Refer to
[this GitHub issue](https://github.com/awsdocs/aws-doc-sdk-examples/issues/4125)
for more information.

## Additional resources
 
* [AWS SDK for Python (Boto3) Documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
* [AWS SDK for Python (Boto3) API Reference](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/index.html)

---

Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved. 

SPDX-License-Identifier: Apache-2.0
