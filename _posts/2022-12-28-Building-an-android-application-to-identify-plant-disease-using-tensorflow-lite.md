---
published: true
layout: post
date: 2020-8-10
---
### In this article, I will share the tools that I have used to build the plant disease identification app (available on Google playstore) and steps right from the start to its deployement.

**After making an new project on Android studio (or whatever IDE you use), get these plugins in your pubspec.yaml file.**

**1. Camera plugin:** This plugin will enable the app to capture images and stream image buffers to dart. We need this plugin to capture plant leaf image and then use our tensorflow model to give results.
Plugin: [link](https://pub.dev/packages/camera)

**2. TensorFlow lite plugin:** Tensorflow is open-source library for machine learning. I will use tensforflow specifically for model training. You can learn more about tensorflow on their [website](https://www.tensorflow.org/learn). 
You can use [teachable machine](https://teachablemachine.withgoogle.com/) to first create a demo machine learning model and then convert it to tensorflow lite so that you can check whether your app is displaying results as intended.
Plugin [link](https://pub.dev/packages/tflite)

**3. Cached Network Images:** The plugin cached network image will load and cache network images. Although it will make the application internet dependent but it will significantly reduce the size which is very important to compete with other apps on the Google playstore. Your download size matters a lot while convincing users to hit that install button. I hosted my images on imgbb.com, the loading times are pretty fast. Best thing about this plugin is that it caches the images once they are loaded. Next times user visits the same page, it feels like image is loaded instantly. I made the decision to use this plugin because I really want to reduce the size the app.
Plugin [link](https://pub.dev/packages/cached_network_image)

**4. Firebase core:** It connects the app multiple firebase services. I am using this to display articles from the firebase database. In future updates, I will enable authentication so that I can store profile specific user data to add more functionalities in the app. To use this plugin first you have to create a new application in firebase. If you are enabling authentication in the app then you have to enter you SHA key while setting up the app or you can do it after creating the app in the settings section. To get SHA fingerprint from android studio go to this [stackoverflow link](https://stackoverflow.com/questions/27609442/how-to-get-the-sha-1-fingerprint-certificate-in-android-studio-for-debug-mode).
I strongly recommend reading about the basics of firebase and the rules to setup database on their [website](https://cloud.google.com/firestore/docs/client/get-firebase).

