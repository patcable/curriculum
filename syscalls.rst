Syscalls
********

System calls are requests for the operating system's 
:ref:`kernel <kernel-101>` to do a thing.

The kernel has exclusive control over
interfacing with hardware. It has that exclusive control because otherwise
applications could interface with hardware at an extremely low level -
behind the kernel's back. This would allow for applications to create all
kinds of havoc, and not to mention it'd be confusing. Consider, if you were
writing an application, how many low-level things you'd need to write to do
anything?

When an application needs to interface with hardware - when it needs to 
read a file, or allocate memory, or talk with a particular device, some
form of system call is issued. The kernel is asked to work on behalf of an
application, performs the work, then returns the information to the
application.

How will this help me?
======================
As an operations professional or system administrator you will often times
execute programs that you don't have the source code to. Sometimes, these
programs or applications will have bugs - and as an added bonus they may
not report why a particular action failed. Using ``strace`` is a way to 
look into what actions an application is performing at a low level, and
debug what might be going wrong.

Common system calls
===================

``fork()`` and ``exec()``
-------------------------
``fork()`` creates a child process of the current running process that
calls it. Many applications will fork child processes to perform actions
in a seperate process.

``exec()`` replaces a running process with a new one. 


``open()`` and ``close()``
--------------------------

``create()``, ``unlink()`` and ``stat()``
-----------------------------------------

``bind()`` and ``accept()``
---------------------------

``ioctl()``
-----------

Using strace
============
