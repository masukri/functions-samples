# Cloud Functions for Firebase Sample Library

This repository contains a collection of samples showcasing some typical uses of [Cloud Functions for Firebase](https://firebase.google.com/features/functions).

### What's Cloud Functions for Firebase?

Cloud Functions is a hosted, private, and scalable Node.js environment where you can run JavaScript code. [Cloud Functions for Firebase](https://firebase.google.com/features/functions) integrates the Firebase platform by letting you write code that responds to events and invokes functionality exposed by other Firebase features.

## Prerequisites

To learn how to get started with Cloud Functions for Firebase by having a look at our [Getting Started Guide](https://firebase.google.com/docs/functions/get-started), trying the [quickstart samples](/quickstarts) and looking at [the documentation](https://firebase.google.com/docs/functions).


## Samples Overview

This repository contains two kinds of samples:

1. **Development Environment Samples** illustrate how to get started with
different, commonly used JavaScript development patterns.
2. **Sample Functions** integrate back-end services or provide sample code for
common applications for Cloud Functions.


## Development Environment Samples

The Firebase CLI generates sample code for Cloud Functions using JavaScript
that is natively supported in NodeJS. Most developers use more modern
JavaScript or TypeScript which requires additional tools.

### [Write Cloud Functions using TypeScript](/typescript-getting-started)

This sample shows how you can write your Cloud Functions code using Typescript.
This requires a buld step, included as an npm script, which transpiles the
source code to a supported version of JavaScript.
Uses an **HTTPS request**.


### [Write Cloud Functions using ES2017 code](/es2017-transpile)

This sample shows how you can write your Cloud Functions code using the ES2017
syntax. This requires to run a preparation step where your code is transpiled to
a supported version of JavaScript.
Uses a **Firebase Realtime Database trigger**.


## Sample Functions

### [Realtime database trigger quickstart: Uppercaser](/quickstarts/uppercase)

This quickstart sample demonstrates using **Cloud Functions** triggered by **Firebase Realtime Database events**. The function uppercase messages written to the datastore.

### [HTTPS trigger quickstart: Time Server](/quickstarts/time-server)

This quickstart sample demonstrates using **Cloud Functions** triggered by **HTTPS requests**. The function returns the current server time and allows for date time formatting.

### [Hosting triggered HTTPS function quickstart: Big Ben](/quickstarts/big-ben)

This quickstart demonstrates using **Cloud Functions** with an HTTPS trigger that's triggered through a Firebase Hosting URL. The function will display a repeated number of "BONG" depending on the hour of the day.

### [Cloud Storage trigger quickstart: Thumbnail generator](/quickstarts/thumbnails)

This quickstart sample demonstrates using **Cloud Functions** triggered by **Firebase Storage events**. The function generates a thumbnail of uploaded images.

### [Auth trigger quickstart: Welcome Email](/quickstarts/email-users)

This quickstart sample demonstrates using **Cloud Functions** triggered by **Firebase Auth events**. The functions sends a Welcome email when user accounts are created (or when users signs-in using an Identity Provider for the first time) and sends a Goodbye email when user accounts are deleted.

### [PubSub trigger quickstart: Hello World](/quickstarts/pubsub-helloworld)

This quickstart sample demonstrates using **Cloud Functions** triggered by **PubSub events**. The functions log the PubSub payload in a Hello world message.

### [Authenticated JSON API](/authenticated-json-api)
This sample shows how to authenticate access to a JSON API to only allow access to data for a specific Firebase user.

### [Authorized HTTP endpoint](/authorized-https-endpoint)

This samples shows how to restrict an HTTPS Function to only the Firebase users of your app.
Only users who pass a valid Firebase ID token as a Bearer token in the `Authorization` header of the HTTP request or in a `__session` cookie are authorized to use the function.
Checking the ID token is done with an ExpressJs middleware that also passes the decoded ID token in the Express request object.
Uses an HTTP trigger.

### [Server-side generated pages w/ Handlebars templating and user sessions](/template-handlebars)

This samples shows how to serve server-side generated HTML pages using the [HandlebarsJs](http://handlebarsjs.com/) templating system and serve User specific content by always passing the Firebase ID token in a `__session` cookie.

### [Google Assistant says ordinal of given number](/assistant-say-number)

This sample shows how to create an action for the Google Home/Assistant using the Actions SDK hosted on Cloud Functions. The sample action asks users to say a number and reads out the ordinal of that number.
Uses an HTTP trigger.

### [Send FCM notifications](fcm-notifications)

This sample demonstrates how to send a Firebase Cloud Messaging (FCM) notification from a Realtime Database triggered Function when users get new followers. The sample also features a Web UI to experience the FCM notification.
Uses a Realtime Database trigger.

### [Authorize with LinkedIn](/linkedin-auth)

Demonstrates how to authorize with a 3rd party sign-in mechanism (LinkedIn in this case), create a Firebase custom auth token, update the user's profile and authorize Firebase.
Uses an HTTP trigger.

### [Image Maker](/image-maker)
This sample demonstrates how to create various customized images through Cloud Functions and Hosting and serve it to the client.

### [Authorize with Instagram](/instagram-auth)

Demonstrates how to authorize with a 3rd party sign-in mechanism (Instagram in this case), create a Firebase custom auth token, update the user's profile and authorize Firebase.
Uses an HTTP trigger.

### [Isomorphic React App](/isomorphic-react-app)
This sample demonstrates how to create an isomorphic React application with server-side data fetching. This sample uses Cloud Functions, Hosting, and the Realtime Database.

### [Authorize with LINE](/line-auth)

Demonstrates how to authorize with a 3rd party sign-in mechanism (LINE in this case), create a Firebase custom auth token, update the user's profile and authorize Firebase.
Uses an HTTP trigger.

### [Convert images after upload](/convert-images)

Demonstrates how to automatically convert images that are uploaded to Firebase Storage to JPEG using ImageMagick.
Uses a Firebase Storage trigger.

### [Generate image thumbnails using ImageMagick](/generate-thumbnail)

Demonstrates how to automatically generate a thumbnail for images that are uploaded to Firebase Storage using ImageMagick and generate a public download link for the images.
Uses a Firebase Storage trigger.

### [Generate image thumbnails using Node.js Stream & Sharp](/image-sharp)

Demonstrates how to use Node.js Stream to read image from Cloud Storage, generate a thumbnail image using Sharp and upload it back to Cloud Storage.
Uses a Firebase Storage trigger.

### [Post GitHub commits to Slack channel](/github-to-slack)

Demonstrates how to automatically post GitHub commits to a Slack channel using an HTTPS triggered Function.

### [Create and charge Stripe customers](/stripe)

Demonstrates hows to integrate Firebase Auth and the Realtime database with Stripe via the Stripe Node.js library.

### [Moderate offensive images](/moderate-images)

Demonstrates how to automatically moderate offensive images that are uploaded to Firebase Storage by using the Google Cloud Vision API to detect offensive images and ImageMagick to blur these images.
Uses a Firebase Storage trigger.

### [Extract image metadata](/exif-images)

Demonstrates how to automatically extract image's metadata using ImageMagick for images that are uploaded to Firebase Storage.
Uses a Firebase Storage trigger.

### [Text moderation](/text-moderation)

How to moderate user input text for bad words. For example this can be used to moderate usernames, chat or forum messages.
Uses a Realtime Database trigger.

### [Email confirmation](/email-confirmation)

Sends email confirmation after users subscribed to a mailing list.
Uses a Realtime Database trigger.

### [LastModified Firebase Database tracking](/lastmodified-tracking)

Tracking when the Firebase Database (or a subset) was last modified.
Uses a Realtime Database trigger.

### [Webhook upon Firebase Database writes](/minimal-webhook)

Writing to the Firebase Database triggers a request to a callback URL (a Webhook). The content of the modified Data is sent to the Webhook.
Uses a Realtime Database trigger.

### [Firebase Database child nodes count](/child-count)

Keeps track of the number of child nodes of a Firebase Database element allowing clients to filter or order results using the child count.
This can be useful to keep tack of the number of "likes" or "followers" of a somethings shares through social media.
Uses a Realtime Database trigger.

### [Automatic message translation](/message-translation)

Integrates the Google Translate API to perform automatic text translation across any number of languages. Language codes can be stored in Firebase for on the fly changes.
Uses a Realtime Database trigger.

### [Automatic URL shortener](/url-shortener)

Integrates the Google URL Shortener API to shorten URLs automatically as they are added to the database.
Uses a Realtime Database trigger.

### [Limit number of child nodes](/limit-children)

Make sure to keep the number of child nodes below a certain threshold. For instance this can be useful to limit the number of lines of logs or chat history below a given number.
Uses a Realtime Database trigger.

### [Import data into Big Query](/bigquery-import)

Copies Firebase Database elements into BigQuery automatically. This can be useful for instance for further logs analysis.
Uses a Realtime Database trigger.

### [Full-text search via Algolia](/fulltext-search)

Enable full-text search on firebase database elements by using an Algolia hosted search service.
Uses a Realtime Database trigger.

### [User data cleanup](/user-data-cleanup)

Deletes all associated user data that's on the Realtime database when a user deletes his Firebase account.
Uses an Auth trigger.

### [Send a survey when users update your app](/survey-app-update)

This sample shows how to send a survey to your users who have updated your app. App Update is detected using a Firebase Analytics event.
Uses an Analytics trigger.

### [Send a coupon to user who have completed a purchase](/coupon-on-purchase)

This sample shows how to send a coupon to your users who have just purchased something. 10% off on your next purchase!
Uses an Analytics trigger.

### [Delete inactive users accounts via cron](/delete-unused-accounts-cron)

Periodically deletes the accounts of users who have not signed in the last month.
Uses an HTTPS trigger.

### [Username/password sign in with Firebase](/username-password-auth)

Demonstrates how to authorize with a username/password sign-in mechanism, create a Firebase custom auth token, update the user's profile and authorize Firebase.
Uses an HTTP trigger.

### [Developer Motivator](developer-motivator)

This sample demonstrates how to send a Firebase Cloud Messaging (FCM) notification to the developer device each time your app get a new user or lose one.
Uses an Analytics trigger.

## Contributing

We'd love that you contribute to the project. Before doing so please read our [Contributor guide](CONTRIBUTING.md).


## License

© Google, 2015-2017. Licensed under an [Apache-2](LICENSE) license.
