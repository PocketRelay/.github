# Manager Setup

> This is a setup guide for allowing the server to be managed using the Management software [Here](https://github.com/PocketRelay/PocketRelayManager)

If you would like to enable the management client you will need to first enable the API and set the username and password that will be used for the manager.

## 1) Enable API

The manager requires the API to be enabled in order to access information from the server. In order to do this you must set the `PR_API` environment variable to `true` this can be done using the system environment variables or by creating a file name `.env` in the same directory as the server executable and adding the following lines to it

```shell
PR_API=true
```

## 2) Set Credentials

It is recommended that you change the default username and password for the server otherwise anyone who finds the default credentials will be able to use the Management software with your server. In order to do this you must set the `PR_API_USERNAME` and `PR_API_PASSWORD` environment variables to the username and password you would like.  This can be done using the system environment variables or by creating a file name `.env` in the same directory as the server executable and adding the following lines to it

```shell
PR_API_USERNAME=TheUsernameYouWantToUse
PR_API_PASSWORD=ThePasswordYouWantToUse
```

## 3) Restart

You will now need to restart the server in order to apply the changes you can do this by simply closing the executable or using Ctrl+C on the terminal then start it again like before

## 4) Connect

Now that you have restarted you can now enter the Connection URL from the startup message into your Pocket Relay Manager client and then enter the username and password you chose and connect