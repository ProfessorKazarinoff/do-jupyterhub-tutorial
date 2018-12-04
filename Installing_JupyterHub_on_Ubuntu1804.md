<!--
Before submission,  create a new Droplet and test your article from start to finish on it exactly as written. 
Cut and paste commands from the article into your terminal exactly. 
If you find yourself executing a command that isn't in the article, 
incorporate it into the article to make sure the reader gets the exact same results. 
DO will test the article and send it back if DO runs into technical problems, which significantly slows down the publication process.
-->


# How To Install JupyterHub on Ubuntu 18.04

![Alt text for screen readers](https://imgur.com/HeHb8Jt)

### Introduction
<!-- 
Introductory paragraph about the topic that explains what this topic is about and why the reader should care; what problem does it solve?
-->

In this guide, you will deploy JupyterHub on an Ubuntu 18.04 server. [JupyterHub](#) hosts [Jupyter Notebooks](#) on a virtual server. JupyterHub allows you run Jupyter Notebooks from anywhere.

When you're finished, you'll be able to log into your JupyterHub server running on Digitial Ocean.

## Prerequisites

<!-- Prerequisites are important. Learn more at https://do.co/style#prerequisites -->

Before you begin this guide you'll need the following:

- 1 Ubuntu18.04 server <!-- Also specify the amount of RAM the server needs if relevant. -->
- A non-root user with sudo privileges (<insert link to Initial Server Setup article for the OS used in this tutorial>) explains how to set this up.)
- (Optional) If software such as Nginx needs to be installed, link to the proper article describing how to install it.
- A GitHub account with a username and password

## Step 1 — Install Miniconda

First we are going to install [Miniconda](#) on the server. Miniconda is a minimal distribution of Python released by Ananconda. 

First wget Miniconda

./ run mini conda

set /opt as installation directory

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

## Step 3 — Title Case

Another introduction

content

Transition to the next step.

## Conclusion

In this article you [configured/set up/built/deployed] [something]. Now you can....

<!-- Speak  to reader benefits of this technique or procedure and optionally provide places for further exploration. -->

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

