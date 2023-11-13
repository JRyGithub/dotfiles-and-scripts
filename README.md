# dotfiles

## Setup

I run ubuntu version `22.04.01` in WSL. As I have tested against this release I suggest you use the same version.

```shell
lsb_release -a
```

output:

```shell
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 22.04.1 LTS
Release:        22.04
Codename:       jammy
```

If you are on an older version I recommend upgrading. This can by done by the following:

- `sudo apt update && sudo apt upgrade -y`
- `do-release-upgrade -d`

1.  Ensure your system is up-to-date via `sudo apt update`

    > To customize your setup with values you want, for example your own git credentials you first need to create a `values.yaml` file using the command below

    ```shell
    cd $HOME && mkdir -p .config/dotfiles && vim .config/dotfiles/values.yaml
    ```

2.  There are two required values you must set. These are
    `git_user_email` and `git_user_name` they can be setup like the following:

    values.yaml

    ```
    ---
    git_user_email: test@email.com
    git_user_name: JohnDoe
    ```

## Install

> Run the following command in your WSL terminal

```shell
bash -c "$(curl -fsSL https://raw.githubusercontent.com/JRyGithub/dotfiles-and-scripts/main/bin/dotfiles)"
```

Then close your terminal and re-open it. :)

## Updating

To synchronize your environment with the main branch you can run `dotfiles` from your shell.
