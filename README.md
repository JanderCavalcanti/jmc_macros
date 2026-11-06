# Oficina de Macros

Site estático de https://macro.jmctecnologia.com.br.

- `app/` é servido como está pelo container `jmc_macros` (nginx:1.27-alpine, porta 8080) no CT 102 (apps, 192.168.5.235).
- No CT 102 este repo fica clonado em `/opt/jmc_macros`; o timer `apps-atualizar` (`/opt/apps/atualizar.sh`) puxa a `main` a cada 5 min. Como o nginx monta `app/` direto, não precisa reconstruir nada.
- A configuração do container está no repo `proxmox`, pasta `apps-docker/` (`docker-compose.yml` e `jmc_macros/nginx.conf`).
