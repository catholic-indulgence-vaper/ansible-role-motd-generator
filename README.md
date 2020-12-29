# ansible-role-motd-generator
Ansible role to generate pretty MOTD message in ANSI font.

# Use
Add to your Ansible Galaxy requirements file:
```
- src: git@github.com:catholic-indulgence-vaper/ansible-role-motd-generator.git
  name: motd-generator
  version: master
  scm: git
```

# Install
```
ansible-galaxy install -r requirements.yml --force
```

# Customize
Provide `motd_generator_message` variable to each your host/host group:
```
---
all:
  hosts:
    example.com:
      motd_generator_message: Shabbat
```

# Enjoy
Enjoy the results:
```
# cat /etc/motd
███████╗██╗  ██╗ █████╗ ██████╗ ██████╗  █████╗ ████████╗
██╔════╝██║  ██║██╔══██╗██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝
███████╗███████║███████║██████╔╝██████╔╝███████║   ██║
╚════██║██╔══██║██╔══██║██╔══██╗██╔══██╗██╔══██║   ██║
███████║██║  ██║██║  ██║██████╔╝██████╔╝██║  ██║   ██║
╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝ ╚═════╝ ╚═╝  ╚═╝   ╚═╝
```

# Supported chars
Dictionary `motd_generator_dictionary` keeps all known chars:
* a-z;
* 0-9;
* Whitespace;
* Other chars:
```
- / , . ! ? < >
```
