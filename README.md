# RX.OKTA-React
Sample about Implementing Okta authentication in a React app

## Prerequisites
* To be familiared with Javascript 

## Setting up OKTA

### Sing up for the developer edition of Okta

- Go to https://developer.okta.com/signup/
- Create a developer account


### Create an OKTA Integration configuration

1. Go to OKTA.com
2. Sing-in with your OKTa account
3. Go to Applications
4. Click on `Create App Integration` button
  ```
  - Sign-in method:OIDC-OpenID Connect
  - Application Type: Single-Page Application
  - Configure the App
  -- App integration name: Test-SPA-OKTA
  -- Sig-in redirect URIs: http://localhost:3000/login/callback
  -- Sign-out redirect URIs :  http://localhost:3000
  ```
5. Save 

### OKTa Application Details
Once the OKTA application integration has been created, the Application details page will be displayed, 
there you can see the information requiered to connect OKTA with React:

- ClientID
- Client authentication
- Okta domain

## Integration with React

### Create a new React application

1. Go to VS code
2. Open a new terminal
3. run command `npx create-react-app test-spa-okta-react`
4. move into the app folder `cd test-spa-okta-react`
5. run command `npm start`

### Install OKTA SDK and OKTA Auth JavaScript SDK 

1. Go to VS code
2. Open a new terminal
3. Run command 
  ```
  # yarn
  yarn add @okta/okta-auth-js @okta/okta-react

  # npm
  npm install --save @okta/okta-auth-js @okta/okta-react'
  ```
### Configure OKTA data in .env file

1. Create a new file .env on root
2. Create and configure environmental variables
```
OKTA_DOMAIN=<YOUR_OKTA_DOMAIN>
CLIENT_ID=<YOUR_CLIENT_ID>
CALLBACK_PATH='/login/callback'
ISSUER='https://<YOUR_OKTA_DOMAIN>/oauth2/default'
HOST='window.location.host'
SCOPES='openid profile email'
```


  



