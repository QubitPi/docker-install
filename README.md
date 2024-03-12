# docker/docker-install
Home of the script that lives at `get.docker.com` and `test.docker.com`!

The purpose of the install script is for a convenience for quickly
installing the latest Docker-CE releases on the supported linux
distros. It is not recommended to depend on this script for deployment
to production systems. For more thorough instructions for installing
on the supported distros, see the [install
instructions](https://docs.docker.com/engine/install/).

This repository is solely maintained by Docker, Inc.

## Usage:

Install Docker from the source repo (This will install latest from the `stable` channel):

```shell
git clone https://github.com/QubitPi/docker-install.git
cd docker-install
sh install.sh
```

### Executing the Docker Command Without Sudo

By default, the docker command can only be run by the root user or by a user in the docker group, which is automatically
created during Docker's installation process. We cannot run the docker command without prefixing it with "sudo" or 
without being in the docker group. If we want to avoid typing "sudo" whenever we run the docker command, add our 
username to the docker group:

```shell
sudo usermod -aG docker ${USER}
```

To apply the new group membership, log out of the server and back in

## Testing:

To verify that the install script works amongst the supported operating systems run:

```shell
make shellcheck
```

## Legal
*Brought to you courtesy of our legal counsel. For more context,
please see the [NOTICE](NOTICE) document in this repo.*

Use and transfer of Docker may be subject to certain restrictions by the
United States and other governments.

It is your responsibility to ensure that your use and/or transfer does not
violate applicable laws.

For more information, please see https://www.bis.doc.gov

## Reporting security issues

The maintainers take security seriously. If you discover a security issue,
please bring it to their attention right away!

Please **DO NOT** file a public issue, instead send your report privately to
[security@docker.com](mailto:security@docker.com).

Security reports are greatly appreciated and we will publicly thank you for it.
We also like to send gifts—if you're into Docker schwag, make sure to let
us know. We currently do not offer a paid security bounty program, but are not
ruling it out in the future.

## Licensing

docker/docker-install is licensed under the Apache License, Version 2.0.
See [LICENSE](LICENSE) for the full license text.
