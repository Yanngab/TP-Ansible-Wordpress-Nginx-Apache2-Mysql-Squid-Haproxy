# TP-Ansible-Wordpress-Nginx-Apache2-Mysql-Squid-Haproxy

Déploiement sur DEBIAN 10 de

- 1 server proxy SQUID par lequel les serveurs devront passer pour l'accès internet, couplé à un load balancer HA proxy qui renvoie ses requetes sur les serveurw web (Apache et Nginx)

- 1 Server Nginx passant par ce proxy, couplé d'une base de données Mysql destinée a Wordpress affichant la page par défaut de Wordpress via Nginx.

- 1 Server Apache affichant également la page par défaut de Wordpress grâce à la base Mysql du serveur Nginx, via Apache.


Méthode d'installation :

J'ai utilisé des machines Debians 10 propres pour ce TP.
Récupérer les adresses IP des 3 machines et modifier les adresses IP situées dans le fichier hosts ainsi que le fichier /vars/vars.yml.
Lancer ensuite le playbook squid-haproxy et ceux des 2 serveurs web.
Vous pourrez par ailleurs observer les stats de l'haproxy à l'adresse suivante : adresseIP/haproxy?stats
