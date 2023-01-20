- [Getting started | Plausible docs](https://plausible.io/docs/self-hosting)

```bash
# prepare
sudo mkdir /opt/plausible
cd /opt/plausible

# clone
sudo git clone https://github.com/plausible/hosting
cd hosting

# Add required configuration
sudo openssl rand -base64 64 | tr -d '\n' ; echo
# copy that ugly string

sudo vi plausible-conf.env
#then change your enviroment variables
```

```env
ADMIN_USER_EMAIL=
ADMIN_USER_NAME=
ADMIN_USER_PWD=
BASE_URL=
SECRET_KEY_BASE= the_ugly_string
```
