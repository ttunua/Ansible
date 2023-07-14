# Ansible

Proof of concept: Running ansible playbooks against Tailscale hosts using github actions.

Uses [action-ansible-playbook](https://github.com/dawidd6/action-ansible-playbook) and [Tailscale github action](https://github.com/tailscale/github-action)

workflows/main.yml 

- workflow that connects to Tailscale and runs ansible. This reusable workflow is extended by run_playbook and scheduled

workflows/run_playbook.yml

- workflow that runs an ansible playbook as a specified user against a host taking these three variables as parameters

workflows/scheduled.yml

- workflow that runs a set ansible playbook as a specified user against a set of hosts on a cron schedule


# Setup

- [Create](https://login.tailscale.com/admin/settings/keys) reusable ephemeral auth key and store it as a github secret
- Change the device names, playbooks etc
