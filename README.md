# Updates

This repository contains Watchtower – an automated update solution for docker images.

## Requirements

Make sure that the [Base](https://gitlab.com/hueske-digital/services/base) is already set up and started.

## Setup instructions

Clone the code to your server:<br>
```
git clone git@gitlab.com:hueske-digital/services/updates.git ~/services/updates
```

Create environment file and fill up with your values:<br>
```
cd ~/services/updates && cp .env.example .env && vim .env
```

Pull images and start the compose file:<br>
```
docker compose up -d
```

## Other information

Update all container images and recreate them if new images are available:<br>
```
docker compose pull && docker compose up -d
```

Restart a single container:<br>
```
docker compose restart app
```

Shutdown all container of this compose file:<br>
```
docker compose down
```

Show and follow logs:<br>
```
docker compose logs -ft
```

Additional configuration:<br>
You can include any other docker config by using an additional [compose file](https://docs.docker.com/compose/extends/).
