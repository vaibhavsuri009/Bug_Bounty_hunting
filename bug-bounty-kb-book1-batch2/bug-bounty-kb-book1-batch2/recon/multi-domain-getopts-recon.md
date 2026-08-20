# Multi-Domain Recon with getopts

- What it is: Parse command-line options and scan multiple domains in one recon run.
- Where to look: Useful for programs with several in-scope root domains.
- Use `-m` to select a mode before domain arguments:
```bash
./recon.sh -m nmap-only facebook.com fbcdn.net
```
- Parse the option:
```bash
getopts "m:" OPTION
MODE=$OPTARG
```
- Iterate only over remaining domain arguments:
```bash
for i in "${@:$OPTIND:$#}"
do
  DOMAIN=$i
  # run selected scans
 done
```
- False-positive/edge note: `getopts` stops option parsing at non-option arguments; place flags before domains as shown.
- Remediation: Not target-side; validate every supplied domain against the authorized scope before scanning.

## Source: Bug Bounty Bootcamp, Ch. 5
