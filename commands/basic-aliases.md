Add alias to preffered terminal
```bash
export ALIAS_HELPER_DIR=~/.bashrc.d/
cat >> ~/.bashrc << EOF
## Docker, docker compose and docker stack commands
[[ -f $ALIAS_HELPER_DIR/general.bashrc ]] && . $ALIAS_HELPER_DIR/general.bashrc
EOF
```
