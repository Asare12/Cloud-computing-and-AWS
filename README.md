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

### AWS
AWS stands for Amazon Web Services. It is a huge set of hardware and services that we can use to build an infrastructure for our app. It's pretty enormous and can do hundreds of things.

We will be using it to create virtual machines that match our dev environment. But these virtual machines will be live to the world. It is definitely not the only service that we could use and you will see many others as well.

Let's get started.

You will have all been set up with an account that allows you to access the Sparta area of AWS. You can log in here:

While the steps for creating a virtual machine on AWS will be different than those for Vagrant the concepts are the same. Try to match them up with what we did in the last lesson.

### Launch an instance
Click on the services tab at the top of the homepage. As you can see AWS has a lot of services that it can offer. The one we want is called EC2 so choose that.

EC2 is Amazon's service for renting hardware and configuring it to your needs. It is very flexible as it allows you to rent hardware for any period of time. We can create and destroy instances as we need them with no penalties. This is why it is incredibly popular.

On the EC2 page click the "Launch Instance" button.

####  Which operating system
The first step is to choose the operating system. On the development environment we are running Ubuntu 14.04 64Bit. This option is close to the bottom of the list of environments.

####  Hardware
The next step is to choose the power of the machine. How many CPUs do we need and how much RAM. We didn't make this choice for our development environment. The more powerful the box the faster it will run. But also the more it will cost.

Choose the t2.micro option as it is more than sufficient for our needs.

#### Make sure you click next and not Launch as this will skip the remaining steps
> NOTE : Power vs Cost is a common trade off for DevOps engineers.
