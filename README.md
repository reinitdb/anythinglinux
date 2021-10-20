# anythinglinux

## Pyenv issue

Upon installing pyenv on a newly installed Ubuntu OS (20.04.3 LTS (Focal Fossa) on my old dell xps laptop, I was unable to run the python version (i.e. 3,9,7) I installed with pyenv. After setting this version, running "python" would initiate the default python version that came with the OS i.e. 3.8.10.

andrei@t2-xps:~$ pyenv versions
  system
* 3.9.7 (set by /home/andrei/.pyenv/version)
andrei@t2-xps:~$ 

andrei@t2-xps:~$ python
Python 3.8.10 (default, Sep 28 2021, 16:10:42) 
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 

In order to fix, I had to update the PATH variable, to include /.pyenv/shims in my .bashrc file.

export PATH="$HOME/.pyenv/shims:$HOME/.pyenv/bin:$PATH"
