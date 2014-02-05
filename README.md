# Simple sudoers role

This role installs sudo package, ensure that /etc/sudoers.d included and
create or remove sudoers files in /etc/sudoers.d.
For now, each user has full sudo access, and global setting determines whether
NOPASSWD is set or not.

## Variables

 * sudoers_filename - file name in /etc/sudoers.d (required)
 * sudoers - A list of users who have sudo access. Use '%foo' to specify that
   users in a given group have sudo access.
   * defaults: []
 * sudoers_nopasswd - if set, NOPASSWD is added to all sudoers entries. Use this
   when users don't have passwords set.
   * default: true
 * sudoers_remove - if enabled, remove /etc/sudoers.d/{{ sudoers\_filename }} instead
   of create.
   * default: false

## TODO
 * Ability to create users with not full access