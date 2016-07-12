Connection
============================================
There are two types of way to push a local repository to the remote repository. They are HTTP and SSH.
	
HTTP
----------------------------------
I prefer the HTTP connection. You may find that when you use the HTTP connection, the system will ask you to input ac/pw every time. It definitely wastes your time. You can use something called "Git Credential Manager for Windows" to remember the ac/pw. Check the reference.

References
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
介紹好用工具：Git Credential Manager for Windows (記憶 Git 常用密碼)
http://blog.miniasp.com/post/2016/02/01/Useful-tool-Git-Credential-Manager-for-Windows.aspx


SSH
----------------------------------
If you use SSH to connect to the remote repository, you need to set up the private and public key pairs first. 
	
I cannot set up the SSH connection properly.  The tortoiseGit cannot find the ssh.exe in Git\bin when pushing the local repository to the remote server. 

Hence, I just forget the SSH connection and always use the HTTP connection.

References
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- 設定SSH連接
https://backlogtool.com/git-guide/tw/reference/ssh.html

- TortoiseGit使用SSH Key和GitLab建立連線 
http://floatfrog.blogspot.hk/2015/06/tortoisegitssh-keygitlab.html

- [Tip] Windows使用ssh對Github進行操作
https://dotblogs.com.tw/kirkchen/2013/04/23/use_ssh_to_interact_with_github_in_windows

