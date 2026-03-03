# Deployment Instructions for Google Cloud

This document provides step-by-step instructions for deploying the Crecemax WhatsApp Bot on Google Cloud.

## Prerequisites
- A Google Cloud account.
- Google Cloud SDK installed on your local machine.
- A project created in Google Cloud.
- Billing enabled for your Google Cloud project.

## Step 1: Setup Google Cloud SDK
1. Open your terminal or command prompt.
2. Authenticate your Google Cloud SDK by running:
   ```bash
   gcloud auth login
   ```
3. Set your project as the active project:
   ```bash
   gcloud config set project YOUR_PROJECT_ID
   ```

## Step 2: Create a Cloud Storage Bucket
1. Create a bucket to store assets:
   ```bash
   gsutil mb gs://YOUR_BUCKET_NAME
   ```
2. Upload all necessary files for the bot to the bucket:
   ```bash
   gsutil cp -r /path/to/your/bot/files/* gs://YOUR_BUCKET_NAME/
   ```

## Step 3: Deploy the Application
1. Navigate to the directory of your bot application.
2. Deploy the application using App Engine:
   ```bash
   gcloud app deploy
   ```

## Step 4: Configure Environment Variables
1. Set environment variables as needed by the bot:
   ```bash
   gcloud run services update YOUR_SERVICE_NAME --set-env-vars KEY=VALUE
   ```

## Step 5: Access the Bot
1. After deployment, access your bot at:
   ```
   https://YOUR_PROJECT_ID.appspot.com
   ```

## Conclusion
You have successfully deployed the Crecemax WhatsApp Bot on Google Cloud. For further instructions, refer to the official [Google Cloud documentation](https://cloud.google.com/docs).