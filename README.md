<!-- START BLUEPRINT-MANAGED README -->

> [!IMPORTANT]
> This project is an unofficial project hosted on the [`blueprint-community`](https://github.com/blueprint-community) GitHub organization.
> [Blueprint](https://blueprint.zip) does not create, endorse or maintain these projects.
>
> You are free to contribute, fork and reuse sections of this codebase [in accordance with this projects' license](LICENSE).

<br>

<h2 align="center"> Redirect </h2>
<p align="center"> Create URL redirects on your Pterodactyl panel </p>

<br>

<!-- END BLUEPRINT-MANAGED README -->



### Installation
To install this extension, download the latest release of Redirect and drag the `redirect.blueprint` file over to your Pterodactyl installation folder. Then, run `blueprint -install redirect` to finish the installation process.

If you're using NGINX as your webserver, assuming you followed the Pterodactyl installation instructions, you will also need to modify your config file. Apache and Caddy should work without additional configuration.

#### NGINX Configuration
- Open your NGINX server config file, typically located in `/etc/nginx/sites-available/`
- Within your `server` block that contains the `index` line (the second server block, if you followed the Pterodactyl guide), change `index index.php` to `index index.php index.html`
- Save the file, then test your config with `nginx -t`
- If the test completes without issue, restart NGINX with `sudo systemctl restart nginx`

<br>

### Usage
Within the extension's page, acessible via the puzzle piece on the admin page, you will see a few different panels:
- Redirects: A list of all of your active redirects
- Add Redirect: Used to add a new redirect
  - Name: The link extension that you would like to use as your redirect. E.g. `test` as the name would create a redirect on the URL `yourserver.com/test`
  - Destination: The URL you would like the link to redirect to
- Remove Redirect: used to remove a redirect
  - Name: The name must match **EXACTLY** that of the link you'd like to remove.
 
After adding a redirect, you can visit \<your website URL>/\<redirect name> to be redirected.

For example, with the website `serverhost.net` and a redirect named `myvideo`, you would visit `serverhost.net/myvideo`

<br>

### Removal
To remove Redirect from your Pterodactyl panel, run `blueprint -remove redirect`. This might not remove all of your redirects, so remove them before removing Redirect.

<br>

### Screenshots
![image](https://github.com/prplwtf/blueprint-redirect/assets/103201875/958ea4eb-f954-4e13-a0da-c662891ccce1)

#### Screenshots but marketingcore

![](https://s3.blueprint.zip/extensions/images/9/fpPoDPPT.webp)
![](https://s3.blueprint.zip/extensions/images/9/Ow7hc3SV.webp)
