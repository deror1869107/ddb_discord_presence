# Discord RP plugin for DeaDBeeF 
Discord Rich Presence Plugin shows your current playing track on your Discord status.

![image](https://user-images.githubusercontent.com/6359901/37570313-94e681fa-2aee-11e8-8b65-cd786c999a0f.png)

## Download
You can find my local builds on https://github.com/kuba160/ddb_discord_presence/releases

Another alternative is to download it from http://deadbeef.sourceforge.net/plugins.html (0.7 branch)

## Configuration
Plugin connects with Discord through Discord Rich Presence API, no further authentication is needed.
You can configure displayed information through plugin settings:

![image](https://user-images.githubusercontent.com/6359901/37570322-c8a79236-2aee-11e8-875f-ba317ded6b25.png)

For more information about title formatting please visit [https://github.com/DeaDBeeF-Player/deadbeef/wiki/Title-formatting-2.0](https://github.com/DeaDBeeF-Player/deadbeef/wiki/Title-formatting-2.0)


## Compile
To compile discord_presence plugin simply do `make` and `sudo make install`. For debug build, compile with `make DEBUG=1`.

#### More information
This plugin uses `libdiscord-rpc` library. By running `make` it will automatically download discord-rpc library through submodule and it will be patched so the library is reallocable (`-fPIC`).
It will build`libdiscord-rpc` library and then move static library file (`libdiscord-rpc.a`) into the main directory. Plugin will be linked with this file.

To compile without building `libdiscord-rpc` run `make discord_presence`.



