# Variuos unix alias helpers

### Docker, compose and swarm commands

Copy to newly created directory

```bash
mkdir -p ~/.bashrc.d/ && \
rm -rf ~/.bashrc.d/*.bashrc && \
cp -r ./alias/*.bashrc ~/.bashrc.d/

```

Add alias to preffered terminal
```bash
export ALIAS_HELPER_DIR=~/.bashrc.d/
cat >> ~/.bashrc << EOF
## Docker, docker compose and docker stack commands
[[ -f $ALIAS_HELPER_DIR/general.bashrc ]] && . $ALIAS_HELPER_DIR/general.bashrc
[[ -f $ALIAS_HELPER_DIR/system.bashrc ]] && . $ALIAS_HELPER_DIR/system.bashrc
[[ -f $ALIAS_HELPER_DIR/docker-shared.bashrc ]] && . $ALIAS_HELPER_DIR/docker-shared.bashrc
[[ -f $ALIAS_HELPER_DIR/docker.bashrc ]] && . $ALIAS_HELPER_DIR/docker.bashrc
[[ -f $ALIAS_HELPER_DIR/docker-compose.bashrc ]] && . $ALIAS_HELPER_DIR/docker-compose.bashrc
[[ -f $ALIAS_HELPER_DIR/docker-stack.bashrc ]] && . $ALIAS_HELPER_DIR/docker-stack.bashrc
EOF
```

## Docker command aliases

|      #SN     |  Command  |Descriptions|    Usage   |
|--------------|-----------|------------|------------|
| 1 | dexec | Run a command in a running container | Usage:  dexec [OPTIONS] CONTAINER COMMAND [ARG...]|
| 2 | di| Return low-level information on Docker objects | Usage:  di [OPTIONS] NAME|ID [NAME|ID...]|
| 3 | dim | List docker images | Usage:  dim [OPTIONS] [REPOSITORY[:TAG]] |
| 4 | dip | Get's IP addresses of all named running containers | Usage:  dip |
| 5 | dl | Fetch the logs of a container | Usage:  dl [OPTIONS] CONTAINER |
