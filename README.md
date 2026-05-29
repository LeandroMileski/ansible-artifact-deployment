# ansible-artifact-deployment

Automates the full deployment lifecycle of a Java Spring Boot application to a remote Ubuntu server — from local build to running process — with a single command.

## Business Value

- **Eliminates manual deployments** — no more SSH sessions, hand-copied files, or forgotten cleanup steps
- **Reduces human error** — process shutdown, artifact replacement, and startup are handled consistently every time
- **Onboards new developers instantly** — any developer can deploy by supplying their name; user provisioning is automatic
- **Audit-friendly** — each deployment runs under a named Linux user, making ownership and accountability clear

## Usage

```bash
ansible-playbook -i inventory/hosts deploy.yml --extra-vars "linux_user=<name>"
```

## Project Structure

```
ansible-artifact-deployment/
├── my-app/             # Java Spring Boot application (Gradle)
├── inventory/hosts     # target server
├── group_vars/all.yml  # shared configuration
└── deploy.yml          # main playbook
```

<img width="1468" height="698" alt="image" src="https://github.com/user-attachments/assets/3e317ed6-c7dc-4029-a060-4f46ea1a6d7b" />
<img width="1464" height="290" alt="image" src="https://github.com/user-attachments/assets/04fc907a-941f-4b81-835a-96f5891af815" />




