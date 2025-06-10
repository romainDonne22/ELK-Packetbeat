Securité projet :

elasticsearch (ELK)
kibana (visualisation)
graphana

Capacté à rediger le rapport / les schémas / puis de visu kibana

Choisir un des deux projets, ne pas faire les deux

Projet indiviuel



# Projet Sécurité : ELK + Packetbeat

## Commandes utiles :  
  
J'ai eu des soucis de permissions sur le fichier packetbeat.yml (je travaille sous Windows / WSL)  
il est stocké chez moi sur /home/rom, il faut copier le fichier sur un repertoire ou on peut changer les droits :  
```sh 
cp -r /mnt/c/Users/romd3/OneDrive/Documents/Telecom/707Securite/projet ~/
cd ~/projet/packetbeat
chmod 644 ./packetbeat.yml
```

Lancer le docker comose depuis le repertoire projet :  
```sh 
cd ..
docker-compose up -d
```

Lancer le PCAP :
```sh
docker exec -it packetbeat bash #rentrer dans le bash du docker packbeat
ls -l /usr/share/packetbeat/packetbeat.yml #vérifier que le .yml est bien présent
ls -l /pcap #vérifier que le dossier pcap est bien présent
curl http://elasticsearch:9200 #écouter sur le bon port, lance les data dans ELK
cat /usr/share/packetbeat/packetbeat.yml #si besoin ouvrir le fichier
```
  
docker-compose restart packetbeat  


## Arborescence du projet



## Dashboard  
graph 1 : Nombre de paquet  
graph 2 : client.port  
graph 3 : dns.id
graph 4 : event.type
network.community_id  
related.ip  
source.port  
