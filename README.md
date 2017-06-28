<p align="center">
   
<img src="https://cloud.githubusercontent.com/assets/4115778/24827505/eab7322a-1c42-11e7-96f3-dbc772da5f10.png" width="70%" alt="Sandcastle logo - AWS S3 bucket enumeration">

Inspired by a conversation with Instacart's [@nickelser](https://github.com/nickelser) on HackerOne, I've optimised and published Sandcastle – a Python script for AWS S3 bucket enumeration, formerly known as bucketCrawler.

The script takes a target's name as the stem argument (e.g. `shopify`) and iterates through a file of bucket name permutations, such as the ones below:

```
-training
-bucket
-dev
-attachments
-photos
-elasticsearch
[...]
```

## Getting started
Sandcastle supports Linux and macOS clients. Here's how to get started:

### Got the AWS CLI installed?
* Please ensure you have installed the [AWS CLI](http://docs.aws.amazon.com/cli/latest/userguide/installing.html) before proceeding.
* After installing the `awscli` package, run `aws configure` to set up your credentials.

### How to use Sandcastle 
1. Clone this repo (PyPi distribution temporarily disabled)
2. Run `sandcastle.py` with your desired target name and an input text file
3. Matching bucket permutations will be identified and read permissions tested.

```
usage: sandcastle.py [-h] -t targetStem [-f inputFile]

arguments:
  -h, --help            show this help message and exit
  -t targetStem, --target targetStem
                        Select a target stem name (e.g. 'shopify')
  -f inputFile, --file inputFile
                        Select a bucket permutation file (default: bucket-
                        names.txt)
```
Interested in learning more about S3? Check out the [Wiki](https://github.com/yasinS/sandcastle/wiki).

## Closing remarks
* This is my first public security project. Contributions are very much appreciated!
* Sandcastle is published "as-is" under the [MIT License](https://github.com/yasinS/sandcastle/blob/master/LICENSE).
* Castle icon by Andrew Doane from the Noun Project; Nixie One typeface from Jovanny Lemonad
