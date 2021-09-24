Support is always available on our [Discord](https://discord.gg/2TsNFKt).

## Protecting against accidental exposure to the internet
Stash has a built-in protection against accidentally exposing itself publicly outside of your network. If Stash receives a request from the public internet, and you do not have a password enabled, Stash will reject the request and shut down to protect your privacy.

This often happens when you use the port-forwarding feature of your router or install Stash on a publicly accessible server, such as a VPS. When you do this, anybody in the world can access your stash instance, so we enforce a password requirement. If your Stash instance has shutdown due to an insecure configuration, it will not start up again until you tell it that you have fixed the problem. After setting up a firewall, or removing your port forwarding rules, you an edit `.stash/config/config.yml` and set the key `security_tripwire_accessed_from_public_internet` to `false`.

### Alternatives to accessing your Stash

You may use several methods to safely access Stash from outside of your home network. In the most basic, you can enable authentication in Stash, and re-enable port forwarding. You can also use a VPN solution that allows you to securely access your home network, such as [Tailscale](https://tailscale.com), [Zerotier](https://zerotier.com), [Wireguard](https://www.digitalocean.com/community/tutorials/how-to-set-up-wireguard-on-ubuntu-20-04), or others.

### Using an external authentication provider
If you are an advanced user, and have secured your Stash instance behind an authwall provided by a reverse proxy or hosting solution, you may continue to use that. You simply have to edit .stash/config/config.yml and set `dangerous_allow_public_without_auth` to `true`. If you have already tripped the security feature, you will also have to set `security_tripwire_accessed_from_public_internet` to `false` in order to allow Stash to start.