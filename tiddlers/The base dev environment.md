However we set it up, we'll want to stash a copy of our clean configured environment somewhere for safe keeping and easy restores, in case we manage to get mired in dependency hell, or our SSD goes fizzle, or something. 

This could be a disk image or an OS restore point; a Docker image or (what? nix?)

It's kind of a pain to nuke any kind of machine and start over, so we don't want to have to that we don't need to change often; conversely, we want to capture as much as practical of the environment stuff we want to be there if we have to wipe the slate clean.

Let's stash our clean-slate environment in a Docker image for safe keeping. This is convenient for deployment on Fly.io!