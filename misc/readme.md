### What is the difference between RBAC and DAC/ACL?

RBAC (Role based access control) is based on defining a list of business roles, and adding each user in the system to one or more roles. Permissions and privileges are then granted to each role, and users receive them via their membership in the role (pretty much equivalent to a group). Applications will typically test the user for membership in a specific role, and grant or deny access based on that.
Discretionary Access Control (DAC) allows a user or administrator to define an Access Control List (ACL) on a specific resource (e.g. file, registry key, database table, OS object, etc), this List will contain entries (ACE) that define each user that has access to the resource, and what her privileges are for that resouce. 

