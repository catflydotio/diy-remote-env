Before deciding exactly what kind of remote instance I want, I'm going to take a slight detour into one of the considerations. If our remote machine is open to the Internet, we need some way to keep the riffraff out.

### SSH or WireGuard

I can _not_ open it to the Internet, and forward some ports over SSH to get to it. Or I can use a WireGuard tunnel. Either way, I need some more software on both the host and the client. But this gives me more flexibility about the kinds of things we can run, straightforwardly, on the remote machine. I can use VS Code Server, and/or tmux or various terminal panes of whatever flavour connected to the remote environment that way.

### HTTPS

In-browser IDEs are a thing now. If I can serve my IDE as a web app over an https connection (with a Let's Encrypt certificate and a TLS-terminating proxy), and put a password in front of it, I don't need to set up SSH or WireGuard on my local machine to use it. I can connect with an iPad. code-server has password protection of its own, but we could disable that and add authentication with Caddy or nginx.

Whatever you think of being trapped inside a browser window, it's a thing you can do. As it happens, we're not entirely stuck in the browser if we're deployed on Fly.io. More on that later.