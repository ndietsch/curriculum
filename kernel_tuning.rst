Kernel tuning
*************

Note: This version of the page only discusses Linux and Solaris. Other authors may choose to add other operating systems later on. 

Kernel tuning is used to modify the behaviour of your operating system’s kernel. This can be done for many reasons, such as changing behaviour of certain low level functions, such as say shared memory allocation or for enabling certain features such as IP forwarding. 

The means of setting kernel variables changes between Operating Systems

* Linux for example uses settings which are set dynamically using the sysctl(1m) command or setting them persistently using the /etc/sysctl.conf file or files within /etc/sysctl.d. The means of setting these are discussed in the various manual pages or online documentation for each distribution.

* Solaris and its derivatives set kernel variables using the mdb(1m) command dynamically, although many of these are now accessible using the Solaris projects interface. The settings are set persistently in /etc/system or /etc/projects. 

The authors of various operating systems have put a lot of thought into the defaults used for each operating system. While these defaults are well thought out, they may not match your specific requirements. This is where operating system tuning comes into play. 

Note: Changing your operating system’s kernel settings can have dramatic impacts on your system and should be tested thoroughly before implementing. Changing kernel variables can result in degraded performance or worse, an unbootable system. :

Kernel tunable should only be modified if you have a full understanding of what a setting does, why it is being changed and the impact that may have. A good place to start is the kernel documentation for Linux https://www.kernel.org/doc/Documentation/ and the Kernel Tunables guide for Solaris http://docs.oracle.com/cd/E19253-01/817-0404/