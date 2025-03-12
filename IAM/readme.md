# AWS CLI

## AWS CLI for Ubuntu Instance

````
sudo apt update -y
sudo apt install unzip -y
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
````
````
aws configure
````
- enter access_key:
- enter secret_key:
- enter region name:
- output format:


# S3

## Listing Buckets
List all AWS S3 buckets:
```sh
aws s3 ls
```

## Creating a New S3 Bucket
Create a new S3 bucket:
```sh
aws s3 mb s3://myaws-s3-bucket
```

## Listing Objects Inside a Bucket
List objects within a specific S3 bucket:
```sh
aws s3 ls s3://myaws-s3-bucket
```

## Copying an Object to an S3 Bucket
Copy a file from local storage to an S3 bucket:
```sh
aws s3 cp file.txt s3://myaws-s3-bucket
```

## Removing an Object Inside a Bucket
Delete a specific object from an S3 bucket:
```sh
aws s3 rm s3://myaws-s3-bucket/file.txt
```

## Deleting an S3 Bucket
Remove an empty S3 bucket:
```sh
aws s3 rb s3://myaws-s3-bucket
```




## References:  
````
https://docs.aws.amazon.com/cli/latest/reference/iam/create-group.html
````

````
https://docs.aws.amazon.com/cli/latest/reference/s3/
````
