# PIRE Playbooks
This is a collection of playbooks for maintaining PIRE project.

## Control Docker Container

Execute a build script `build_control_docker` to build control docker container. The command below will create a docker container image `pire_control`.

```bash
./build_control_docker
```

Then execute a run script `run_control_docker` to run the control container. This command will also copy your `~/.ssh` directory into the image to setup an access to `pire` server. Be careful!

```bash
./run_control_docker
```

Lastly, execute a script `terminal_control_docker` to get into the control container. This command will give you a `bash` terminal. 

```bash
./terminal_control_docker
```

## Run in the Control Docker Container 

Use VPN if you want to access from off-campus.

```bash
openconnect vpn.arizona.edu
```

Run `ansible-playbook` to execute playbooks.

```bash
ansible-playbook -i inventory/pire_webdav webdav/webdav.yml
```