# desktop-ansible

This is a playbook to setup my personal desktop runing Manjaro i3.

That's about it, there's nothing more to see here ¯\\_(ツ)_/¯


## Running the playbook

First things first, we'll need at least git and ansible installed.
```(bash)
pacman -Sy git ansible
```

Then we'll need to install the requirements.
```(bash)
ansible-galaxy install -r requirements.txt
```

The system playbook will install all tools and configures the system to my likings. Needs root permissions.
```(bash)
ansible-playbook -v system.yml -i hosts --ask-become-pass
```

The "profile" playbook make changes to my own profile files so it does not need any root access.

```(bash)
ansible-playbook -v profile.yml -i hosts
```

