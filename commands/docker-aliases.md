# Development alias helpers

  

## Docker, docker compose and docker stack commands

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

[[ -f $ALIAS_HELPER_DIR/docker.bashrc ]] && . $ALIAS_HELPER_DIR/docker.bashrc

[[ -f $ALIAS_HELPER_DIR/docker-compose.bashrc ]] && . $ALIAS_HELPER_DIR/docker-compose.bashrc

[[ -f $ALIAS_HELPER_DIR/docker-stack.bashrc ]] && . $ALIAS_HELPER_DIR/docker-stack.bashrc

  

EOF

```

  

## Docker command aliases

| #SN | Command | Descriptions | Usage |
|--------------|-----------|------------|------------|
| 1 | dexec | Run a command in a running container | Usage:  dexec [OPTIONS] CONTAINER COMMAND [ARG...]|
| 2 | di| Return low-level information on Docker objects | Usage:  di [OPTIONS] NAME|ID [NAME|ID...]|
| | | | |

