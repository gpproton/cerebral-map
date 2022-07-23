## General alias setup

### Pull from files from repository
```bash
git clone https://github.com/gpproton/unix-assist.git
```


### Copy to newly created directory
```bash
cd unix-assist/ && \
mkdir -p ~/.bashrc.d/ && \
rm -rf ~/.bashrc.d/*.bashrc && \
cp -r ./alias/*.bashrc ~/.bashrc.d/
```

### Manually add shell aliases
```bash
## Add alias to preffered terminal
alias_helper_dir="~/.bashrc.d"
cat >>~/.bashrc <<EOF
########## Helper unix alias ############
## General and system command alias
[[ -f $alias_helper_dir/general.bashrc ]] && . $alias_helper_dir/general.bashrc
[[ -f $alias_helper_dir/system.bashrc ]] && . $alias_helper_dir/system.bashrc
## Docker, docker-compose and docker-stack command alias
[[ -f $alias_helper_dir/docker-shared.bashrc ]] && . $alias_helper_dir/docker-shared.bashrc
[[ -f $alias_helper_dir/docker.bashrc ]] && . $alias_helper_dir/docker.bashrc
[[ -f $alias_helper_dir/docker-compose.bashrc ]] && . $alias_helper_dir/docker-compose.bashrc
[[ -f $alias_helper_dir/docker-stack.bashrc ]] && . $alias_helper_dir/docker-stack.bashrc
EOF
```

### Loads all users bash files
```bash
# User specific aliases and functions
if [ -d ~/.bashrc.d ]; then
	for rc in ~/.bashrc.d/*; do
		if [ -f "$rc" ]; then
			. "$rc"
		fi
	done
fi
```

### Add bashrc to shell if not using bash
```bash
# Get the aliases and functions
if [ -f ~/.bashrc ]; then source ~/.bashrc; fi
```