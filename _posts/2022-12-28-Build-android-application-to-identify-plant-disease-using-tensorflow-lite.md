---
published: true
layout: post
date: 2020-8-10
---
#In this article, I will share the tools that I have used to build the plant disease identification app (available on Google playstore) and steps right from the start to its deployement.

After making an new project on Android studio (or whatever IDE you use), get these plugins in your pubspec.yaml file.
Camera plugin: This plugin will enable the app to capture images and stream image buffers to dart. We need this plugin to capture plant leaf image and then use our tensorflow model give results.
Plugin link: [camera](https://pub.dev/packages/camera)

