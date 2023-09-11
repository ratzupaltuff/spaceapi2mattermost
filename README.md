# Spaceapi to Mattermost Bot
This Bot updates a Mattermost room according to the Spaceapi status.

A config like this is needed:
```
---
url: chat.domain.de
user: username
password: yourpasswordgoeshere
```

# Run the Container with Docker
```
sudo docker build -t spaceapi2mattermost .
sudo docker run -v ./s77-status-bot-config.yaml:/config/config.yaml:ro -d --name sapi2mm spaceapi2mattermost
```
to stop the container:
```
sudo docker stop sapi2mm
```


Interesting links:
Python Library https://vaelor.github.io/python-mattermost-driver/endpoints.html#module-mattermostdriver.endpoints.channels
Mattermost Api https://api.mattermost.com/#tag/channels/operation/UpdateChannel
