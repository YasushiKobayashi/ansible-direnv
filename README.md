[![Build Status](https://travis-ci.org/YasushiKobayashi/ansible-direnv.svg?branch=master)](https://travis-ci.org/YasushiKobayashi/ansible-direnv)


### install dirnev
C
`ansible-galaxy install YasushiKobayashi.ansible-direnv`

### ansible role initial setting
- cenos6
- amazone-linux

### set bash
```bash
eval "$(direnv hook bash)"
$ echo 'eval "$(direnv hook bash)"' >>  ~/.bash_profile
$ echo 'eval "$(direnv hook bash)"' >>  ~/.bashrc
```

```yml
- name: set direnv bash_profile
  become: false
  lineinfile:
    dest: ~/.bash_profile
    line: 'eval "$(direnv hook bash)"'

- name: set direnv bashrc
  become: false
  lineinfile:
    dest: ~/.bashrc
    line: 'eval "$(direnv hook bash)"'
```
