# Keycloak-js

This is an extended version of the existing keycloak.js Adapter. It's the same code with a few modification.

## Change log

### 25.0.6-id-token-hint

Update keycloak-js to 25.0.6
Applies the `cordova-native` adapter code (login/logout function) from the version '16.1.1-id-token-hint-oauth'

### 16.1.1-id-token-hint-oauth

Change the `cordova-native` adapter code to use the `cordova-plugin-oauth` (https://github.com/1PlaceNZ/cordova-plugin-oauth.git branch feature/OpenID)

### 16.1.1-id-token-hint

Made the module compatible when running keycloak 18.x.x with legacy-logout-redirect-uri=true.
This module will also work when running keycloak < 18 as well
Added `id_token_hint` to createLogoutUrl method to removed the confirm logout screen.
Removed `hidden=yes` from the logout process for `cordova` adapter

### 16.1.1

Copy of keycloak-js@16.1.1 re formatted into a layout to easily publish to a npm repository

## to build

We need to install npm dependencies and build the keycloak js, then pack the output into tgz file.
Update the properties section in the pom.xml if your node/npm version are different.

npm install

npm run build

mvn clean package

This creates keycloak-js-25.0.6-id-token-hint.tgz in the `target` folder where you can publish the modified package

    cd target
    npm login --registry <npm registry>
    npm publish --registry <npm registry>

for beta or testing

npm publish keycloak-js-25.0.6-id-token-hint.tgz --registry https://jenkinstest.1placeonline.com:4873/ --tag beta

npm install --registry https://jenkinstest.1placeonline.com:4873 keycloak-js --tag beta

## License

-   [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
