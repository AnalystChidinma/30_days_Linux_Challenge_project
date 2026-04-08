# Day 08 - Users In Linux System Admins=istration

## Objective

To understand how user management works in Linux system administration, including user types, account structure, and key commands used to manage users.

---

## What I Learned
- A user in Linux is an entity that can log into and interact with the system.
- Each user is identified by a unique User ID (UID) and associated with a Group ID (GID).

    **Types of Users**:
- Root User (UID 0): Full administrative control over the system
- Regular Users: Limited access for daily operations
- System Users: Used by services (e.g., web servers, databases)

    User information is stored in:
- /etc/passwd → user details (username, UID, home directory, shell)
- /etc/shadow → encrypted passwords and password policies

- When a user is created:
    - A home directory is created (/home/username)
    - A default shell is assigned
    - Default configuration files are copied from /etc/skel

---

## What I Built / Practiced

- Checked current user:
    
    `whoami`

- Viewed user identity details:
    
    `id`

- All the information of users in a system are stored in 
    
    `/etc/passwd`

    I ran this commands:

    `cd /etc/passwd`
---

## Challenges Faced

- Due to lack of superuser (root) privileges, I was unable to:
    - Create new users (useradd, adduser)
    - Modify existing users (usermod)
    - Delete users (userdel)
    - Access or inspect password details (/etc/shadow)

- My access level was limited to read-only operations, restricting hands-on practice for administrative commands.

---

## Key Takeaways

- Linux follows the principle of least privilege, restricting sensitive operations to authorized users only.
- User management commands require elevated privileges because they directly impact system security and access control.
- Even with read-only access, it is possible to:
    - Analyze system users
    - Understand account structures
    - Interpret user-related configurations
- This setup reflects real-world environments where engineers often operate without full administrative access.

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/users-in-linux-system-administration/

---

## Output

![etc/](<cat passwd.PNG>)

![etc/](<etc file.PNG>)

![permission]](image.png)