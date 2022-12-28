---
published: true
layout: post
date: 2020-8-10
---
# In this article, I will share the tools that I have used to build the plant disease identification app (available on Google playstore) and steps right from the start to its deployement.

After making an new project on Android studio (or whatever IDE you use), get these plugins in your pubspec.yaml file.

1. Camera plugin: This plugin will enable the app to capture images and stream image buffers to dart. We need this plugin to capture plant leaf image and then use our tensorflow model to give results.
Plugin: [link](https://pub.dev/packages/camera)

2. TensorFlow lite plugin: Tensorflow is open-source library for machine learning. I will use tensforflow specifically for model training. You can learn more about tensorflow on their [website](https://www.tensorflow.org/learn). 
You can use [teachable machine](https://teachablemachine.withgoogle.com/) to first create a demo machine learning model and then convert it to tensorflow lite so that you can check whether your app is displaying results as intended.
Plugin [link](https://pub.dev/packages/tflite)


