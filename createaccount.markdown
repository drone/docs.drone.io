---
layout: default
title: Create Account / Sign In
---

This document will explain how to create an account on Drone.io, and how to sign into the system. 

## Creating an Account 

You have two options:

* Use your existing GitHub, Bitbucket or Google account. This option means you will not need to enter a username and password on Drone.io.  Instead Drone.io will ask GitHub, Bitbucket or Google to verify your identity.
* Create a custom Drone.io account. This option means you'll need to enter a username and password each time you sign into Drone.io.
 
Create an account by clicking the "Sign up" button in the upper right and choosing an option.

![Sign-In](img/sign-in.png)

If you choose to use an existing account from GitHub, Google or Bitbucket, then you'll be redirected to their site and asked to authorize Drone.io.  This authorization is used by Drone.io to verify who you are and to help automate setting up projects.

After authorizing, you'll need to confirm your username, display name and email address.

![Register](img/register-new.png)

## Sign-in

If you are signed into Github or Google, then you should be automatically signed into Drone.io.  If not, you'll be redirected to their site and asked to sign-in first.

***

## Details about using Google and Github to sign in

Drone.io leverages login services provided by Google, Github or Bitbucket to verify who you are, and to help automate project setup.

Drone.io never has access to your password.  Whenever you enter your username and password, you are doing it on your provider's servers.

<!--
For this to work, when you first create an account Google or Github will ask you to authorize Drone.io to have access to basic account information.

The very specific permissions and data Drone.io requests are highlighted below.
<table>
<tr>
<td>
Github
</td>
<td>
<ul><li>Read your public information</li>
<li>Update your public and private repositories (Commits, Issues, etc).</li>
</ul>
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
</ul>
</td>
</tr>
</table>
-->

To see more details about the permissions granted to Drone.io, and to modify or delete them, you'll need to go to Github's, Google's, or Bitbucket's account management screen

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
4. You will see a list of all sites you've ever authorized, and their permissions
5. You should see Drone.io in the list.  You can view or modify it's permissions by following the instructions provided by Github on this screen

For Bitbucket:

1. Go to <bitbucket.org> and sign in
2. Click on your user in the upper right, then select "Manage Account"
3. Click on "Integrated Applications"
4. You will see a list of all sites you've ever authorized


