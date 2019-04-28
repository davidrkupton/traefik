## Scripts ...

This folder contains scripts which can help with the deployment of containers.

If a docker container is configured to:
 1. use traefik.entrypoint.sh script as its entrypoint,    
 (i.e. ```entrypoint: /path-here/traefik-entrypoint.sh```)   
 and,  
 1. mounts this script folder to /helpers   
 (i.e. ```volumes: ./scripts:/helpers```)    
  
 then ...:
 * An ssh certificate will be generated/refreshed and mounted on startup, and
 * Other scripts in a `/scripts` folder will also be executed, (mount a volume with scripts if desired) and
 * ENVARS can be set to control things:
    * TRAEFIK_NEEDS_EXEC
    * TRAEFIK_NO_SCRIPTS: Don't run scripts in the `/scripts` folder.
    * TRAEFIK_NO_USER_PERMS
    
