MISCELLANEOUS
==============

Archiving the project
-----------------------
Use ".zip" will destroy the path name of the .wav under the /gen directory. So, use ".rar" to archive the project. 

It is very easy to have some problems about the encoding for the Latin letters in folder "sound" and that for the songs stored in folder "midi" as there are Chinese characters in their file names.

If there are such encoding problems, it will lead these problems
#. The WinRaR try to overwrite what it has just unzipped
#. The music composer software cannot play the "human audio".

Pakawadee has used the following method to send the project to me.

#. Log in machine"rwcpu2.cse.ust.hk" (not "ras.cse.ust.hk")
#. Sender upload the file to the following folder “/rwproject/kdd-db/share/music”
#. After that, type "chmod 777 <that file>". Both of you must be able to access this file.
#. After the receiver downloads it, the sender just change back to "chmod 770 <that file>".

International Interface
-------------------------

The interface program is *easy* to incorporate with it. 
This is because the interface program only reads a file containing the mapping between English and Chinese for that. However, based on the current program structure, some parts of the UI need to be adjusted the size to support the longer length of the words. So, the interface program only needs to know the "length" of each text before putting it to the appropriate place. 

- English to Chinese translation: Coleman
- English to Spanish translation: Sergio


Sergio Góngora ‘s work
------------------------

Sergio has sent one folder named "final.zip" to Raymond. Inside the folder are four things. However, I do not have such "final.zip".

The following is the message from Serigo.

#. "spanishComplete.db" it is a database that I created and I think can be useful. It has  the word, phonetic, mode, phonology, word divided into syllables, and tone of all the words.

#. "syllPho.db" it is a database with all the single syllables in spanish and the phonetic of each syllable.

#. "uiWordList_v2.xlsx" it has the instructions in spanish and german. One german friend checked the german part and he did some corrections so I think its complete correct.

#. "SpanishSeparator.zip" it is a Java programm that can split any spanish word into syllables.


