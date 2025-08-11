# Webresume

## Setup

Create and configure the bucket (one time).

```bash
gcloud config set project webportfolio-399411
gcloud services enable storage.googleapis.com
gsutil mb -l us-east1 -b on gs://thomasbersez/
gsutil iam ch allUsers:objectViewer gs://thomasbersez
gsutil web set -m index.html gs://thomasbersez
```

Upload files:

```bash
gsutil cp -r index.html src gs://thomasbersez
```

The website is served at `https://storage.googleapis.com/thomasbersez/index.html`.
