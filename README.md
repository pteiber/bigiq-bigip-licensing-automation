# BIG-IP Licensing with BIG-IQ Automation

This repository contains examples, tips, and ideas for automating BIG-IP licensing with BIG-IQ.

## Environment

The examples in this repository were created in a simple environment consisting of two BIG-IQ CM devices (operating with the License Manager persona) and three BIG-IPs, with all devices having their management interfaces on the same network.

All automation tooling was run from an Ubuntu jump box located on the same network.

## Ansible

### Install the f5_bigip Collection

The following are basic steps. Refer to the [instructions](https://clouddocs.f5.com/products/orchestration/ansible/devel/f5_bigip/install_f5_bigip.html) on F5 CloudDocs for additional information.

To install the f5_bigip collection:

```shell
cd ansible
ansible-galaxy collection install f5networks.f5_bigip
```

### Examples

The examples found under the `ansible` directory demonstrate techniques for licensing
BIG-IP devices through BIG-IQ. Each example contains a README.md file that provides additional details.

| Example | Description |
|---------|-------------|
| basic-license-unlicense | Demonstrates licensing and unlicensing without attempting to protect credentials. |
| multiple-bigip-env | Demonstrates licensing and unlicensing across multiple BIG-IPs with different offerings. |
| hashicorp-vault-integration | Demonstrates retrieving credentials and license keys from a HashiCorp Vault installation. |
