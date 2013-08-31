Website : quickauth.org

# Quick authentification concept

There is the source code of the website in this repo but the concept is explained here:

## Intro

This is an authentification concept initially created for a mobile application (Five Seconds, not available yet).
This concept allows to keep user logic in any kind of application but removes the signing-up and signing-in process for the user. More friendly for the user, simple to integrate and the same "user logic" in your code.

## The problem in the classic auth concept:

The classic auth concept (email/password) is easy to develop and everyone knows how it works but it has many problems: 

- Many people use an unsophisticated password, easy to find or to hack. 

- Not suitable for mobile interfaces and time wasting, the users will remove the app. They will sign up only if they really want to use it. It's easy to loose a user because of this. However, you can't remove it because you need to authenticate your users. 

- It takes to much time as the user must register and then login to use an app.

## The concept:

In this concept, we assume that the base of the digital identity of a person is his e-mail address. A single form is used both for signing-up and logging-in, only asking the user his email address.

If a user enters the app for the first time, he just needs to enter his email and then, he is signed up and logged! 
If the user has already registered before but is logged out, a randomly generated password is sent to him by email to authenticate him. After entering it in the app, he is logged-in again.

In fact, this concept is mainly designed for mobile application but not only. As a user will rarely logout on mobile, we just ask for his email one single time and he is signed up and logged in. 

## Security, same as before:

The most important security breach is the user's email account. If someone hacks his email, the hacker is able to login in your app. But the breach exists in the classical authentification concept with "I forgot my password". Then, it's the same as before. 

- The password sent by email can be used one single time. It's generated when the user wants to login. 
- The password can't (or not easily) be attacked by brute-force because it's sophisticated. 

In fact, I think this system can be used for most of the mobile application but for security reasons, I don't think it's a good idea for application that contains sensitive informations.

## For users, quick and easy:

With this authentification concept, the period between the moment when the user launches the application and the moment when he uses it is really quick. The user can't be discouraged because of the authentification process. In most of the cases, your user will never logout and will never use the email authentification process. Maybe if he wants to use his account on another device. 

So, there is no sign up plus login system. It's the same form for both!

## Technically, easy to develop:

Technically, you can code this concept the same way you would do with a classic auth system, using an API or not. Most importantly, with this you keep a "user logic" in your code. If you want more information about the user, you can ask him later but not during the sign-up process.

## Licence

Concept by William AGAY. With the licence "you are free to use this idea, customize it but please, keep me in touch" !