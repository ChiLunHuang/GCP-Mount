# GCP-Mount
The way to connecting to Cloud Storage buckets (Mount)

## Follow the steps from here
>https://github.com/GoogleCloudPlatform/gcsfuse/blob/master/docs/installing.md

**Install the package what you want**

`apt-get install python-pip`

**Mount**

`gcloud init`

`export GCSFUSE_REPO=gcsfuse-`lsb_release -c -s`
echo "deb http://packages.cloud.google.com/apt $GCSFUSE_REPO main" | sudo tee /etc/apt/sources.list.d/gcsfuse.list
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
`
`
sudo apt-get update
sudo apt-get install gcsfuse
`
**Make new directory to your path **
`
sudo mkdir /mnt/gcs-bucket
sudo chmod a+w /mnt/gcs-bucket
`

**Real time to update the data from bucket  

`sudo gcsfuse --implicit-dirs onead-hadoop /mnt/gcs-bucket`
