# Voltage Monitor

The voltage monitor microservice for the R nineT Scrambler navigation tower uses the
[ads1015](https://github.com/sailingscally/ads1015) Node.JS module to read various relevant voltages and
publishes the values to the following MQTT topics:

- `voltage/main` - main system voltage
- `voltage/ups` - *(to be implemented)*

## Running the Service

To run the service on system startup, the [PM2](https://pm2.keymetrics.io/) process manager for Node.JS
applications is used. It provides process monitoring capabilities which are great for this application.
To start the service run:

```
pm2 start app.js --name volts --watch --time
```
