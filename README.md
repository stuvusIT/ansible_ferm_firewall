# ferm_firewall

Installs and configures a ferm firewall from any git repository.


## Requirements

A Linux server with `apt` as package manager and ferm, git in his repositories.


## Role Variables

### Primary
| Option                              | Type            | Default  | Description                                                                                                         | Required |
|-------------------------------------|-----------------|----------|---------------------------------------------------------------------------------------------------------------------|:--------:|
| `ferm_firewall_repo`                | string          |          | Repository to use as firewall                                                                                       |     Y    |
| `ferm_firewall_version`             | string          | `master` | Remote reversion/branch/tag/... to checkout                                                                         |     N    |
| `ferm_firewall_ssh_key`             | string          |          | ssh key to clone the repository (ex. Deployment key)                                                                |     N    |
| `ferm_firewall_ignore_hostkey`      | boolean         | `False`  | Accept any host key from remote git server (ensure that "-o StrictHostKeyChecking=no" is present as an ssh options) |     N    |
| `ferm_firewall_accept_hostkeys`     | list of strings | `[]`     | List of host keys to accept from remote git server                                                                  |     N    |
| `ferm_firewall_upstream_submodules` | boolean         | `True`   | Keep the submodules on their remote master                                                                          |     N    |


## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).


## Author Information

 * [Markus Mroch (Mr. Pi)](https://github.com/Mr-Pi) &lt;_markus.mroch@stuvus.uni-stuttgart.de_&gt;
