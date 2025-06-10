Securité projet :

elasticsearch (ELK)
kibana (visualisation)
graphana

Capacté à rediger le rapport / les schémas / puis de visu kibana

Choisir un des deux projets, ne pas faire les deux

Projet indiviuel



docker-compose up -d

J'ai eu des soucis de permissions sur le fichier packetbeat.yml
il est stocker chez moi sur /home/rom
si vous travaillez sur WSL il faut copier le fichier sur un repertoire ou vous pouvez changer les droits
puis faire : 
cp -r /mnt/c/Users/romd3/OneDrive/Documents/Telecom/707Securite/projet ~/
cd ~/packetbeat
chmod 644 ./packetbeat.yml
puis modifier le docker compose dans la partie volume de packetbeat mettre votre repertoire


docker exec -it packetbeat bash
ls -l /usr/share/packetbeat/packetbeat.yml
ls -l /pcap
curl http://elasticsearch:9200
cat /usr/share/packetbeat/packetbeat.yml

docker-compose restart packetbeat