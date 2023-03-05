# Bash Shell wrapped in SSH-Agent Action

A GitHub action that wraps a bash shell in a `ssh-agent` session with a provided base64 encoded key and optional passphrase.

 ## Usage


```
on: pull_request
name: bash ssh-agent action
jobs:
  mybashystuff:
    name: bash ssh-agent action on pr
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: bash ssh-agent action on pr
      uses: JamesJonesConsulting/github.bash-in-ssh-agent.action.git@main
      with:
        encoded-key: ${{ secrets.someprivatekeyencodedbase64 }}
        run: |
          echo "whatever you need to run inside a ssh-agent... like ansible-playbook perhaps"
```

## To Do

This is a very early but functional iteration.

