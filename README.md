# LEBERTRAN

Extends the deno `file_server` from `std` with live reload via websocket.

## INSTALL

Install latest version of `lebertran` from [deno.land:](https://deno.land/x/lebertran/)

    deno install --allow-net --allow-read --import-map=https://deno.land/x/lebertran/import_map.json https://deno.land/x/lebertran/lebertran.ts

## RUN

In plain HTTP/WS mode:

    lebertran someFolderOnYourComputer

In secure HTTPS mode you will need to pass a certificate and key file:

    lebertran -c localhost.crt -k localhost.key someFolderOnYourComputer",

## DEVELOPMENT

For local development `lebertran` will need localhost certificates (`openssl` needs to be installed):

    deno task certs

Then `lebertran` can be started in secure mode (HTTPS and WSS enabled) mode with automatic reloading. The contents of the `www` folder in the root directory will be used :

    deno task dev

### PRIOR ART

`Lebertran` (code and name) was inspired by [`denoliver`](https://github.com/joakimunge/denoliver) from [@joakimunge](https://github.com/joakimunge)
