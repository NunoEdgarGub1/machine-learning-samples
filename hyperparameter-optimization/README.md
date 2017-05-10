# Performing Hyperparameter Optimization with Amazon Machine Learning
This document and associated sample script show you how to build a hyperparameter optimization pipeline for Amazon Machine Learning using the latest AWS SDK for Python (Boto 3).

This example is heavily based on Amazon's [K-Fold Cross Validation](https://github.com/awslabs/machine-learning-samples/tree/master/k-fold-cross-validation) example, but is upgraded to boto3 and runs as a single script.

## Setting Up

### Install Python

This sample script was developed and tested in python 2.

### Pull Dependent Libraries

This sample script depends on the `boto3` and `sigopt` packages, listed in the [requirements.txt](https://github.com/alexandraj777/machine-learning-samples/blob/master/k-fold-cross-validation/requirements.txt) file.

### Configure AWS Credentials

Your AWS credentials must be stored in a `~/.boto` or `~/.aws/credentials` file. Your credential file should look like this:

```
  [Credentials]
  aws_access_key_id = YOURACCESSKEY
  aws_secret_access_key = YOURSECRETKEY
```

To learn more about configuring your AWS credentials with Boto 3, go to [Boto 3 Quickstart](http://boto3.readthedocs.io/en/latest/guide/quickstart.html).

### Sign up for SigOpt

By default, this code optimizes the hyperparameters of the Amazon Machine Learning model with [SigOpt](https://www.sigopt.com). Sign up for a free trial and grab your API key from your [user profile](https://www.sigopt.com/user/profile)
