## amazon setup
``git clone https://github.com/adaptiveapplications/ckan-vagrant``

``cd ckan-vagrant/``

``./bootstrap_280.sh``

## enable ckan site
``sudo vim  /etc/ckan/production.ini # comment out ckan.max_image_size = 2``

``sudo -u solr cp ./artifacts/schema.xml /var/solr/data/ckan/conf/``

``sudo cp ./artifacts/ckan.conf /etc/apache2/sites-available/``

``sudo a2ensite ckan``

``sudo apache2ctl restart``

``sudo systemctl reload apache2``

## create a user
``cd /usr/lib/ckan/src/ckan/``

``. /usr/lib/ckan/bin/activate``

``paster sysadmin add parker -c /etc/ckan/production.ini``