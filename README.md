# Packer templates for VMware vSphere

## Build

```
$ cp variables.json.tmpl variables.json
$ vim variables.json
$ packer build -var-file variables.json ubuntu-20.04.json 
```

## Security

### Ubuntu

Default credentials: ubuntu:ubuntu

Change user password in http_ubuntu2004/preseed.cfg :

```
$ mkpasswd -m sha-512
$ vim http_ubuntu2004/user-data
```

### Debian

Default credentials : debian:debian

Change root and user password in http_debian10/preseed.cfg :

```
$ mkpasswd -m sha-512
$ vim http_debian10/preseed.cfg
```

## Troubleshooting

### 'Build vsphere-iso errored after 1 minute 29 seconds: unable to find an IP'

Check http/user-data for incorrect interface name.
