# GCP

testing GCP API and client, notes for references

## Google Cloud REST API

```shell
python -m venv venv
source venv/bin/activate
pip install -r requirements

```

## Google Cloud CLI - gcloud

```shell

# install gcloud 
sudo tee -a /etc/yum.repos.d/google-cloud-sdk.repo << EOM
[google-cloud-cli]
name=Google Cloud CLI
baseurl=https://packages.cloud.google.com/yum/repos/cloud-sdk-el8-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=0
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg
       https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOM

sudo dnf install libxcrypt-compat.x86_64
sudo dnf install google-cloud-cli

# initialize
gcloud init

# activate using the service account
gcloud auth activate-service-account insights-qe@optimal-shard-347020.iam.gserviceaccount.com  --key-file=/home/ecerquei/.ssh/optimal-shard-347020-471eb80d20a1.json

# listing accounts
gcloud auth list

# listing compute/VMs
gcloud compute instances list
```

### Links

* [install](https://cloud.google.com/sdk/docs/install)
* [initialize](https://cloud.google.com/sdk/docs/initializing)
* [Authorizing SA](https://cloud.google.com/sdk/docs/authorizing)
* [filtering with glcoud cli](https://cloud.google.com/sdk/docs/scripting-gcloud#filtering_and_formatting_output)

