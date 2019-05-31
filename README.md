# ferm_firewall

Installs `ferm` and configures it by cloning a git repository containing the config.


## Requirements

- `apt`-based distribution with `ferm` and `rsync` in its repositories
- `git` and `rsync` have to be available on the machine executing this role.


## Role Variables

| Variable                            | Default/Mandatory  | Description                                                                                                                                |
|-------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `global_cache_dir`                  | :heavy_check_mark: | Writable directory on the executing host. By cloning the repo to the local machine, no SSH keys have to be transferred to the target host. |
| `ferm_firewall_repo`                | :heavy_check_mark: | Repository to clone to `/etc/ferm/ansible_config`                                                                                          |
| `ferm_firewall_version`             | `master`           | Remote reversion/branch/tag/... to checkout                                                                                                |
| `ferm_firewall_upstream_submodules` | `True`             | Update the submodules to the latest commit of the submodule branch                                                                         |


## Example

```yml
global_cache_dir: /tmp
ferm_firewall_repo: https://github.com/YourGitHubNick/YourFermConfigRepo.git
ferm_firewall_version: dev_fuu
```


## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).


## Author Information

- [Markus Mroch (Mr. Pi)](https://github.com/Mr-Pi) _markus.mroch@stuvus.uni-stuttgart.de_
- [Michel Weitbrecht (SlothOfAnarchy)](https://github.com/SlothOfAnarchy) _michel.weitbrecht@stuvus.uni-stuttgart.de_
