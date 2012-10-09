---
layout: default
title: Create Account / Sign In
---

This document will explain how to create an account on Drone.io, and how to sign into the system. 

It assumes:

* You are a new to Drone.io
* You have a Github or Google account

## Creating an Account 

Drone.io lets you sign in using either your Github or Google account.  Just click on "Create Account" button and choose either Github or Google.

![Sign-In](img/sign-in.png)

Github or Google will then ask you to authorize Drone.io to have read-only access to your basic account information.  You must authorize/allow in order to use Drone.io (you can read more about this here).

The final step to create an account is confirming your details and clicking "Register" button.

![Register](img/register.png)

## Sign-in

If you are signed into Github or Google, then you should be automatically signed into Drone.io.  Drone.io never asks you for a username or password.

If you end up at the Drone.io sign in screen, click the Github or Google button, and enter your login information like you normally would for those sites.  Note: You will need to rememeber which account you used when you first joined Drone.io.

When you successfully sign in you should see your project dashboard.

![Register](img/register-success.png)

You have now created an account and signed in!





***

## Details about using Google and Github to sign in

Drone.io leverages login services provided by Google or Github to verify who you are.

Drone.io never has access to your username or password.  Whenever you enter your username and password, you are doing it on Google's or Github's servers.

For this to work, when you first create an account Google or Github will ask you to authorize Drone.io to have access to basic account information.

The very specific permissions and data Drone.io reqeusts are highlighted below.
<table>
<tr>
<td>
Github
</td>
<td>
<ul><li>Read your public information</li></ul>
<td>
</tr>
<tr>
<td>
Google
</td>
<td>
<ul><li>View basic information about your account</li>
<li>View your email address</li>
<li>Perform these operations when I'm not using the application</li>
</td>
</tr>
</table>

To see more details about these permissions, and to modify or delete them, you'll need to go to Github's or Google's account management screen

For Google:

1. Go to <www.google.com>, and sign in
2. Click on your User Name, then Account
3. On the Accounts page, select the Security tab
4. Click the "Edit" button next to "Authorizing applications and sites"
5. You will see a list of all sites you've ever authorized, and their permissions
6. You should see Drone.io in the list.  You can view or modify it's permissions by following the instructions provided by Google on this screen

For Github:

1. Go to <github.com> and sign in
2. Click on the "Account Settings" button, it's in the upper right
3. Click on the Applications tab
5. You will see a list of all sites you've ever authorized, and their permissions
6. You should see Drone.io in the list.  You can view or modify it's permissions by following the instructions provided by Github on this screen
