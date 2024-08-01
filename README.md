# Hosting Services
A one stop shop for hosting my applications on a VPS.

General idea is to bundle a bunch of utilities together and leverage docker to allow for DevOps and workflows to be setup near instantly.

## Nginx
This repository is the home to my VPS's nginx configuration managed through docker. Dockerization is used here to allow for no down time deployment with nginx being able to talk directly to the containers not having to juggle IPs on the machine.

currently hosting:
- pass.tmanti.dev (https://github.com/tmanti/Passmanager)
- tmanti.dev (currently placeholder html)

## services.tmanti.dev
This subdomain will be the api responsable for receiving all push event webhook payloads and triggering the CI/CD processes for no down time deployment.

To achieve no downtime deployment and consistent CI/CD processes I will be leveraging docker compose container scaling to replace outdated versions with the new code pushed to the main branch of the hosted repos.
