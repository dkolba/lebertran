# LEBERTRAN

Extends the deno `file_server` from `std` with live reload via websocket.

## INSTALL

Install `lebertran` from this repo as a command-line tool:

    deno install --allow-net --allow-read --import-map=deno.jsonc ./lebertran.ts

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
