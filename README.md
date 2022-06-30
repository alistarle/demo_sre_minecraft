# Monitoring of a minecraft server

## Run an instance on OVH public cloud

1. Create a new instance on OVH public cloud

2. Put the following userdata:

        #!/bin/bash
        curl -fsSL https://get.docker.com | sudo sh
        sudo usermod -aG docker ubuntu
        su ubuntu
        cd /home/ubuntu
        git clone https://github.com/alistarle/demo_sre_minecraft
        cd demo_sre_minecraft
        docker compose up -d

3. Go to grafana: http://YOUR_INSTANCE_IP:3000

4. Login to the minecraft server using http://YOUR_INSTANCE_IP:25565
