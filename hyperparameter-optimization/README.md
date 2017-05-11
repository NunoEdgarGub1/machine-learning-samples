# Performing Hyperparameter Optimization with Amazon Machine Learning

This document and associated sample script show you how to build a hyperparameter optimization pipeline for Amazon Machine Learning using the latest AWS SDK for Python (Boto 3).

This example is heavily based on Amazon's [K-Fold Cross Validation](https://github.com/awslabs/machine-learning-samples/tree/master/k-fold-cross-validation) example, but is upgraded to boto3 and runs as a single script.

## Setting Up

### Install dependencies

This sample script was developed and tested in python 2.

This sample script depends on the `boto3` and `sigopt` packages, listed in the [requirements.txt](https://github.com/alexandraj777/machine-learning-samples/blob/master/k-fold-cross-validation/requirements.txt) file.

### Configure AWS Credentials

Your AWS credentials must be stored in a `~/.boto` or `~/.aws/credentials` file. Your credential file should look like this:

```
  [Credentials]
  aws_access_key_id = YOURACCESSKEY
  aws_secret_access_key = YOURSECRETKEY
```

To learn more about configuring your AWS credentials with Boto 3, go to [Boto 3 Quickstart](http://boto3.readthedocs.io/en/latest/guide/quickstart.html).

### Get the Code

Get the samples by cloning this repository.

```
  git clone https://github.com/alexandraj777/machine-learning-samples.git
```

## Demo

This sample code provides two scripts, `hyperparameter_optimization.py` and `hyperparameter_optimization_with_sigopt.py`.

```
python hyperparameter_optimization.py --name 4-fold-hy-opt-demo 4
```

Edit the hyperparameter assignments in `hyperparameters.py` to manually tune your model.

For a more in depth description of how cross validation is performed with Amazon ML, see the original [K-Fold Cross Validation](https://github.com/awslabs/machine-learning-samples/tree/master/k-fold-cross-validation) example that formed the basis for this code sample.


### Running with SigOpt

If you would like to use SigOpt to optimize your hyperparameters faster and better than tuning by hand, sign up for a free trial on our [website]([SigOpt](https://www.sigopt.com)) and grab your API token from your [user profile](https://www.sigopt.com/user/profile).

SigOpt uses an ensemble of Bayesian Optimization techniques to suggestion new hyperparameter configurations that learn from past results.

Run the script `hyperparameter_optimization_with_sigopt.py` with all of the options in the above section, and additionally provide your SigOpt API token.

```
python hyperparameter_optimization_with_sigopt.py --name 4-fold-hy-opt-sigopt-demo 4 --sigopt-api-token <SIGOPT_API_TOKEN>
```

Amazon's Machine Learning (Amazon ML) provides and API for asynchronously creating data sources, machine learning models, and evaluations.

