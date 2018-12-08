<!--
Before submission,  create a new Droplet and test your article from start to finish on it exactly as written. 
Cut and paste commands from the article into your terminal exactly. 
If you find yourself executing a command that isn't in the article, 
incorporate it into the article to make sure the reader gets the exact same results. 
DO will test the article and send it back if DO runs into technical problems, which significantly slows down the publication process.
-->


# How To Install JupyterHub on Ubuntu 18.04

![Alt text for screen readers](https://imgur.com/HeHb8Jt.png)

### Introduction
<!-- 
Introductory paragraph about the topic that explains what this topic is about and why the reader should care; what problem does it solve?
-->

What is the goal of the tutorial? What will the reader accomplish if they follow it?

In this guide, you learn how to will deploy JupyterHub using Python 3 on an Ubuntu 18.04 server. [JupyterHub](https://jupyterhub.readthedocs.io/en/latest/) hosts [Jupyter Notebooks](https://jupyter-notebook.readthedocs.io/en/latest/) on a virtual server. Typically, Jupyter Notebooks are run locally, but JupyterHub allows you run Jupyter Notebooks in the cloud.

<!-- 
What software is involved, and what does each component do (briefly)?
-->

In this tutorial, you will use an Ubuntu 18.04 server, Python 3, JupyterHub, Jupyter Notebooks, Nginx and certbot. The Ubuntu 18.04 server will run the instance of JupyterHub. JupyterHub itself will create Jupyter Notebook servers for each user that logs in. Jupyter Notebooks are what JupyterHub servers. In the Jupyter Notebooks you can run Python 3 code. Nginx will be used as a reverse proxy to field incomming connections and forward them on to Jupyter Hub. Certbot will be used to create SSL credentials so you can run JupyterHub using https. 

Running JupyterHub in the cloud is benefiticial because it means that your developer team, research group, or class do not need to install Python locally run Python code. In addition, Python code is usually run on Windows, MacOS or Linux. When you run JupyterHub on the server you can run Python code with a Chromebook, a tablet and even a phone. If you want a team to be able to run Python code, without installing any software continue reading. You can deploy JupyterHub as part of a class or training.

When you're finished with this tutorial, you'll be able to log into your JupyterHub server and run Python code in Jupyter Notebooks hosted in the cloud.

## Prerequisites

<!-- Prerequisites are important. Learn more at https://do.co/style#prerequisites -->

Before you begin this guide you'll need the following:

- One Ubuntu 18.04 server set up by following the [Initial Server Setup with Ubuntu 18.04 tutorial](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04
- A non-root user with sudo privileges (<insert link to Initial Server Setup article for the OS used in this tutorial>) explains how to set this up.)
- A fully qualified domain name (FQDN) with an A record pointing your domain to your server's IPv4 address. You can purchase a FQDN on Namecheap or get one for free on Freenom, and you can follow this [hostname tutorial](#) for details on how to set up DNS records.
- The following DNS records set up for your server. You can follow this [hostname tutorial](#) for details on how to add them.
    - An A record with your server name (e.g. ipa.example.com) pointing to your server's IPv4 address.
    - An AAAA record with your server name pointing to your server's IPv6 address, if you want your server reachable via IPv6.
- A GitHub account with a username and password. If you don't have a GitHub account sign up for one at [github.com/join](https://github.com/join).

## Step 1 — Install Miniconda

First, we are going to install [Miniconda](#) on the server. Miniconda is a minimal distribution of Python released by Ananconda. It comes with Python and the conda package manager. Browse the releases at [https://repo.continuum.io/miniconda/](https://repo.continuum.io/miniconda/). You are looking for the latest release of Miniconda3 for 64-bit Linux. Look for something like:

Miniconda3-latest-Linux-x86.sh

Right-click on the installer file and select [copy link address] the link will have the form:

https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

Log into the server as a non-root sudo user. Navigate to the ```tmp``` directory then use wget to download the installer.

```
$ cd ~/tmp
$ wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh
````

Once the download finishes, you can view the installer file in the ```tmp``` directory.

```
$ ls

Miniconda3-latest-Linux-x86.sh
```

Make the installer file executable, then run the installer script

```
$ chmod g+e Miniconda3-latest-Linux-x86.sh
./Miniconda3-latest-Linux-x86.sh
```


change permissions

Finally run conda --version

<!--
When showing a command, explain the command first by talking about what it does. Then show the command.

If showing a configuration file, try to show only the relevant parts and explain what needs to change.
-->

Now that Miniconda is installed on the server, we will use conda to create a virtual environment and install JupyterHub

## Step 2 — Create a Virtual Environment and Install JupyterHub

In this step we will...

content

Transition to the next step.

## Step 3 — Run and Test JupyterHub

Another introduction

content

Transition to the next step.

## Step 3 — Configure Nginx

Another introduction

content

Transition to the next step.

## Step 3 — SSL security

Another introduction

content

Transition to the next step.

## Step 3 — Run JupyterHub as a System Service

Another introduction

content

Transition to the next step.

## Step 3 — Add GitHub Authentication

Another introduction

content

Transition to the next step.

## Conclusion

In this article you [configured/set up/built/deployed] [something]. Now you can....

<!-- Speak  to reader benefits of this technique or procedure and optionally provide places for further exploration. -->

For futher explanation see: JupyterHub documentation, Littlest JupyterHub deployment, Zero to JupyterHub on Kubernetes.

<!-- Some examples of how to mark up various things

This is _italics_ and this is **bold**.

Only use italics and bold for specific things. Learn more at https://do.co/style#bold-and-italics

This is `inline code`. Use it for referencing package names and commands.

Here's a command someone types in the Terminal:

```command
sudo nano /etc/nginx/sites-available/default
```

Here's a configuration file. The label on the first line lets you clearly state the file that's being shown or modified:

```nginx
[label /etc/nginx/sites-available/default]
server {
    listen 80 default_server;
    listen [::]:80 default_server ipv6only=on;

    root <^>/usr/share/nginx/html<^>;
    index index.html index.htm;

    server_name localhost;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

Here's output from a command:

```
[secondary_label Output]
Could not connect to Redis at 127.0.0.1:6379: Connection refused
```

Learn about formatting commands and terminal output at https://do.co/style#code

Key presses should be written in ALLCAPS with in-line code formatting: `ENTER`.

Use a plus symbol (+) if keys need to be pressed simultaneously: `CTRL+C`.

This is a <^>variable<^>.

This is an `<^>in-line code variable<^>`

Learn more about how to use variables to highlight important items at https://do.co/style#variables

Use `<^>your_server_ip<^>` when referencing the IP of the server.  Use `111.111.111.111` and `222.222.222.222` if you need other IP addresses in examples.

Learn more about host names and domains at https://do.co/style#users-hostnames-and-domains

<$>[note]
**Note:** This is a note.
<$>

<$>[warning]
**Warning:** This is a warning.
<$>

Learn more about notes at https://do.co/style#notes-and-warnings

Screenshots should be in PNG format and hosted on imgur. Embed them in the article using the following format:

![Alt text for screen readers](/path/to/img.png)

Learn more about images at https://do.co/style#images-and-other-assets
-->

