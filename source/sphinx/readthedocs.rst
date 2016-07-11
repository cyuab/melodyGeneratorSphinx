Read The Docs
============================================
Once we have installed Sphinx in the local machine, we can compile the source code to html by the Sphinx in the local machine. 
Upload the whole website to the remote server

It does the job but it is troublesome. We need to upload the whole website every time!
	
A more convenient way is as follows.
	
#. Commit the sphinx project to git in local machine.
#. Push the local repository to the remote repository.
#. Done!.

It sounds amazing, right? At least it sounds awesome and amazing to me.
In other to do it, you need to do some setting between the git and the readTheDocs, which is a documentation hosting module.
	

Webhooks
----------------------------------
	You need to create a webhook in the git. Once you push to the git and the content of the documentation has been changed, the webhook is triggered. It will send a signal to the readTheDocs to rebuild the documentation website

References
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. `Webhooks <http://read-the-docs.readthedocs.io/en/latest/webhooks.html>`_.
