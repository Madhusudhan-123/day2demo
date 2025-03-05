# day2demo
# AWSGLUE
First, install Boto3 if you haven’t already:
pip install boto3
Then, configure AWS credentials using:
aws configure
or set them in your script:
import boto3

aws_access_key = "your-access-key"
aws_secret_key = "your-secret-key"
region = "us-east-1"

glue_client = boto3.client(
    "glue",
    aws_access_key_id=aws_access_key,
    aws_secret_access_key=aws_secret_key,
    region_name=region
)
# AWSREDSHIFT
# Python's boto3 library allows programmatic control over AWS Redshift.
Install Boto3
pip install boto3 
Initialize Boto3 Client
import boto3 redshift = boto3.client('redshift', region_name='us-east-1') 
Madhu awsredshift cluster = redshift.describe_clusters() for cluster in clusters['Clusters']: print(cluster['ClusterIdentifier'], cluster['ClusterStatus']) 
# Create a Redshift Cluster
•	
response = redshift.create_cluster( ClusterIdentifier='my-redshift-cluster', NodeType='dc2.large', MasterUsername='admin', MasterUserPassword='MySecurePassword', ClusterType='single-node' ) print(response) 
