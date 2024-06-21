# Demo: Matomo Analytics & CO2.js

This page is a demonstration of how the [Performance Resource Timing API](https://developer.mozilla.org/en-US/docs/web/api/performanceresourcetiming) can be used with [CO2.js](https://github.com/thegreenwebfoundation/co2.js/tree/main) on a web page, and then report those values to Matomo Analytics.

This demo page uses the iife version of CO2.js, meaning that the entire library is loaded into the page. This isn't an ideal solution, but works for a proof of concept.

At present, a script runs when the page is loaded (window state is `load`). This script uses the Performance Resource Timing API to collect information about the data transferred when the pay was loaded. This information is then fed into CO2.js which uses it to provide a carbon emissions estimate based on the Sustainable Web Design Model version 3.

_At the moment this, demonstration does not make any adjustments to grid intensity based on server location or user location, nor does it make any checks to see if the web page is hosted on a Green web host. This should be noted as changes to these variables would affect the final carbon emissions estimate produced on this page._

## Demo

View online at: [https://fershad.github.io/matomo-co2js-demo/](https://fershad.github.io/matomo-co2js-demo/)

## Run locally

1. Clone this repository.
2. Navigate to root folder for this project on your device.
3. Run `npm run start`. This will install the `http-server` package and spin up a local server.
4. Visit [http://localhost:8080](http://localhost:8080) to view the demo.
