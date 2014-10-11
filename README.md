User management
=========

This role manages user accounts and groups on a server.

Role Variables
--------------

user_management_users:
A dictionary of users that would typically be set in group_vars/all.
each entry is keyed by user name and has the following properties:

real_name: The real name field for the account.
public_key: Name of the public key file in the asset directory for the user.
additional_public_key: A second public key for the user.
old_public_key: A public key previously in use by this user, to be removed.

user_management_active_users: A list of user accounts that should be active on
the server.
user_management_removed_users: A list of user accounts that should be removed.
user_management_active_admins: A list of admin users.
user_management_locked_users: List of user accounts that should be locked.
user_management_admin_groups: A string of groups that every admin user should be
added to.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: hosts
           hosts_additional_hosts:
               - address: 192.168.0.1
                 hostnames:
                     - server.example.com
                     - server

License
-------

MIT/Simplified BSD license

Author Information
------------------
Role created by Antti J. Salminen in 2014.
