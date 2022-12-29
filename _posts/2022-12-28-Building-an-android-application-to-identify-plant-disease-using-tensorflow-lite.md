---
published: true
layout: post
date: 2020-8-10
---
### In this article, I will share the tools that I have used to build the plant disease identification app (available on Google playstore) and steps right from the start to its deployement.
I am using flutter because of its fast development cycles and ability to built fast and smooth UI. I recommned reading [flutter documentation](https://docs.flutter.dev/).
**Make a new flutter project on Android studio (or whatever IDE you use) and add these plugins in your pubspec.yaml file.**

**1. Camera plugin:** This plugin will enable the app to capture images and stream image buffers to dart. We need this plugin to capture plant leaf image and then use our tensorflow model to give results.
Plugin: [link](https://pub.dev/packages/camera)

**2. TensorFlow lite plugin:** Tensorflow is open-source library for machine learning. I will use tensforflow specifically for model training. You can learn more about tensorflow on their [website](https://www.tensorflow.org/learn). 
You can use [teachable machine](https://teachablemachine.withgoogle.com/) to first create a demo machine learning model and then convert it to tensorflow lite so that you can check whether your app is displaying results as intended.
Plugin [link](https://pub.dev/packages/tflite)

**3. Cached Network Images:** The plugin cached network image will load and cache network images. Although it will make the application internet dependent but it will significantly reduce the size which is very important to compete with other apps on the Google playstore. Your download size matters a lot while convincing users to hit that install button. I hosted my images on imgbb.com, the loading times are pretty fast. Best thing about this plugin is that it caches the images once they are loaded. Next times user visits the same page, it feels like image is loaded instantly. I made the decision to use this plugin because I really want to reduce the size the app.
Plugin [link](https://pub.dev/packages/cached_network_image)

**4. Firebase core:** It connects the app with multiple firebase services. I am using this to display articles from the firebase database. In future updates, I will enable authentication so that I can store profile specific user data to add more functionalities in the app. To use this plugin first you have to create a new application in firebase. If you are enabling authentication in the app then you have to enter you SHA key while setting up the app or you can do it after creating the app in the settings section. To get SHA fingerprint from android studio go to this [stackoverflow link](https://stackoverflow.com/questions/27609442/how-to-get-the-sha-1-fingerprint-certificate-in-android-studio-for-debug-mode).
I strongly recommend reading about the basics of firebase and the rules to setup database on their [website](https://cloud.google.com/firestore/docs/client/get-firebase).

**### Front-end thought process:**
I used figma to just get an idea of how my app will look like. I used horizontal Tab bar to switch between categories because it is similar to whatsapp. Majority of the interenet using population have installed whatsapp on their phone so they are familiar with the UI of whatsapp. Even the old people won't be intimidated while navigating through the app. Here is the [link](https://docs.flutter.dev/cookbook/design/tabs) for implementing the tab bar. 
The smooth transition from homepage to a specific plant page is done with [Hero animations](https://docs.flutter.dev/development/ui/animations/hero-animations#:~:text=Flying%20an%20image%20from%20one,as%20a%20shared%20element%20transition.). It looks so cool, I use it for almost every time I have to make change pages with a common asset between them.
To get the photo of the fruits, vegetables and plants, I used [pixabay.com](pixabay.com) and [pexels.com](pexels.com) because they have plenty of high quality images to choose from for free.

I compressed these images. why? 
Even though I am using cached network images to load all these images from web and it is not effecting the app size. But I want to decrease the load time of the photos that's why I compressed these images using [compressnow.com](https://compressnow.com/)

I cropped their background using this online AI tool [photoscissor.com](https://photoscissors.com/). It will look good because we are using Hero animation.

I used same online tools that I have mentioned above to create background image of leaf. I inverted this image horizontally to use it on second tab bar background to make switching between two tab bars feel more natural.




