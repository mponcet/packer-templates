# Packer templates for VMware vSphere

## Build

```
$ cp variables.json.tmpl variables.json
$ vim variables.json
$ packer build -var-file variables.json ubuntu-20.04.json 
```

## Security

### Debian

Default password : debian

Consider changing root and user password in http_debian10/preseed.cfg :

```
$ mkpasswd -m sha-512
$ vim http_debian10/preseed.cfg
```

## Troubleshooting

### 'Build vsphere-iso errored after 1 minute 29 seconds: unable to find an IP'

Check http/user-data for incorrect interface name.
