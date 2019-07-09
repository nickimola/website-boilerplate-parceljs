# Getting Started

* Install parcelJS if you don't have it already on your machine https://parceljs.org/
* `git clone https://github.com/nickimola/website-boilerplate-parceljs.git`
* `cd website-boilerplate-parceljs` 
* `npm i` or `yarn install`
* `yarn run dev` and navigate to `localhost:1234` to see the placeholder page.

## Structure

* All the soruce files are located inside `./src/`
* All the asset files are located inside `./src/assets/`

## Features

#### PWA
In order for you to have this as PWA you need a valid manifest file (navigate to https://tomitm.github.io/appmanifest/ to get one) and copy the resulting manifest file inside `./src/manifest.webmanifest`

#### Service worker
By default, the service worker is commented out and disabled for development purposes.
To enable it, simply uncomment the code you find inside `./src/assets/scripts/index.js`.
The default behaviour is to cache all the files necessary for your app to run properly. Inside `./package.json` you can adjust the `maximumFileSizeToCacheInBytes` to better suit your needs.

#### Font face
 I've included a really nice scss file that helps with font face css generation.
The full documentation and instructions on how to use it can be found here: https://gist.github.com/jonathantneal/d0460e5c2d5d7f9bc5e6

#### Google fonts
If you use google fonts, I've included DNS-prefetch and Preconnect on `./src/index.html` to optimize google fonts loadings. (you can read more about it here: https://www.smashingmagazine.com/2019/06/optimizing-google-fonts-performance/?ref=devawesome.io)

#### Cookie policies
I've included a banner that comes in and asks for cookie policies agreement.
The script I used comes from https://cookieconsent.osano.com/download/ (documentation on how to set this up available on the page) and I've generated the privacy policy explanation here: https://www.cookiepolicygenerator.com/generator

#### From Dev to Prod
Once you're happy with your website or PWA you can run `yarn run build` to minify ad optimise your application using parcel default options.

> NB: it's reccomended you delete the `./dist` and `.cache` folders before running `build` task. Also, if you have service worker enable remember to clear all the website storage and be sure you're now looking at a cached version.