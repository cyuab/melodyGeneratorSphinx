Read The Docs
==============
Recall that the documenting environment used for this project consists of three components.

#. Sphinx: Used to generate document website from source code (rst).
#. Git: GitHub or GitLab. Used to store/keep the source code of the document website.
#. ReadTheDocs: Import the source code from Git and generate the document website. 

I guess ReadTheDocs is constructed by Django.

- https://carolhsu.gitbooks.io/django-girls-tutorial-traditional-chiness/content/django/README.html

In my opinion, I think this set of tools is the best environment of writing document.  
I will explain why this set of tools is the best.

Naive method #1
---------------

Normally, using Sphinx is enough for writing a beautiful document. Once we have installed Sphinx (and of course Python) in our machine, we can compile the source code (rst) to generate a document website by the Sphinx in our machine.

Then, we can simply upload the whole website to the server by SSH. 

However, there are several drawbacks. We need to upload the whole website to the server every time when we have updated the source code and compiled a updated website. It wastes of times.

Naive method #2
---------------
We can upload the rst directly to the server by SSH. And then compile the rst by the Sphinx compiler installed in the server. Then the website document is updated.
However, there are several drawbacks too. We need to upload the modified rst files one by one to the server. Or we upload all the source codes to the server. But it is wastes of times too.

Our method
-----------

You can simply ignore Naive method #1 and Naive method #2. They are useless for us.
You just need to focus on this method.

#. Edit the rst files in the sphinx project in the local machine.	
#. Commit the sphinx project to git in local machine.
#. Push the local repository to the remote repository.
#. Done!.

After you have pushed the project to the remote repository, 
Git will tell ReadTheDocs that there are updates. 
Then ReadTheDocs will visit Git to check that whether the updates affect the content of the document website. If it does, it will rebuild the website.
If this is the first time to import Git into ReadTheDocs, ReadTheDocs will build the document website according to the source code.

Hence, we do not need to commit the folder "build" in the sphinx project to the Git. A ".gitignore" file is written and placed inside the folder "build" to ignore all the files under the folder "build".

It sounds amazing, right? At least it sounds awesome and amazing to me.
In other to do it, you need to do some setting between the git and the readTheDocs. The setting is called "webhook".

First, I will introduce how to install readTheDocs to the server. You do not need to worry about that. Coleman has installed it. The following session is just for Coleman to record how he installed readTheDocs to the server.
	
Install "readthedocs"
---------------------------
I follow the instruction from these websites.

- http://stackoverflow.com/questions/19892310/hosting-a-read-the-docs-like-server-in-house
	
- http://read-the-docs.readthedocs.io/en/latest/install.html
	
There are some typos in the second link. So, please take the first link as reference.

Note that you need to replace the following commands in the above websites to the followings,

- "pip" replaced by "/usr/local/bin/pip2"
	
- "python" replaced by "/usr/local/bin/python2"
	
Besides, the website said you need to install "virtualenv" by "pip virtualenv". 

Study "virtualenv" from below.

- http://tech.mozilla.com.tw/posts/2155/python-%E9%96%8B%E7%99%BC%E5%A5%BD%E5%B9%AB%E6%89%8B-virtualenv

- http://blog.gasolin.idv.tw/2010/02/virtualenv.html
	
You need to install it by "/usr/local/bin/pip2 install virtualenv --user". Supplying the "--user" flag.

In addition, we cannot activate the "rtd" created by "virtualenv rtd" using this command "source bin/activate".
It is because "activate" is written in written in Bourne-shell format, and currently our default shell is t(csh). You can't expect that tcsh would understand script written in Bourne-shell.
We should use the corresponding file "activate.csh" under bin.

The above guideline is told by Dominic from CS system.

The following websites suggest that we should create the "rtd" folder under "/opt/readthedocs".
In other words, we should create folder "readthedocs" under "/opt/".

- https://github.com/rtfd/readthedocs.org/issues/609
	
- http://linux-wiki.cn/wiki/zh-tw/Linux%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84



Webhooks
-----------
You need to create a webhook in the git. 
Once you push the project to the remote repository and the content of the documentation has been changed, the webhook is triggered. It will send a signal to the readTheDocs to rebuild the documentation website.


References
^^^^^^^^^^^^
#. `Webhooks <http://read-the-docs.readthedocs.io/en/latest/webhooks.html>`_.
