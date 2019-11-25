# CODER (Visual Studio Code)

This is my version of a compose file for Coder which is basically Visual Studio Code in a container that you can access from a web browser.

[Coder on Docker Hub](https://hub.docker.com/r/codercom/code-server)

[Coder on GitHub](https://github.com/cdr/code-server)

## Environment Variables

`${DOCKERDIR}` = Where you store your Docker container data. I use my home folder for my user in a docker subfolder. EX: `/home/ltm/docker`

`${PUID}` = The user ID of the host machines user. You can get this by using the `id` command in the command line. Mine is set to `1000`.

`${PGID}` = Docker group number. You can get this by using the `id` command in the command line. Mine is set to `999`.

`${TZ}` = Your local timezone. Mine is set to `America/New_York`

`- PASSWORD` = Set this variable to what password you would like to access the code server. Highly recommended if you are going to make this accessible outside of your network. If you do not want to use a password, you can either comment out this environment variable as well as change the `--auth=password` portion of the command to `--auth=none`.

## Commands

`--disable-telemetry` = Disables usage statistics.

`--auth=password` = Enables password protection for accessing Coder. Change to `--auth=none` to disable.