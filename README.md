# docker-credential-gcloud-cached

faster builds

## install

cached credential helper for gcr

    git clone https://github.com/matti/docker-credential-gcloud-cached.git
    cd docker-credential-gcloud-cached
    ln -s "$(pwd)/docker-credential-gcloud-cached" /usr/local/bin/docker-credential-gcloud-cached

sanity check:

    $ echo "eu.gcr.io" | docker-credential-gcloud-cached get
    {
      "Secret": "asdf.asdfasdfasdfasdf",
      "Username": "_dcgcloud_token"
    }

easy setup:

    $ docker-credential-gcloud-cached __cached_setup

example `$HOME/.docker/config.config`:

    {
      "credHelpers": {
        "eu.gcr.io": "gcloud-cached",
        "us.gcr.io": "gcloud-cached",
      }
    }
