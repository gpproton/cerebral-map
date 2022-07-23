## General unix system command aliases

Add alias to preffered terminal
```bash
alias_helper_dir="~/.bashrc.d"
cat >> ~/.bashrc << EOF
## Docker, docker compose and docker stack commands
[[ -f $alias_helper_dir/system.bashrc ]] && . $alias_helper_dir/system.bashrc
EOF
```

|      #SN     |  Command  | Description |    Usage   |
|--------------|-----------|-------------|------------|
| 1 | | | |
