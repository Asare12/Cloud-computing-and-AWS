# Cloud-computing-and-AWS
- ## [Intro presentation to cloud computing and AWS](https://docs.google.com/presentation/d/1mCpHtCIQjaBd_lCSvReo3g7xFn86ZkB96lQiQ9dSDeI/edit#slide=id.p)

# Simple Deployment
### Pre-requisites
- set up with an IAM account
In the previous lesson we built an "environment" for the developers to work in by creating virtual machines with all the software they need to build and run their applications.

Now we want people to be able to use it. This is the basic idea of deployment. How can we get our app in to the hands of the people we want using it?

For web applications ( which we'll be building ) this means getting your code on to a server that is publically visible. But there are other types of deployment too.

In our case we aren't ready for a fully Continuously Deployed system yet so we're going to push it to an environment that we'll call "UAT" User acceptance Testing.

This will be a dummy server that is accesible from the web but it won't be public. This server will be used for testing by our imaginary manual testing teams.

You may remember from the development environment lesson that one of the principles ideas was that all the places that the code needs to run should be as close to identical as possible. This was to avoid the dreaded "it works on my machine" error.

So our goal for this lesson is to recreate our development environment on a machine that can be seen from the web. For this we'll be using AWS.
