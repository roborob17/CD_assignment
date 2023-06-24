# CD_assignment
Winc Python final assignment CD
![example print workflow](https://github.com/roborob17/CD_assignment/actions/workflows/hello.yml/badge.svg)

Continuous Deployment (CD)

In this assignment I used GitHub Actions to implement a continuous deployment pipeline. As a starting point I have set up a VPS running a Flask application as described in a previous exercise. 

I have used the tips in the assignment to setup continuous deployment. I elaborate on them further down the line.

The continous deployment pipeline should look like this:

1. You manually write, commit and push some code. This only requires you to be familiar with git. --> 
2. GitHub Actions runs tests on your code. You can use Pytest for this. -->
3. If and only if the tests pass, GitHub Actions logs into the VPS you have running with Digital Ocean and runs commands such that the code is updated to the latest version. -->

Tip 1: SSH keys: it took me a while to figure out how to set up the SSH key, but the I came across the procedure and followed it. I couldn't do much at first with it, I saw in the testing that the connection was working, but the tests failed many times. I than searched the Internet and found https://zellwk.com/blog/github-actions-deploy/ which helped a lot, but not all the way, since his live example was removed from Github...Then I found https://medium.com/swlh/how-to-deploy-your-application-to-digital-ocean-using-github-actions-and-save-up-on-ci-cd-costs-74b7315facc2 and finally I got it!

Tip 2: sh files: I have used a .sh file to put together the commands that my github action needed to execute
in the droplet, even if it is not a complex script I believe this was the most easy and clean solution, and it was a tip!

Tip 3: Secrets: weren't to hard to get into Github and use in the actions, since there wasd a lot of info on the web on how to di this, also in the 2 links I mentioned before.

Problems, problems

As already said with Tip 1, getting the SSH keys to work between Github and the remote server was a bit of a hassle, but in the end, with help from the aforementioned websites, I got it...

It finally helped when I got to the use of the .sh file to get the pipeline working from Github to the droplet remote server.

It took a long time getting the syntax right in the .yml files to get no more errors when running with the tests, but finally with a lot of trial and error I got it to work! Especially the specific errors you can see in the Actions itself are very helpful, so you can pinpoint where the problem lies and then go and solve it!
