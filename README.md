# react-native-aws-withauthenticator
Step by step instruction for setting up AWS Cognito withauthenticator and React Native using Expo

## AWS Setup
#### Step 1: Create a new Mobile Hub project from AWS Console
#### Step 2: Add the "User Sign-in" Cognito backend and configure
#### Step 3: Download the cloud config zip file from "Integrate" and extract aws-exports.js

## Client Setup
#### Step 1: Create a new expo project
exp init react-native-withauthenticator
cd react-native-withauthenticator
#### Step 2: Add and install aws-amplify libries
npm add --save aws-amplify
npm add --save aws-amplify-react-native
npm install
#### Step 3: Add the extracted aws-exports.js file in the project directory
#### Step 4: In App.js, import new libraries and the config file
```import Amplify from 'aws-amplify';
import { withAuthenticator } from 'aws-amplify-react-native';
import aws_exports from './aws-exports';
```

#### Step 5: In App.js, configure Amplify
```Amplify.configure(aws_exports);```

#### Step 6: In App.js, use withAuthenticator component
```export default withAuthenticator(App);```

#### References
- https://github.com/aws-amplify/amplify-js/
- https://aws-amplify.github.io/amplify-js/media/authentication_guide.html
