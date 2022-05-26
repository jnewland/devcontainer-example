# devcontainer-example

The devcontainer configuration in this branch can be used to reproduce an issue with port forwarding after rebuilding an existing GitHub Codespace.

* Create a Codespace using VS Code Desktop from this branch: `docker-compose-port-forward` 
* View the forwarded port labeled `nginx`, observe that you see a default nginx page.
* Codespaces > Rebuild Container
* View the forwarded port labeled `nginx`, observe that the connection is dropped.
* Run `curl localhost:80` in the terminal to confirm that nginx is still running.
* Attempt to change the visibility of the `nginx` port to `public` and interact with it. Observe that after a long timeout you receive a 504 error. Observe that subsequent refreshes display a 502 instead.
