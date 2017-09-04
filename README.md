# commands
Nice-to-have, not-as-nice-to-write commands.

### Convert each .js file under the current dir to tabs (only leading spaces are converted) (tested on Cygwin):
```
find . -name "*.js" -exec bash -c 'unexpand -t 4 --first-only "$0" > /tmp/totabbuff && mv /tmp/totabbuff "$0"' {} \;
```
