# Littlechat

To start your Phoenix server:

  * Install dependencies with `mix deps.get`
    * You may have trouble installing `stun` due to OpenSSL. If so, you'll want to set your headers in your environment. [Try this GitHub issue comment for a fix.](https://github.com/processone/ejabberd/issues/1107#issuecomment-217828211)
  * Create and migrate your database with `mix ecto.setup`
  * Install Node.js dependencies with `npm install` inside the `assets` directory
  * Start Phoenix endpoint with `mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

### Building a Release

To build a release using distillery, run the `bin/release` script.

Deploys on Gigalixir are not supported because it is not possible to open a port other than 80 or 443 on Gigalixir - so it's not possible to run the STUN server.

The main thing you'll want to watch out for in deployments is that most browsers require HTTPS for WebRTC unless you're at localhost, so make sure you're using HTTPS.

If you'd rather deploy on your own box, you'll just need to adjust some of the values in `prod.exs` accordingly and you'll be on your way.

## Resources

* https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/Connectivity
* https://www.pkc.io/blog/untangling-the-webrtc-flow/
* https://www.html5rocks.com/en/tutorials/webrtc/infrastructure/
