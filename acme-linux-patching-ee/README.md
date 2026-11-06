# acme-linux-patching-ee

Linux system patching and compliance EE

## What's included

### Ansible collections

| Collection | Version | Source |
|---|---|---|
| redhat.rhel_system_roles | - | Private Automation Hub (rh-certified) |
| ansible.posix | - | Private Automation Hub (rh-certified) |
| redhat.insights | - | Private Automation Hub (rh-certified) |



## Details

- **Tags:** `execution-environment`

- **Image registry:** `52.21.70.135/acme-linux-patching-ee:v1.0.0`

## Use this execution environment

If your EE uses collections from private sources (Automation Hub, private automation hub), update the token settings in `ansible.cfg` before building.


Log in to the registry and pull the image:

```bash
podman login 52.21.70.135
podman pull 52.21.70.135/acme-linux-patching-ee:v1.0.0
```

If the registry uses a self-signed certificate, you may need to append `--tls-verify=false` to each `podman` command.

To use it in Ansible Automation Platform:

1. Go to **Automation Execution** > **Infrastructure** > **Execution Environments**.
2. Click **Create execution environment** and enter the image URL: `52.21.70.135/acme-linux-patching-ee:v1.0.0`
3. Select this execution environment in your job templates.

## Build details

- **Base image:** `registry.redhat.io/ansible-automation-platform/ee-minimal-rhel9:2.18`
- **Definition file:** `acme-linux-patching-ee.yml`
- **Template file:** `acme-linux-patching-ee-template.yml` - import this into Ansible automation portal to let others create EEs from the same starting point.

To make changes, use this EE's template in Ansible automation portal or rebuild manually with `ansible-builder` and the definition file.
