---
layout: post
title:  "Ssh -  GIThub"
date:   2019-01-13 23:05:36 +0530
categories: Projects production
---

![ssh](https://media.giphy.com/media/65NO1TrKrJUT6/giphy.gif)



### After you've checked for existing SSH keys, you can generate a new SSH key to use for authentication, then add it to the ssh-agent.

Open Terminal.

Paste the text below, substituting in your GitHub email address.
> $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

This creates a new ssh key, using the provided email as a label.
>  Generating public/private rsa key pair.

When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

> Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]

At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".

> Enter passphrase (empty for no passphrase): [Type a passphrase]

> Enter same passphrase again: [Type passphrase again]


# Adding your SSH key to the ssh-agent

Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key.

Start the ssh-agent in the background.

> $ eval "$(ssh-agent -s)"
> Agent pid 59566


Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.

> $ ssh-add ~/.ssh/id_rsa