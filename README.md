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

Tip 1: SSH keys: it took me a while to figure out how to set up the SSH key, but the I came across the procedure and followed it. 

Tip 2: sh files:

Tip 3: Secrets: 
