# commands
Nice-to-have, not-as-nice-to-have-to-remember commands.

### Search code in the git history for "find_me", case insensitive, and print the diff:
```
git log -S find_me -i -p
```

### Search commit messages in the git history for "find_me", case insensitive, and print the diff:
```
git log --grep find_me -i -p
```

### Convert each .js file under the current dir to tabs (only leading spaces are converted) (tested on Cygwin):
```
find . -name "*.js" -exec bash -c 'unexpand -t 4 --first-only "$0" > /tmp/totabbuff && mv /tmp/totabbuff "$0"' {} \;
```

### Fix keyboard led lights getting stuck on ubuntu
sudo kbd_mode -u

### Get the git branch name as a string
$(git rev-parse --abbrev-ref HEAD)

### SSH tunnels
https://unix.stackexchange.com/questions/46235/how-does-reverse-ssh-tunneling-work/118650#118650

#### Forward local port 80 to a remote machine on remote port 8001:
```
sudo ssh me@my-machine.local -L my-machine.local:80:some-remote-machine:8001
```

### Find process owning a port:
```
sudo lsof -i ':80' | grep LISTEN
```
