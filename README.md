# Containerized WordPress configuration
A demo for containerized wordpress
---

### HowTo:

- Using ansible and some tags would help to initiate all containers at once. For ease of use, the certbot directive from compose file is commented to bring the app completely at init step. Then you can uncomment that and gain certificate. Just please substitude your domain name!

  With below command find the appropriate tag you want to play:
   ```
   ansible-playbook playbook/playbook.yaml -i playbook/inventory.yaml --list-tasks
   ```

  With defining tag, you can run/update just the application you need to be updated:
   ```
   ansible-playbook playbook/playbook.yaml -i playbook/inventory.yaml --tags proxy
   ```

- Or, just change your directory to the root of the project and run:
`docker compose up -d`
 ,and verify all containers all up and running:
`docker ps`
