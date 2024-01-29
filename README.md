## BeSLighthouse
Pronounced as "B-e-S Lighthouse", is a dashboard project for visulaizing the security assessment and risk posture of open source projects and ML models tracked by a BeS lab deployment. BeSecure community hosts an instance of BeSLighthouse [here](https://be-secure.github.io/BeSLighthouse/).

## Getting Started
BeSLighthouse is a [React](https://react.dev/) based web interface project that expects a BeS lab ecosystem datastore to pull the data and visualize it. The BeSecure community datastore is maintained in GitHub.com under Be-Secure namespace. 

### Run BeSLighthouse locally
To try out BeSLighthouse on your own machine, clone the latest release tag and set up the datastore.

#### Prerequisites
- Install NodeJS v16.0 or higher

#### Set up datastore
The current version of BeSLighthouse assumes that the lab assets details are stored in a Git repository structure. The [datastore.ts](https://github.com/Be-Secure/BeSLighthouse/blob/main/src/dataStore.ts) file should be edited to point to your lab's datastore repository. The path urls you see now in the file points to the BeSecure community lab datastore. You can create a Git repository structure in your GitHub or GitLab namespace as given below. Then update the path variables in datastore.ts file.

    - Be-Secure
        - besecure-assets-store
        - besecure-assessment-datastore
        - besecure-ml-assessment-datastore

#### Start BeSLighthouse
- Clone the latest release tag into your local machine
- Update datastore.ts with the path 
- Build and start the project

```
> npm install --force

Set the environment variable NODE_OPTIONS to --openssl-legacy-provider. This environment variable is used to specify options or flags to be passed to the Node.js runtime. In this case, it sets the OpenSSL provider to use the legacy provider instead of the default one.

Linux / MacOS
> export NODE_OPTIONS=--openssl-legacy-provider

Windows Powershell / CMD
> set NODE_OPTIONS=--openssl-legacy-provider

> npm start
```

## Usage
A BeS lab ecosystem focus on addressing common security requirements of open source projects, ML models and ML datasets. BeSLighthouse is the face of a BeS lab instance. It gives a detailed view of the open source projects, ML models, ML datasets and the vulnerabilities being tracked in the lab.  

### Projects Of Interest (POI)
Open source projects tracked by the BeS lab is listed in the POI dashboard. The tracking involes forking the open source projects into the Git namespace of the lab and proactively assess each version source code for vulnerabilities. Project details page gives the comprehensive view of the risk posture of the proejct, including the known vulnerabilities.

### Vulnerabilities Of Interest (VOI)
Known vulnerabilities that are of interest to the BeS lab is listed in the VOI dashboard. The lab may want to share the information about known vulnerabilities and the affected projects within its tracked projects.

### Models Of Interest (MOI)
Pretrained machine learning models are available in various public platforms that can put to use for many useful usecases. These open source models may contain severe secutiry vulnerabilities. The ML models tracked by the lab is listed in MOI dashboard. Model card (details page) gives a holistic view of the risk posture and the various attack emulation on that particular model.

### Datasets of Interest (DOI)
Publicly availbable training dataset that are of interest to the BeS lab is listed in the DOI dashboard. Currently not available for public access. This feature is coming soon.

## Technology Stack
- NodeJS
- React
- Typescript

## Report Issue
BeSLighthouse uses GitHub's integrated issue tracking system to record bugs and feature requests. If you want to raise an issue, please follow the recommendations below:

* Before you log a bug, please search the [issue tracker](https://github.com/Be-Secure/BeSLighthouse/issues) to see if someone has already reported the problem.
* If the issue doesn't already exist, [create a new issue](https://github.com/Be-Secure/BeSLighthouse/issues/new/choose).
* Please provide as much information as possible with the issue report.
We like to know the BeSLighthouse version you're using.
* If possible, try to attach the screenshot of the issue.

## License
BeSLighthouse is an Open Source software released under the [Apache 2.0 license](https://www.apache.org/licenses/LICENSE-2.0.html).