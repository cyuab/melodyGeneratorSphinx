How to use Sphinx in Window environment.
============================================

Install Sphinx to Window
----------------------------------
First you need to install python to your PC. I use python 2.7.
You may also need to step up the environment variables in the Window so you can call the python directly in the Window command line (cmd).

After it, you need to install "Sphinx" through the python.

If you want to build a whole new Sphinx website, you can simply use the command.

	sphinx-quickstart

When you build a new Sphinx website, you need to input some setting such as 

- Root path for the documentation
	
- Separate source and build directories
	
- Name prefix for templates and static dir ...
	
I  simply follows the instruction from the 1st reference website.

References
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. `写最好的文档：Sphinx + Read the Docs <http://avnpc.com/pages/writing-best-documentation-by-sphinx-github-readthedocs>`_.


Tools used in Window
----------------------------------
I use notepad++ to edit the .rst files. In other to use notepad++ to edit .rst files smoothly and happily, I suggest you to install the syntax highlighting for rst and allow text wrapping. Read the references.

Beside, you will need to use the cmd to access your sphinx project and then type "make html" to build the website. You may need to build a "short cut" to specific folder location.

References
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. `reStructuredText tool support <http://stackoverflow.com/questions/2746692/restructuredtext-tool-support>`_.

#. `Turn On/Off Word Wrap in Notepad++ <http://dineshkarur.blogspot.hk/2011/03/turn-onoff-word-wrap-in-notepad.html>`_.

- Command Prompt - How to use the simple, basic commands
http://www.digitalcitizen.life/command-prompt-how-use-basic-commands

- Windows: Create Command Prompt That Opens To Specific Folder Location
http://www.technipages.com/handy-command-prompt-shortcut

