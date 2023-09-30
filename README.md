# Nutanix Role to manage the Nutanix Files Manager service within Prism Central

This Ansible role manages the Nutanix Files Manager service on Prism Central.

## Role Variables

| Variable                                          | Required | Default | Choices                   | Comments                                                                                               |
|---------------------------------------------------|----------|---------|---------------------------|--------------------------------------------------------------------------------------------------------|
| role_nutanix_pc_svc_files_mgr_host                | yes      |         |                           | The IP address or FQDN for the Prism Central where you want to enable the service.                     |
| role_nutanix_pc_svc_files_mgr_host_username            | no       | "admin" |                           | A valid username with appropriate rights to access the Nutanix API.                                    |
| role_nutanix_pc_svc_files_mgr_host_password            | yes      |         |                           | A valid password for the supplied username.                                                            |
| role_nutanix_pc_svc_files_mgr_host_port                | no       | 9440    |                           | The Prism TCP port                                                                                     |
| role_nutanix_pc_svc_files_mgr_host_validate_certs      | no       | false   | true / false              | Whether to check if Prism UI certificates are valid.                                                   |
| role_nutanix_pc_svc_files_mgr_debug               | no       | false   | true / false              | Whether to output variable contents for debugging purposes.                                            |
| role_nutanix_pc_svc_files_mgr_enable              | yes      |         | true / false              | Set  to 'true' to enable Nutanix Files Manager.                                                        |

## Dependencies

- grdavies.role_nutanix_prism_api
- grdavies.role_nutanix_prism_monitor_task

## Example Playbook

```YAML
- hosts: localhost
  gather_facts: false
  roles:
    - role: grdavies.role_nutanix_pc_svc_files_mgr
  vars:
    role_nutanix_pc_svc_files_mgr_host: 10.38.179.39
    role_nutanix_pc_svc_files_mgr_host_username: admin
    role_nutanix_pc_svc_files_mgr_host_password: nx2Tech283!
    role_nutanix_pc_svc_files_mgr_enable: true
```

## License

See LICENSE.md

## Author Information

Ross Davies
