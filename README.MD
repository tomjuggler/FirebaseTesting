Using Firebase Realtime Database to store incremental data. Test code, without authentication.

Based on: https://cloud.google.com/community/tutorials/building-flask-api-with-cloud-firestore-and-deploying-to-cloud-run

First you need to generate firebase_key.json in google cloud console. 
Enable the Google Cloud Console permissions (I AM) for the project - Realtime Database, as well as Cloud Build, Cloud Run. Helpful documentation: https://cloud.google.com/build/docs/deploying-builds/deploy-cloud-run

Add firebase_key.json to project root. 
Add firebase_key.json to .gitignore.

deploy to the cloud with Google Cloud SDK: 
need to remove firebase_key.json from .gitignore for this to work!
gcloud builds submit --config cloudbuild.yaml .