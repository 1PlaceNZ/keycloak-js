# Keycloak-js
This is an extended version of the existing keycloak.js Adapter. It's the same code with a few modification.


## Change log

### 16.1.1-id-token-hint

Made the module compatible when running keycloak 18.x.x with legacy-logout-redirect-uri=true.
This module will also work when running keycloak < 18 as well
Added `id_token_hint` to createLogoutUrl method to removed the confirm logout screen.
Removed `hidden=yes`  from the logout process for `cordova` adapter

### 16.1.1 

Copy of keycloak-js@16.1.1 re formatted into a layout to easily publish to a npm repository 

## to build

 mvn package

This creates a `npm`  folder in the `target` folder where you can publish the modified package

    cd target/npm/

    rmdir css  //empty css folder to remove
    npm login --registry <npm registry>
    npm publish --registry <npm registry>

## License

* [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
