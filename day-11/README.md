# Day 11 - Group Management in Linux

## Objective

To understand how groups are used in Linux to manage user access and permissions, and to explore group-related commands within the limits of non-sudo access.

---

## What I Learned

### What is Group Management?

    A group is a collection of users used to simplify permission management.
Instead of assigning permissions to individual users, permissions can be assigned to a group.

### Types of Groups
- Primary Group : Every user has one primary group. Files created by the user automatically inherit this group

- Secondary Groups A user can belong to multiple secondary groups
Used to grant additional permissions (e.g., access to shared resources or tools) 

### Group Management Files
- /etc/group → Stores group information:
    - Group name
    - Group ID (GID)
    - Members of the group

- /etc/gshadow → Stores secure group data:
    - Encrypted group passwords
    - Group administrators

### Group Management Commands
- View Group Membership
groups username
id username

**View Group File**
cat /etc/group

### Administrative Commands (Require sudo)
groupadd groupname
groupdel groupname
usermod -aG groupname username

---

## What I Built / Practiced

Viewing My Current Group Information

whoami

id

groups

### Exploring System Groups
**cat /etc/group**
- Identified:
    - System groups
    -User group memberships
    - Relationship between users and groups

---

## Challenges Faced

- Due to lack of sudo privileges, I was unable to:
    - Create groups (groupadd)
    - Delete groups (groupdel)
    - Add users to groups (usermod -aG)
Practice was limited to viewing and analyzing group configurations.

---

## Key Takeaways

- Groups are essential for scalable permission management in multi-user environments.
- Administrative privileges are required for modifying group configurations.
- Administrative privileges are required for modifying group configurations.
Understanding groups completes the foundation of: 

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/group-management-in-linux/

---

## Output

