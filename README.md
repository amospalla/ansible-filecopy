# ansible-filecopy
* * *

## Description
Copies a file which has some string to recognize it is being managed by Ansible.

If the file being overwritten does not have the identifier string then it is renamed to file.original_before_ansible.

## Variables

Mandatory:
- _file_src_: file to be copied.
- _file_dest_: remote file path.

Optional:
- _file_owner_: file owner (default: root).
- _file_mode_: "mode perms" (needs quotes, default: "0600").
- _file_enable_: <boolean> (default: True).
- _file_string_identifier_: string used to identify the managed file (default: "^# Ansible managed: ").
