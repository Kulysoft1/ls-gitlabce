Run the image:

sudo docker run --detach \
	--hostname gitlab.example.com \
	--publish 8443:443 --publish 8080:80 --publish 2222:22 \
	--name gitlab \
	--restart always \
	--volume /srv/gitlab/config:/etc/gitlab \
	--volume /srv/gitlab/logs:/var/log/gitlab \
	--volume /srv/gitlab/data:/var/opt/gitlab \
	inistor/ls-gitlabce:latest

More information on Gitlab CE docker at http://doc.gitlab.com/omnibus/docker/
