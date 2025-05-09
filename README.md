# Custom Glance Widgets

This is a collection of custom widgets for https://github.com/glanceapp.

- [paperless-ngx](https://github.com/anakles/glance-widgets?tab=readme-ov-file#paperless-ngx)
- [portainer](#portainer)


---

## Paperless-ngx

A widget for [paperless-ngx](https://docs.paperless-ngx.com/).

![paperless-ngx](images/paperless-ngx.png)

**Usage**

Copy the content of the file [`paperless-ngx.yaml`](paperless-ngx/paperless-ngx.yaml) at the position you like.

|Parameter|Value|Example|
|---|---|---|
|`${PAPERLESS_URL}`|The URL of your paperless-ngx instance.|e.g. `https://paperless.example.com`|
|`${PAPERLESS_TOKEN}`|An API token for paperless-ngx. Currently, only token-based authentication is supported.</br>Take a look at the official [paperless-ngx documentation](https://docs.paperless-ngx.com/api/#authorization) on how to create an API token.||

The widgets requires two variables, which can be configured in the glance `.env` file.
If you are using an `.env` file, add these lines:

```bash
# The URL to paperless-ngx
PAPERLESS_URL=https://paperless.example.com
# The API token for paperless-ngx
PAPERLESS_TOKEN=verySecureToken
```


---

## Portainer

A widget for [portainer CE](https://www.portainer.io/). It lists the total amount of containers and counts how many are running or stopped.

![portainer](images/portainer.png)

**Usage**

Copy the content of the file [`portainer.yaml`](portainer/portainer.yaml) at the position you like.

|Parameter|Value|Example|
|---|---|---|
|`${PORTAINER_URL}`|The URL of your portainer instance.|e.g. `https://portainer.example.com`|
|`${PORTAINER_ENV}` |The slug / ID for the portainer environment you want to monitor. </br>You can identify this environment the URL. |E.g. for `https://portainer.example.com/#!/2/docker/containers`, the slug would be `2`.|
|`${PORTAINER_API_KEY}`|An API key for your portainer instance.</br>Take a look at the official [portainer documentation](https://docs.portainer.io/api/access) on how to create an API token.|

The widgets requires two variables, which can be configured in the glance `.env` file.
If you are using an `.env` file, add these lines:

```bash
# The URL to portainer
PORTAINER_URL=https://portainer.example.com
# The slug / environment ID
PORTAINER_ENV=2
# The API key to access your portainer API
PORTAINER_API_KEY=verySecureApiKey
```


---


