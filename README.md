# Create Ubuntu 20.04 template for VMware vSphere with Packer

## Build

```
$ cp variables.json.tmpl variables.json
$ vim variables.json
$ packer build -var-file variables.json ubuntu-20.04.json 
```

## Troubleshooting

### 'Build vsphere-iso errored after 1 minute 29 seconds: unable to find an IP'

Check http/user-data for incorrect interface name.
