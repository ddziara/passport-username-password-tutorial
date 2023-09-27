# Overview

In modern web applications, authentication can be performed in a variety of ways. 
Traditionally, users log in by providing a username and password. Social networks, 
along with the billions of people that have joined them, have made [**single sign-on**](https://en.wikipedia.org/wiki/Single_sign-on) (SSO) 
using [**Facebook**](https://www.facebook.com/) or [**Google**](https://www.google.com/) a popular option. Recent innovations, encompassed by 
[**Web Authentication**](https://en.wikipedia.org/wiki/WebAuthn) (WebAuthn), allow people to log in using fingerprint or facial 
recognition.

Application architectures also impact how authentication is achieved. To support web 
applications as well as native mobile and desktop applications, server-side logic can 
be exposed as an API which is invoked by applications running on a desktop, mobile device, 
or within a browser executing client-side JavaScript. Access to APIs is protected by 
token-based credentials, typically issued via [**OAuth**](https://oauth.net/).

Passport provides a flexible framework which allows an application to make use of any 
of these authentication mechanisms. Passport reduces the complexity of authenticating 
a request to a simple statement:

    app.post('/login/password', passport.authenticate('local'));

Hidden behind that simple statement are three fundamental concepts:

* Middleware
* Strategies
* Sessions