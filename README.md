# How to install

Import the unsup Prismlauncher component into an empty instance
<details>
<summary>How to install a custom component</summary>
<br>
Create an empty component with the UID of `com.unascribed.unsup` with the following contents:
```
{
  "formatVersion": 1,
  "name": "unsup",
  "uid": "com.unascribed.unsup",
  "version": "1.1-pre9",
  "+agents": [
    {
      "name": "com.unascribed:unsup:1.1-pre9",
      "url": "https://repo.sleeping.town"
    }
  ]
}
```
You can save this component file for later by copying it from `<INST_DIR>/patches` to the central mods folder, then you can just click import component and select the component json.
</details>

Create a file in the `minecraft` directory called `unsup.ini` with the following contents:
```
version=1
source_format=packwiz
source=https://cdn.piplup.pp.ua/packs/im-thauming-so-hard-rn/pack.toml
server_authority=true
public_key=signify RWRBgYcfobPE7I7STPLaQnp69F06aqQaBSWk0AuUFKlUoCyE6VUZKxJv
```

<details>
<summary>What the file does</summary>
<br>
`version` is required in all unsup config files to set the compatibility level
`source_format` specifies what type of pack unsup needs to download
`source` tells unsup where the packwiz pack is located at
`server_authority` tells unsup to download the remote `unsup.ini` file and then use that for the rest of the run
`public_key` is there for security purposes, if the signature is bad, unsup will refuse to install the pack. This prevents installing a broken version on accident, and it will also ensure that you can trust that this pack comes from me (if you get malware without using `public_key`, it's not my fault because that version of the pack probably isn't from me)
</details>