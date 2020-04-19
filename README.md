# Cloud Run Functions Framework Nodejs
A boilerplace for a basic [functions framework](https://github.com/GoogleCloudPlatform/functions-framework-nodejs) based nodejs app that runs on Google Cloud Run. Includes a *dev.yaml* for local docker development with hot reloading. 

## Run Locally With Docker Compose (dev.yaml)
_Supports Hot-Reloading on File Change_

`npm run up:dev`
- This uses docker-compose **dev.yaml** configuration to serve locally in a docker environment (as opposed to running on our local machine with our natively installed node version). This is closer to cloud-run production environment.
    - In dev.yaml, the local working directory is mapped to the docker instance.
    - The dev.yaml **command** installs [nodemon](https://www.npmjs.com/package/nodemon), which watches for file changes and allows **hot reloading**, so we can see changes on file-change without rebuilding the image.
    - When the docker instance is running, make a change to **index.js**, save, and reload your browser to instantly see changes reflected.
- Requires docker to be installed on your machine
- Close the image down with `npm run down:dev`
