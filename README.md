## Development ceased: Sandcastle is at EOL
Thanks for supporting the Sandcastle project. Apologies for the inconvenience, but upon consideration I've decided to cease development and place this project at End of Life. @tomdev's [Bucketeers](https://github.com/tomdev/teh_s3_bucketeers/) tool incorporates a wider range of scanning prefixes and is open to contribution PRs under the MIT License. Please feel free to use the `bucket-names.txt` list in your projects; a de-duplicated version can be found [here](https://gist.github.com/yasinS/9e77cecd2fe8b275006f0436c6443a13).

<hr/>

<p align="center">
   
<img src="https://cloud.githubusercontent.com/assets/4115778/24827505/eab7322a-1c42-11e7-96f3-dbc772da5f10.png" width="70%" alt="Sandcastle logo - AWS S3 bucket enumeration">

Inspired by a conversation with Instacart's [@nickelser](https://github.com/nickelser) on HackerOne, I've optimised and published Sandcastle – a Python script for AWS S3 bucket enumeration, formerly known as *bucketCrawler*.

The script takes a target's name as the stem argument (e.g. `github`) and iterates through a file of bucket name permutations, such as the ones below:

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
Sandcastle supports Linux and macOS clients right now. Here's how to get started:

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
Interested in learning more about S3 buckets? Check out the [Wiki](https://github.com/yasinS/sandcastle/wiki).

## Closing remarks
* This is my first public security project. Contributions are very much appreciated!
* Sandcastle is developed and published "as-is" under the [MIT License](https://github.com/yasinS/sandcastle/blob/master/LICENSE).
* Castle icon by Andrew Doane from the Noun Project; Nixie One typeface from Jovanny Lemonad
