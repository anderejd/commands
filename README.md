# commands
Nice-to-have, not-as-nice-to-have-to-remember commands.

### Convert each .js file under the current dir to tabs (only leading spaces are converted) (tested on Cygwin):
```
find . -name "*.js" -exec bash -c 'unexpand -t 4 --first-only "$0" > /tmp/totabbuff && mv /tmp/totabbuff "$0"' {} \;
```

### Fix keyboard led lights getting stuck on ubuntu
sudo kbd_mode -u

### Get the git branch name as a string
$(git rev-parse --abbrev-ref HEAD)
