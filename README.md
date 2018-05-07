# getstarted

Exemples de Docker Domunetation / Get Started

https://docs.docker.com/get-started/

1: orientation

2: containers

3: Services

4: Swarms

5: Stacks

6: Deploy


## Descripció

a) Es crea un servei web amb un comptador de visites i es desa com a imatge getstarted al docker-hub.
És una pàgina web (atacant el port 80) que mostra la benvinguda i un comptador de visites (que no
anirà fins al final de tot que es configuri apropiadeaent redis).

b) S'executa com a un servei en un swarm individual usant un file yml de docker compose. 
Ovservar que es poden definir varies rèpliques. Atacant el port 80 contesta qualsevol dels containers, 
es pot observant amb el id que mostra).

c) Amb swarm i docker-machine es creen dues maquines virtuals (virtualbox) des de on executar els serveis.
El servei és el mateix docker compose. Ara es pot observar que les tasques es reparteixen entre els dos nodes del swarm.
Atacant el port 80 contesta 'algu' que pot estar en un node o l'altre.

d) Ampliem l'stack amb un visualizer que mostra les taskes i nodes. L'he ampliat amb portainer per mostrar/administrar 
visualment tot docker.

e) finalment s'amplia l'stack amb redis i es crea un volum perquè el comptador de visites no es desi en el container sinó
en un directori del host (en el cas concret el manager és una MV i es desa a /home/docker/data).


