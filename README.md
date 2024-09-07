# genai-apps-docker
Docker compose files to stand-up some GenAI apps:

- **Open WebUI**
- **ComfyUI** (adapted from [Huggingface Spaces Example](https://huggingface.co/spaces/SpacesExamples/ComfyUI/blob/main/Dockerfile))
- **Prometheus/Grafana** (adapted from [Docker Examples](https://github.com/docker/awesome-compose/blob/master/prometheus-grafana/README.md))
- **Docker Registry**

Will add more as I find them useful for my home setup.

## Update Compose.yml file

Before going all cowboy and firing this, up, I recommend updating the comments in the compose.yml and make the following changes:

- Update the password in Grafana: [GF_SECURITY_ADMIN_PASSWORD=Ch@ngeMeN0w!](https://github.com/drikster80/genai-apps-docker/blob/main/compose.yaml#L34)
- Point ComfyUI model location to wherever your models directly lives [$PWD/comfyui-models](https://github.com/drikster80/genai-apps-docker/blob/main/compose.yaml#L52)
- Update the hostname of the server for the registry [REGISTRY_HTTP_HOST](https://github.com/drikster80/genai-apps-docker/blob/main/compose.yaml#L60)
- Change the registry data volume location [$PWD/registry-data](https://github.com/drikster80/genai-apps-docker/blob/main/compose.yaml#L66)