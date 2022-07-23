Add alias to preffered terminal
```bash
export ALIAS_HELPER_DIR=~/.bashrc.d/
cat >> ~/.bashrc << EOF
## Docker, docker compose and docker stack commands
[[ -f $ALIAS_HELPER_DIR/system.bashrc ]] && . $ALIAS_HELPER_DIR/system.bashrc
EOF
```
