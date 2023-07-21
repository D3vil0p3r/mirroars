# Mirroars - Get the fastest mirrors from all mirrorlists!

## Dependencies
Install the following dependencies:
```
sudo pacman -S parallel
```

## Usage
```
As rankmirrors, it ranks pacman mirrors by their connection and opening speed and update the related files. Pacman mirror files
are located in /etc/pacman.d/. It can also rank one mirror if the URL is provided.

Usage: mirroars [options] <mirrorfile | url>

Options:
  -n <num>              number of servers to output, 0 for all
  -m, --max-time <num>  specify a ranking operation timeout, can be decimal
                        number
  -p, --parallel        run tests in parallel for all servers (may be
                        inaccurate, depends on GNU parallel)
  -r, --repo            specify a repository name instead of guessing
  -t, --times           only output mirrors and their response times
  -u, --url             test a specific URL
  -v, --verbose         be verbose in output
  -w, --update          update mirrorlist file sorted by faster mirrors
  -h, --help            display this help message and exit
  -V, --version         display version information and exit

Examples:
sudo mirroars -n 21 -m 15 -p -t -w -r blackarch /etc/pacman.d/blackarch-mirrorlist
sudo mirroars -n 21 -m 15 -p -t -w -r chaotic-aur /etc/pacman.d/chaotic-mirrorlist
```
