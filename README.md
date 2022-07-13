# projectD1_d134
Модуль D1. Задание D1.3.4

Чтобы не возится с VPN для Terraform, все VM были созданы вручную. Но файл решения внимательно изучен :)

docker-compose.yml приведен к виду v3, позже добавлены параметры для репликации.


Команды:

docker swarm init --advertise-addr 10.128.0.27 

docker swarm join --token SWMTKN-1-35z9tgjwpg7zdvh2xd9etnqoecpglmuuxudo4loqh5fcsaw5sz-2m2clu3r3k5vto0jv6d02albe 10.128.0.27:2377

docker node ls

docker stack deploy --compose-file docker-compose.yml d134demo

docker stack services d134demo

docker stack ps d134demo

docker service scale d134demo_edge-router=2

docker stack rm d134demo


