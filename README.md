# PIRE Playbooks
This is a collection of playbooks for maintaining PIRE project.

## Control Docker Container

Run `docker build` to build control docker container.

```bash
docker build -f ./control_docker/Dockerfile -t pire_control  .
```

Then run `docker run` to get into the container.
```bash
docker run -ti --privileged pire_control /bin/bash
```

## Run

Use VPN if you want to access from off-campus.
```bash
openconnect vpn.arizona.edu
```

Run `ansible-playbook` to execute playbooks.

```bash
ansible-playbook -i inventory/pire_webdav webdav/webdav.yml
```