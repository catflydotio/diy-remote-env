What would I like from a remote development environment? The ability to build and test on the same architecture I'm deploying to. Maybe more cores or more RAM than my local machine has. May as well be able to deploy from there. In a pinch, what about quickly fixing something from a mobile device when I'm away from my computer?

From here on, I'm going to dispense with questions like "why?" I'm assuming we want to set up a remote development environment and think about how we might go about it.

For individual use, you don't need load balancing or lots of instances or always-on. You need one VM, close by for latency, and for cost-effectiveness, exit the process on a provider that will charge you less when you do that
-	on-demand start, stop
-	timeout in case you forget
