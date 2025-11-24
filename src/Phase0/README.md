## Install rye & configure environment

First install rye - read what's that
```bash
curl -sSf https://rye.astral.sh/get | bash
```

Then make it visible for your system
```bash
echo 'source "$HOME/.rye/env"' >> ~/.bashrc
source ~/.bashrc
```

Then configure your env
```bash
rye sync
```

Install pre-commit - read what's that
```bash
pre-commit install
```

If you want to commit to your repo run (find what does it do under the hood):
```bash
rye run commit
```

Done
