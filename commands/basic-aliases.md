## General unix command aliases

Add alias to preffered terminal
```bash
alias_helper_dir="~/.bashrc.d"
cat >> ~/.bashrc << EOF
## Docker, docker compose and docker stack commands
[[ -f $alias_helper_dir/general.bashrc ]] && . $alias_helper_dir/general.bashrc
EOF
```

|      #SN     |  Command  | Description |    Usage   |
|--------------|-----------|-------------|------------|
| 1 | | | |
