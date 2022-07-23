## Docker, compose and swarm commands

Add alias to preffered terminal
```bash
alias_helper_dir="~/.bashrc.d"
cat >> ~/.bashrc << EOF
## Docker, docker compose and docker stack commands
[[ -f $alias_helper_dir/docker-shared.bashrc ]] && . $alias_helper_dir/docker-shared.bashrc
[[ -f $alias_helper_dir/docker.bashrc ]] && . $alias_helper_dir/docker.bashrc
[[ -f $alias_helper_dir/docker-compose.bashrc ]] && . $alias_helper_dir/docker-compose.bashrc
[[ -f $alias_helper_dir/docker-stack.bashrc ]] && . $alias_helper_dir/docker-stack.bashrc
EOF
```

## Docker command aliases

|      #SN     |  Command  | Description |    Usage   |
|--------------|-----------|-------------|------------|
| 1 | dexec | Run a command in a running container | Usage:  dexec [OPTIONS] CONTAINER COMMAND [ARG...]|
| 2 | di| Return low-level information on Docker objects | Usage:  di [OPTIONS] NAME|ID [NAME|ID...]|
| 3 | dim | List docker images | Usage:  dim [OPTIONS] [REPOSITORY[:TAG]] |
| 4 | dip | Get's IP addresses of all named running containers | Usage:  dip |
| 5 | dl | Fetch the logs of a container | Usage:  dl [OPTIONS] CONTAINER |
