# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:
```
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{       //variable to store calling function's process id
        pid_t process_id;
        //variable to store parent function's process id
        pid_t p_process_id;
        //getpid() - will return process id of calling function
        process_id = getpid();
        //getppid() - will return process id of parent function
        p_process_id = getppid();
        //printing the process ids
        printf("The process id: %d\n",process_id);
        printf("The process id of parent function: %d\n",p_process_id);
        return 0; }
```

## OUTPUT


<img width="452" height="97" alt="437701817-8e0d2dcf-c2d7-4364-9436-dd521d222b32" src="https://github.com/user-attachments/assets/6cd7bb2c-0d9b-4efb-9b87-412b757bb64f" />




## Program 
```
#include <stdio.h>
#include<stdlib.h>
int main()
{ int pid; 
pid=fork(); 
if(pid == 0) 
{ printf("Iam child my pid is %d\n",getpid()); 
printf("My parent pid is:%d\n",getppid()); 
exit(0); } 
else{ 
printf("I am parent, my pid is %d\n",getpid()); 
sleep(100); 
exit(0);} 
}
```


## OUTPUT


<img width="456" height="100" alt="437702324-2bdf69bf-a63e-47d6-9b82-f1c5077bd193" src="https://github.com/user-attachments/assets/0b00683b-28a4-4c55-b482-3188bf58c00b" />


## program

```
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
int main()
{
	printf("Running ps with execlp\n");
	execlp("ps", "ps", "ax", NULL);
	printf("Done.\n");
	exit(0);
}
```

## output 


<img width="542" height="226" alt="437702702-150b81fc-e098-4cc8-91ed-105ab7aebddb" src="https://github.com/user-attachments/assets/108f52e5-57c1-42c1-94e9-22ec688f5849" />



# RESULT:
The programs are executed successfully.
