# Update package lists

```bash
sudo apt update

# Add the deadsnakes PPA which has newer Python versions
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa

# Install Python 3.9
sudo apt install python3.9
```
# install aws cli
```bash
sudo apt update
sudo apt install awscli
```
# Configure aws
```bash
aws configure
```
AWS Access Key ID [None]: Paste the Access key ID you saved in Part 2 and press Enter.

AWS Secret Access Key [None]: Paste the Secret access key you saved and press Enter.

Default region name [None]: us-west-2

Default output format [None]: Press enter or use json

# Install pip 

```bash
pip install iam-ape
```

# Update ape 

```bash
iam-ape --update
```

# List your usernames

```bash
aws iam list-users
```
Copy the <arn> and paste in the below command 

# Here we have 2 ways 
1. Live Fetch from AWS
2. Using a Local File (More Efficient)

# First Way
# Run the arn 

```bash
iam-ape --arn arn:aws:iam::<aws-accountid>:user/<username> --profile default
```

# Second Way
# Get account authorization details

```bash
aws iam get-account-authorization-details > auth-details.json
```

# Point APE to this file:

```bash
iam-ape --arn arn:aws:iam::<aws-accountid>:user/<username> --input auth-details.json
```
