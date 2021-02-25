# Configuring Airship
This is a tutorial on utilizing airship on your web app.

<img align="center" alt="redesign of thumbnails" width="500px" src="https://vectorlogoseek.com/wp-content/uploads/2019/07/urban-airship-inc-vector-logo.png" />

## Table of Contents
1. [Development Setup](#development-setup)
1. [Running](#running)
1. [Dependencies](#dependencies-overview)
1. [Workflow](#workflow)
1. [UX Research](#ux-research)

## Step 0: Login to your dashboard > Select project

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/0-step.png?raw=true" />

## Step 1: Settings > Channels

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/1-step.png?raw=true" />


## Step 2: Channels > Web Notifications 
## Add a title > URL > Img URL > Hit Update

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/2-step.png?raw=true" />


## Step 3: Download SDK Bundle

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/3-step.png?raw=true" />

## Step 4: Unzip SDK Bundle (anywhere)

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/4-step.png?raw=true" />

## Step 5: There should be 3 files within the SDK

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/5-step.png?raw=true" />

## Step 6: Copy snippet.html to your index.html / index.php (bottom)

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/6-step.png?raw=true" />

## Step 7: Place the push-worker.js into the root directory of index

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/7-step.png?raw=true" />

## Step 8: Register a service worker in your index.html / index.php

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/8-step.png?raw=true" />


```
<script>
if ('serviceWorker' in navigator) {
  window.addEventListener('load', function() {
    navigator.serviceWorker.register('/sw.js').then(function(registration) {
      // Registration was successful
      console.log('ServiceWorker registration successful with scope: ', registration.scope);
    }, function(err) {
      // registration failed :(
      console.log('ServiceWorker registration failed: ', err);
    });
  });
}
</script>
```

*This is sourced from the [Google Developer docs](https://developers.google.com/web/fundamentals/primers/service-workers). Make sure to change the .register('/sw.js') to .register('/push-worker.js').

## Step 9: Run index.html on a live server. Right click > Inspect > Console > Ensure the service worker registration is successful

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/9-step.png?raw=true" />


## Step 10: Also ensure the push worker is showing in the Console > Sources

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/10-step.png?raw=true" />

## Step 11: Go to system preferences

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/11-step.png?raw=true" />

## Step 12: Make sure notifications are turned on in your settings

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/12-step.png?raw=true" />

## Step 13
## Run the following code in your server's terminal 

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/13-step.png?raw=true" />

To allow notifications for your browser (this is usually ran with a button displayed on the frontend).
```

```

To get the user identifier of the browser (usually this works in tandem with the user login info) 
```
```

Make sure to copy that number. 


## Step 14: Go back to Airship > Audience > Test Groups

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/14-step.png?raw=true" />

## Step 15: Test Groups > Create Test Group 

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/15-step.png?raw=true" />

For large scale projects your groups will most likely be sectioned by user-type, etc. 

## Step 16: Fill in the group name to your choice > Create

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/16-step.png?raw=true" />

## Step 17: In that group > Add test user

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/17-step.png?raw=true" />

## Step 18: Fill in the details, Click Add

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/18-step.png?raw=true" />

Your User Identifier is the number discovered in [Step 13](#step-13)

## Step 19: Time to create a message > Messages > Messages Overview

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/19-step.png?raw=true" />

## Step 20: Create (in the top right corner) 

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/20-step.png?raw=true" />


## Step 21: Select Message

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/21-step.png?raw=true" />


## Step 22: Select Channel > And select one group of respective user

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/22-step.png?raw=true" />

In this case I chose the All Users group. Normally you would target specific users or test users.

## Step 23: What type of message is this > Select > Next

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/23-step.png?raw=true" />


## Step 24: Fill in details marked below > Next when done

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/24-step.png?raw=true" />


## Step 25: Delivery > Send Now (for testing purposes) 

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/25-step.png?raw=true" />


## Step 26: Delivery > Web Only > Require Interaction true

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/26-step.png?raw=true" />

This is a UX preference. Select items that match your UX needs.

## Step 27: Review and Send > Send Test

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/27-step.png?raw=true" />


## Step 28: Send a test message > Test audience > select the group we made in Step 18 > Send

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/28-step.png?raw=true" />

## Step 29: Rejoice! Your notif should show up

<img align="center" alt="redesign of thumbnails" width="800px" src="https://github.com/loreleim/airship/blob/main/images/29-step.png?raw=true" />



