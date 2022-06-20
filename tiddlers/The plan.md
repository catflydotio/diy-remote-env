I'm going to set up a remote development environment running code-server as a web app on Fly.io.

My Docker image will hold a clean-slate (but mostly-configured) development environment. A persistent disk will keep my working files, and any changes I make to the environment on-the-fly.

I'm going to use the new Fly Machines feature to run my VM. For individual use, I don't need load-balancing, or lots of instances, or always-on. I need one VM, close by for latency, and for cost-effectiveness, I want to shut it down when I'm not using it (because I don't get charged for CPU or RAM if my Fly Machine is stopped).

I can manually start and stop my machine using flyctl, but I'm going run the code-server process behind a small proxy that shuts down if it doesn't get any http requests for some time.

A note: I'm using the flyctl a lot here. It's more of a secret than it should be, but flyctl uses `fly` as an alias for `flyctl`. So if I type `fly secrets` and the docs are for `flyctl secrets`, that's all that is.