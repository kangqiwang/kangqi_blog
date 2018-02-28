---
title: Android_bActive
date: 2018-02-20 19:16:57
tags:
---
bActive--APP
============
I did project as volunteer in Cardiff Univerisity.

## Frist Step
I look at assessing the options – (i) modify code (ii) re-write code to get bActive to work on Nougat and Oreo Android phones, and write a short report on the options. 

## Backgroud

With the development of sensors, smartphones are an ideal tool for monitoring and promoting physical exercise (Harries Tim, 2016). Smartphones are becoming the sensor hubs in a way, opening a rich experience for users. There are multiple different types of sensors which are built in android, such as motion sensors, position sensors and environment sensors (Google, 2018). 


There are different ways to calculate the number of steps taken by the user. The first method is based on accelerometer using the Pythagorean theorem to calculate the magnitude of the acceleration vector of each sample. In this way, a service has to keep the device awake for calculating the steps (Martin Mladenov, 2009 ). In other words, the program can prevent the device from going into sleep during a lifetime of your service. But this approach will drain the battery fast. Another different way is built-in step counter and step detector sensor, which internally uses an accelerometer, but Android still treats them as logically separate sensors. Meanwhile, sensors are high battery optimized and consume very low power (Nagpa, 2016). Its high accuracy has been verified.


The report will discuss how to change the existing code from accelerometer to built-in step.   Now, there are two different choices. Firstly, the outdated code can be refactored from accelerometer to built-in step counter. Another choice, the existing code can be abolished, the new app will be rewritten. 

## Methodology

In the report, the existing code has been accessed by three aspects. Firstly, the function of the application need be accessed properly. Secondly, the structure of application should be reasonable. Lastly, readable code is important as well such as enough comments.


The author read the existing code and document, meanwhile, the writer will learn and consider the prospective method and structure to decide whether the outdated is useful.

## Results
 
In comparison with the existing application, the main idea is similar. Both of them separate the views, the main algorithms, and services. But I would like to build a module for the Pedometer module and provide an interface, which is easier to test and maintain it.


For the functional aspect, the existing code is more comprehensive than I thought. But I reckon the combination of built-in step counter and accelerometer. In other words, the existing code can add codes for selecting suitable methods based on the edition of Android. It will make app suitable for most Android edition. It is easy to say that we keep the existing arithmetic and add the step counter API, the new application should be suitable for most Android edition. A number of functions are one of the advantages of outdated version, which consider the most functions in research. 

According to Harries and Eslambolchilar (2016), the implemented functions have been listed below:

1. There is no requirement for additional equipment such as pedometers and no need for data entry.
2.    The application counts steps continually and automatically.
3.    the application was disabled until the start of the trail when it was remotely enabled

In contrast with the function in the source code, it is just the tip of the iceberg. The elder version considered about researching the effect of physical activity, in which the participants were divided into three groups: a control, an individual feedback groups and a social feedback groups. The application has considered about groping.

For the version of the application and supported package, the elder edition was developed in 2012, and the MinSdkVersion was 7. The author didn’t write down the targetSdkVersion and MaxSdkVersion in AndroidManifest.xml. But it was compiled by the Android 10 in the project.properties file, which is based on Android Gingerbread (Google, 2018).  The number of packages in latest edition is about two times more than the existing edition.

The other reasons for modifying the code:

1.    The existing code has a number of useful functions such as debug logger and traffic logger, and some of the files of utility class could be useful for approaching development such as DateUtil.class.
2.    Re-writing usually takes longer time than we expected, and there is no need to code some repetitive functions.
3.    the existing UI design makes application become a mature product, and program structure is clear and understandable.
4.    To be honest, I did not have any working experience in Android.

However, some drawbacks provide information about reasons for rewriting existing code. Firstly, the most important problem is that application crashing issue has not been solved. In fact, the application has a crash problem and I am trying to solve it based on application crash report. Furthermore, the kernel of the algorithm has to rewrite, ActivityMonitor.java. Even worse, it has not been provided with the effective interface. Alternatively, our workloads would be bigger than we thought. In addition, the number of the newest package in Android Oreo is twice as many as the target version.

## Conclusion

In my point of view, the refactoring code is a more suitable choice in this situation due to the mentioned reason. Refactoring is the preferred way to incrementally improve the application. It is slow paced to improve the quality of the application. Rewrite has its advantages, but it is a riskier option due to lack of working experience in Android.

In addition, the application can keep the original algorithm and add another method to measure steps, it will make application suitable for most of the edition. However, a number of other functional changes can also increase the workload. 

In conclusion, the crashing problem should be resolvable easily, which may be caused by deployment. Because it has been used to collect data for research. Based on readable code and reasonable program structure, the existing source code need be refactored for updating the version and changing the kernel of arithmetic.
