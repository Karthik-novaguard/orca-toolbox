# GCP Lateral Movement Detector 

The script iterates through all the available projects (according to your token's access level) in your GCP account and extracts the compute engine instances that can access all compute engine instances in it's project's scope (e.g. can use the command gcloud compute ssh to access other VMs in the same project).

It is based on the misconfiguration of a compute engine instance configured with the default service account (with editor role) and all cloud api access scope.

Deploying compute engine instances with permissive permissions of the default service account is a bad practice and should be avoided at all times.

Examine the results to quickly identify this misconfiguration and prevent attackers from spreading throughout your GCP environment.

# Disclaimer
This tool is for testing and educational purposes only. 

Any other usage for this code is not allowed. Use at your own risk.

The author bears NO responsibility for misuse of this tool.

By using this you accept the fact that any damage caused by the use of this tool is your responsibility.

# Dependencies
1. Install the gcloud sdk prior running the script.
You can get the installation instructions for your OS here:
https://cloud.google.com/sdk/docs/install

2. Sudo apt-get install jq

# Usage 
./gcp-lateral-movement-detector.sh -o results.txt

# TODO
Add iteration for organizations level

# Author
<a href="https://twitter.com/ellicho007">Liat Vaknin</a>
