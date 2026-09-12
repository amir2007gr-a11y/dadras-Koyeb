# Dadras — Koyeb Ready

## Koyeb deployment
1. Upload these files to the root of a GitHub repository (do not upload the ZIP itself as the project source).
2. In Koyeb choose **Create Web Service** → **GitHub** and select the repository.
3. Use the Dockerfile builder if Koyeb asks for a builder. The included Dockerfile exposes port 3000 and runs `npm start`.
4. If using Buildpack instead, use:
   - Build command: `npm install`
   - Run command: `npm start`
   - Port: `3000`
5. The app listens on `0.0.0.0` and automatically uses Koyeb's `PORT` environment variable.

## Important
The JSON database (`dadras-data.json`) is local to the running instance. On hosts with ephemeral storage, data can be lost after a redeploy/restart. For permanent user/activity/quiz/result storage, move the database to a persistent external database later.
