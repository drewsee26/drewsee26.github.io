<!---
---
layout: post
title: Blocipedia
thumbnail-path: "img/blocipedia_thumb.jpg"
short-description: A production quality SaaS app that allows users to create their own wikis. 


---
{:.center}
[![Drew's Blocipedia]({{ site.baseurl }}/img/blocipedia.jpg)](https://drews-blocipedia.herokuapp.com)

## Summary

Wikis are a great way to collaborate on community-sourced content. Blocipedia lets users create their own wikis and share them publicly or privately with other collaborators.

## Explanation

The goal for this project was to create an app for users to generate Wikis.  This was the first large project that I worked on independently, using the Rails framework.  I was required to be the designer, project manager, developer and tester.

## Problem

Blocipedia needed to solve several problems including

* user authentication
* the ability to create, view, update and delete Wikis
* user role updates
* account upgrades associated with payment
* creating private Wikis based upon user role
* instituting markdown syntax for Wiki creation and editing
* adding/removing Collaborators for private Wikis


## Solution

I was able to tackle the user authentication issue by using the Devise gem in conjunction with SendGrid, which allows new users to sign up and send emails for account confirmation.  Once the email is received, they can click a link to confirm their email address and sign in to their account.  Public wikis are generated through CRUD actions associated with the Wikis Controller.  A Wiki belongs to a User through the User model.  Authorization is accomplished by using the Pundit gem, which establishes standard, premium and admin roles.  The premium role can only be obtained through payment, which is an upgrade option on the user’s profile page.  This allows a user to enter their credit card information in a secure fashion, which I incorporated using the Stripe gem.  Once a user is premium, they can create private Wikis or make public Wikis private.  The Redcarpet gem allows for Markdown syntax to be used when creating and editing Wikis.  Finally, Collaborators are established in the WikiPolicy as part of the Pundit gem, via the ApplicationPolicy.

## Results

For each problem, I thoroughly tested each piece I implemented by running through all user case scenarios.  

## Conclusion

This was a challenging project both in length and problem sets.  The use of Ruby gems aided in having to write authentication and authorization features.  I had not previously used the Pundit and Stripe gems so they took a bit longer to understand how they work and then integrating them into the application.  My initial worry was doing this alone without a team and how quickly I could build the application.  However, once I got over some configuration issues with some of the gems, the project went rather quick.  I will definitely use these Ruby gems in the future as they make common tasks much easier.
--->