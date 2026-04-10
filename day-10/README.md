# Day 10 - User Management in Linux

## Objective

To deepen my understanding of Linux user management by exploring user types, group structures, system files, and administrative commands used to manage users securely.

---

## What I Learned

### User Management Overview
- User management is essential for system security, access control, and auditing.
- nLinux is a multi-user system, allowing multiple users to operate simultaneously with controlled access.

### Types of Users

- Root User (Superuser): Full system control (UID 0)
- Regular User: Limited access for daily operations
- Sudo User: Regular user with temporary administrative privileges
- System/Service Accounts: Used by services (e.g., databases, web servers)
- Guest User: Temporary access with minimal privileges

**User Groups**
A group is a collection of users with shared permissions.
Primary Group
Automatically assigned when a user is created
Files created by the user inherit this group
Secondary Groups
Provide additional access permissions
Used for collaboration and system-level access

### Key User Management Files
- /etc/passwd → Stores user account details
- /etc/shadow → Stores encrypted passwords and security policies
- /etc/group → Stores group information
- /etc/gshadow → Secure group details
- /etc/sudoers → Controls sudo privileges
- /etc/skel/ → Default configuration files for new users
- /var/log/auth.log → Authentication logs and user activity

### User Management Commands
-  List all users
awk -F':' '{print $1}' /etc/passwd

- Get User ID
id username

- Add a User
useradd username geeks

- Assign a Password
passwd username geeks

- Accessing a User Configuration File
cat /etc/passwd

### Modify User Information
- Change User ID
usermod  -u new_id username

- Change Group ID
usermod -g  new_group_id username

- Change Login Name
usermod -l new_login_name old_login_name

- Change Home Directory
usermod -d new_home_directory_path username

- Delete a User
userdel -r username

---

## Challenges Faced

- Due to lack of superuser (sudo) privileges, I was unable to:
    - Create users (useradd)
    - Modify users (usermod)
    - Delete users (userdel)
    - Assign or reset passwords (passwd)
- Access to sensitive files like /etc/shadow was restricted.
- Practice was limited to read-only exploration, not execution of administrative commands.
- 

---

## Key Takeaways

- User management is central to Linux system security and governance.
- Groups simplify permission management across multiple users.
- Critical system files (/etc/passwd, /etc/shadow) underpin user authentication and access.
- Administrative privileges are required for most user management operations.
- Understanding user management is essential for DevOps, cloud engineering, and system administration roles.
- 

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/user-management-in-linux/

---