# How to install

Import the unsup Prismlauncher component into an empty instance on version `1.12.2` with forge installed (unsup can change the forge version, so dont worry about getting the correct version)
<details>
<summary>How to install a custom component</summary>
<br>
Create an empty component with the UID of <code>com.unascribed.unsup</code> with the following contents:
<pre><code>
{
  "formatVersion": 1,
  "name": "unsup",
  "uid": "com.unascribed.unsup",
  "version": "1.1.2",
  "+agents": [
    {
      "name": "com.unascribed:unsup:1.1.2",
      "url": "https://repo.sleeping.town"
    }
  ]
}
</code></pre>
You can save this component file for later by copying it from <code>&lt;INST_DIR&gt;/patches</code> to the central mods folder, then you can just click import component and select the component json.
</details>

Create a file in the `minecraft` directory called `unsup.ini` with the following contents:

```
version=1
source_format=packwiz
source=https://raw.githubusercontent.com/p1x3l101-10/im-thauming-so-hard-rn/refs/heads/main/pack.toml
server_authority=true
public_key=signify RWRBgYcfobPE7I7STPLaQnp69F06aqQaBSWk0AuUFKlUoCyE6VUZKxJv
```

<details>
<summary>What the file does</summary>
<br>
<code>version</code> is required in all unsup config files to set the compatibility level
<br>
<code>source_format</code> specifies what type of pack unsup needs to download
<br>
<code>source</code> tells unsup where the packwiz pack is located at
<br>
<code>server_authority</code> tells unsup to download the remote <code>unsup.ini</code> file and then use that for the rest of the run
<br>
<code>public_key</code> is there for security purposes, if the signature is bad, unsup will refuse to install the pack. This prevents installing a broken version on accident, and it will also ensure that you can trust that this pack comes from me (if you get malware without using <code>public_key</code>, it's not my fault because that version of the pack probably isn't from me)
</details>