# Ansible

Proof of concept: Running ansible playbooks against Tailscale hosts using github actions.

Uses [action-ansible-playbook](https://github.com/dawidd6/action-ansible-playbook) and [Taislcale github action](https://github.com/tailscale/github-action)

workflows/ansible.yml 

- workflow that connects to Tailscale and runs ansible. This reusable workflow is extended by run_playbook and scheduled

workflows/run_playbook.yml

- workflow that runs an ansible playbook as a specified user against a host taking these three variables as parameters

workflows/scheduled.yml

- workflow that runs a set ansible playbook as a specified user against a host on a cron schedule
