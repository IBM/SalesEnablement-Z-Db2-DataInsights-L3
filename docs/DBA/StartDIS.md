When instructions are given to type text, the text is usually like below:

```
Sample text to enter.
```

This is to help indicate that you need to type or copy/paste all of the text. Notice the **Copy to clipboard** button (![](_attachments/copyToClipboard.png)). Use it to copy the text and then use your system's paste option (++cmd+v++ or ++ctrl+v++) to enter the text.

Follow the directions below to start the SQL Data Insights service.

- Open the **Putty terminal**, by double clicking on the proper desktop icon **(A)**.

    ![](_attachments/desktop.jpg) ![](_attachments/puttyIcon.jpg)

- CLick on **wg31_large** in the Saved Session table **(A)**, and then click **Load** **(B)**. Click **Open** **(C)** to open a ssh terminal session to the z/OS host: **wg31**.

    ![](_attachments/puttySession.jpg)

- Login with user **(A)**:
  
    ```
    IBMUSER
    ```
    and password **(B)**:

    ```
    SYS1
    ```

    ![](_attachments/puttyLogin.jpg)

<div class="annotate" markdown>
- Switch user to **AIDBADM** (1) using the **su** command **(A)**:

     ```
     su - adibadm
     ```

     and enter the password **(B)**:

     ```
     AIDBADM
     ```

     ![](_attachments/suCMD.jpg)
</div>
1.  **AIDBADM** is the instance owner of the SQL Data Insights instance.

- Stat the SQL Data Insights instance using the command below **(A)**:
     
    ```
    sqldi.sh start
    ```

    ![](_attachments/sqldiStart.jpg)

    The SQL Data Insights Services runs under Unix System Services (USS), which is why you have started it from the USS command line. It can easily be wrapped in a JCL member and run as a started task with system automation.
