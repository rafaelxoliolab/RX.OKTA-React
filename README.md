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
