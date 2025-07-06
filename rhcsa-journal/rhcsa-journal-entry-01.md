#Journal Entry 01 - RHCSA Start + Bash and Terminal Tools

**Date:** 2025-07-05
**Focus:** Starting Rhcsa course, Bash navigation, man pages, virtual terminals, and text editors


---


### What I Did:
- Began the Sander Van Vugt Rhcsa course; reviewed basic CLI usage, terminal controls, and manual pages 
- Practiced terminal shortcuts:
     - `Ctrl + Shift + +` to increase terminal font size
     - `Ctrl + A` to jump to the beginning of a line in bash 
- Explored user login tracking with: 
     ```bash
     who
     sudo chvt 3 
     ```
        - this showed currnt terminal sessions and how to move between virtual terminals (e.g. tty2, tty3) 


---

- Reviewed and practiced man command usuage
    - /,n, G, q, and spacebar navigation
    - man -k user | grep 8 to filter system admin commands 
    - sudo mandb to update man page index 


---


- Refreshed nano and vim text editor shortcuts 
    - practiced opening files, inserting text, and exiting properly 
    - reviewed Vim commands like :wq, dd, yy, gg, G, and :%s/old/new/g


---


- Completed Lab 
    - used man to find password command 
        ```bash 
        man -k password | grep 8
        ```
    - created user anna
        ```bash
        sudo useradd anna
        ```
    - set password for user anna
        ```bash
        sudo passwd anna
        ```
    - used vim to create a file called users and entered names on separate lines 


---

- Reviewed I/O redirection, pipes and standared input/output/error numbering 
