[linuxserverurl]: https://linuxserver.io
[forumurl]: https://forum.linuxserver.io
[ircurl]: https://www.linuxserver.io/irc/
[podcasturl]: https://www.linuxserver.io/podcast/

[![linuxserver.io](https://raw.githubusercontent.com/linuxserver/docker-templates/master/linuxserver.io/img/linuxserver_medium.png)][linuxserverurl]

## LinuxServer.io LibreELEC extended repo

This is the x86/arm/aarch64 combined repo containing docker wrapper addons that did not make it into the LibreELEC repo.

Grab the repository.linuxserver.docker.ext.zip file, install from zip in libreelec and you can install the addons from the repo list in the gui.

The main LinuxServer repo can be installed within LibreELEC from the LE repository.

---

If after installing an add-on it doesn't work on reboot, you can check the error messages with `journalctl -xeu docker.linuxserver.radarr.service`. If there was a problem pulling the corresponding docker image due to the device platform, you can force a specific platform by manually editing the `/bin/docker.linuxserver.radarr` file and adding on the `docker run` command the `--platform linux/arm64`.
