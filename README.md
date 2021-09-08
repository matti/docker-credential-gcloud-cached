# docker-credential-gcloud-cached

faster builds

## install

cached credential helper for gcr

    git clone github.com/matti/docker-credential-gcloud-cached
    cd docker-credential-gcloud-cached
    ln -s "$(pwd)/docker-credential-gcloud-cached" /usr/local/bin/docker-credential-gcloud-cached

test:

    $ echo "eu.gcr.io" | docker-credential-gcloud-cached get
    {
      "Secret": "asdf.asdfasdfasdfasdf",
      "Username": "_dcgcloud_token"
    }

example `$HOME/.docker/config`:

    {
      "credHelpers": {
        "eu.gcr.io": "gcloud-cached",
        "us.gcr.io": "gcloud-cached",
      }
    }
