# EfficientIP SOLIDserver Provider

This provider allows to easily interact with SOLIDserver's REST API.
It allows managing all IPAM objects through CRUD operations.

This provider is compatible with SOLIDserver version 6.0.0 and higher.

# Install
Download the appropriate build for your system from the release page.

Store the binary somewhere on your filesystem such as '/usr/local/bin'.

Then edit the '~/.terraformrc' file of the user running terraform to include the provider's path.

The resulting file should include the following:
```
providers {
    efficientip = "/path/to/terraform-provider-efficientip"
}
```

# Usage
## Using the SOLIDserver provider
SOLIDServer provider supports the following arguments:
* `username` - (Required) Username used to establish the connection. Can be stored in `SOLIDServer_USERNAME` environment variable.
* `password` - (Required) Password associated with the username. Can be stored in `SOLIDServer_PASSWORD` environment variable.
* `host` - (Required) IP Address of the SOLIDServer REST API endpoint. Can be stored in `SOLIDServer_HOST` environment variable.
* `space` - (Required) IP Space into which provionning the resources. Can be stored in `SOLIDServer_SPACE` environment variable.
* `sslverify` - (Optionnal) Enable/Disable ssl certificate check. Can be stored in `SOLIDServer_SSLVERIFY` environment variable.

```
# Add a record to the domain
provider "solidserver" {
    username = "ipmadmin"
    password = "default"
    host  = "192.168.0.1"
    space = "local"
    sslverify = "false"
}
```

## Available Resources
### IP Address
### IP Subnet
### A Record
### CNAME Record

