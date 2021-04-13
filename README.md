[![Build Status](https://drone-ci.hopto.org/api/badges/Diesel-Net/rt-ax88u/status.svg)](https://drone-ci.hopto.org/Diesel-Net/rt-ax88u)

# rt-ax88u
Automation for Asus RT-AX88U Router running Asuswrt-Merlin

# Dependencies
- Asus Router RT-AX88U running Asuswrt-Merlin firmware
- Ansible 2.10+

# Renew TLS Certificates
1. Update certificate data in [certificates.yaml](.ansible/group_vars/all/certificates.yaml)

2. Deploy new certificates
```bash
ansible-playbook .ansible/update_certificate.yaml -i .ansible/inventory/production/hosts --vault-id ~/.tokens/master_id
```
