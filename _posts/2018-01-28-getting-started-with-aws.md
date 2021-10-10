---
layout: post
title:  "Getting Started with AWS"
author: Russell A. Ray
---

Welcome. This is the starting point of my journey. The goal for me is
bringing up a static website on Amazon Web Service
([AWS](https://aws.amazon.com/?nc2=h_lg)). Bringing up a personal
website has been a personal aspiration since I started my career. When I
first took this on, it was very tedious and brittle work using HTML.
Today, the work for spinning up a website has been streamlined with the
advent of of software tools that generate the HTML and styles for you.

Very specialized tools list Jekyll, Jekyll themes, Visual Studio Code, Git, GIMP, and AWS has cut down the effort for developers significantly.

<h6>Environment Setup</h6>

We will need a development environment.  I won't bore you with the details here on what it takes for setting up your environment in this blog post. Below are some basic steps for accomplishing the work.  For those developers who want the details, [here](/docs/setup) is the detail process.

<table>
<tr><th>Step</th> <th>Description</th></tr>
<tr><td>1</td><td> Install Homebrew</td></tr>
<tr><td>2</td><td> Install pip3</td></tr>
<tr><td>3</td><td> Install Python3</td></tr>
<tr><td>4</td><td> Install awscli</td></tr>
<tr><td>5</td><td> Install Ruby</td></tr>
<tr><td>6</td><td> Install Node Package Manager</td></tr>
</table>

<h6>Getting Started</h6>

My first step in creating a website is creating an AWS account.  This is the starting point in my journey. This took me a total of 30 minutes and I had an account. The
[process](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/)
is well documented and easy to follow. I choose the support plan for
developers as I saw this a quick way to solving my challenges as I got started on my project.

<table>
<tr><th>Step</th> <th>Description</th></tr>
<tr><td>1</td><td>Create AWS Access Key/ AWS Secret Key Access Key</td></tr>
<tr><td>2</td><td>Setup local environment keys</td></tr>
</table>


<h6>Creating a Simple Storage Service (S3)</h6>

Next, I looked at the different ways on creating a useful on-line
presence using AWS. While AWS offers an endless amount of capability and
functionality, I focused on steps that built upon the basics. This is
when I targeted a static content and I can control or change occasionally.  One way is storing documents and images on AWS using a S3 service.  This is commonly known as <i>buckets</i> in AWS.  A couple things that you cannot store in the <i>buckets</i> is server side code, such has PHP or ASP.NET.

1. **Create a Separate Domain**
Creating a separate domain for yourself is very cost effective. This was the reason I created my domain using AWS because it was faster than using other services like GoDaddy.com.  Oh, you can use a third party registrar and AWS would support it, but there are additional steps in the configuration so the user is routed to your website on AWS.

2. **Create a Record Set using AWS Route 53**
AWS Route 53 is a cloud Domain Name System(DNS) web service.  It provides a means of routing users from a name (www.mywebsite.net) to an IP address (192.125.6.1) so computers and connect with one another.  When you create a new domain, several record sets are created within AWS Route 53 for you. The first is the Naming Servers. Your new domain is stored in a database around the world so users can find your website.  The second record set is the Start of Authority.  The SOA record provides some information about the base DNS about the new domain.

3. **Creating an Amazon S3 Bucket**
  Using the below aws-cli command creates a bucket. The response returns as a successful bucket creation

   ![](/img/command-create-bucket.png)