---
layout: post
title: "What I Learn From Xamarin Party Event"
description: "A story that I want to share after attending Xamarin Party in Bandung"
tags: [Android, Xamarin, C#]
comments: true
image:
  feature: xamarin-party.jpg
  credit: Dicoding
  creditlink: https://limaapril.wordpress.com/2016/12/21/bandung-developer-day-5/
---

### Bandung Developer Day #5
Bandung developer day is an event for developers in Bandung. The purpose of this event is to share new knowledge for developers. In 20 Desember 2016, Fifth event of Bandung developer day was held. the topic is `Introduction to Xamarin`. <!-- more --> The speakers are Puja Pramudya and Albilaga from Radya Labs. There are 2 sessions, first session is Puja's stage to introducing Xamarin to the attendees and second session is workshop session delivered by Albilaga. We were creating CRM apps for workshop session.

### What is Xamarin
Xamarin is a set of tools for cross-platform development (Android, iOS, Windows) and the development language is C#.

### Xamarin Classic Vs Xamarin Forms
There is 2 types of Xamarin, Xamarin Classic and Xamarin Forms. The differents are 

* `Xamarin Classic`
  Using C# as logic languange but Xamarin Classic uses the platform specific language for the interface. Android is using XML, iOS is using story board, and Windows is using XAML.
  <center>
    <figure>
      <a href="{{ site.url }}/images/xamarin-classic-figure.png"><img src="{{ site.url }}/images/xamarin-classic-figure.png" alt=""></a>
    </figure>
  </center>

  When you should use Xamarin Classic ?
  
  * You will build apps that has many platform API specific
  * Custom UI is number one

* `Xamarin Forms`
  Using C# as logic languange and using XAML for the interface. Xamarin Forms already has pretty much widget supported.
  <center>
    <figure>
      <a href="{{ site.url }}/images/xamarin-forms-figure.png"><img src="{{ site.url }}/images/xamarin-forms-figure.png" alt=""></a>
    </figure>
  </center>

  When you should use Xamarin Forms ?

  * You will build apps that has not many platform API specific
  * If you want to code once (C# and XAML), run everywhere

### PCL Vs Shared Project
There are 2 types of Xamarin project styles. The main different of this two is

* Shared Project
  You will see a lot of `if` when you want to do platform specific code.

  ```c#
  #if __ANDROID__ 
  path = "android";
  #else 

  #if __IOS__ 
  path = "iOS"; 
  #endif 
  ```

* PCL
  If you want to do platform specific code, you can't do something like `#if __ANDROID__`. You can create an interface to solve this and the implement it in each platform projects.

### Some Useful Links
I'm doing some research after this event and found some useful links, here they are

* <a href="http://university.xamarin.com" target="_blank">http://university.xamarin.com</a>
* <a href="http://www.slideshare.net/Xamarin" target="_blank">http://www.slideshare.net/Xamarin</a>
* <a href="https://programming.albilaga.id/kenalan-dengan-xamarin-aeb3bccbd689#.rqijajjd1" target="_blank">https://programming.albilaga.id/kenalan-dengan-xamarin-aeb3bccbd689#.rqijajjd1</a>
* <a href="https://programming.albilaga.id/kenalan-dengan-xamarin-part-2-1dbb35d3a51a#.arccl5fqk" target="_blank">https://programming.albilaga.id/kenalan-dengan-xamarin-part-2-1dbb35d3a51a#.arccl5fqk</a>
* <a href="https://www.dicoding.com/events/326" target="_blank">Bonus : Documentation of this event</a>


