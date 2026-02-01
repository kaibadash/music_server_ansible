# Music Server Ansible

An Ansible playbook for MPD + myMPD on Armbian.

## Setup

```bash
# client PC
pipx install --include-deps ansible
brew install sshpass # for Setup SSH
cp hosts.ini.example hosts.ini
vi hosts.ini # edit

# Setup SSH
ansible-playbook -i hosts.ini setup_ssh.yml --ask-pass --ask-become-pass

# Setup music server
ansible-playbook -i hosts.ini setup_music_server.yml --ask-become-pass
```

## Open

https://music.local

## Add music

```
scp ~/Music/Music/Media.localized/Music/YOUR_MUSIC your_name@music.local:/var/lib/mpd/music
```
