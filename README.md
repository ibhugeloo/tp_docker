# Conteneurisation DevOps

- Mise en place d’un cluster docker swarm
- Mise en place d’un stockage partagé glusterfs
- Mise en place de keepalived pour la HA réseau
- Déploiement de wordpress avec une base de données
- Exposition du service via un reverse proxy
- Mise en place de Prometheus pour la supervision

# Cluster Swarm

- docker node ls

# HA du réseau

- nano /etc/keeaplived/keepalived.conf
- systemctl status keepalived

# HA du stockage

- cd /mnt/mysql
- cd /mnt/wp-content
- cd /mnt/prometheus

- gluster pool list
- systemctl status glusterd

# Wordpress

- cd projet
- docker stack deploy -c docker-compose.yml wordpress
- docker stack ps wordpress
- docker stack rm wordpress

FQDN : grp8.wordpress.courses.studalya.net<br>
Identfiant : goat<br>
Mot de passe : KWYx&8qmoxcfljC(BK

# Prometheus

- cd prometheus
- docker stack deploy -c docker-compose.yml monitoring
- docker stack ps monitoring
- docker stack rm monitoring

FQDN : grp8.prometheus.courses.studalya.net
