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

*This is sourced from the [Google Developer docs](https://developers.google.com/web/fundamentals/primers/service-workers). Make sure to change the .register('/sw.js') to .register('/push-worker.js')