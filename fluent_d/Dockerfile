FROM fluent/fluentd:v1.11-1

# Use root account to use apk
USER root

# below RUN includes plugin as examples elasticsearch is not required
# you may customize including plugins as you wish
RUN apk add --no-cache --update --virtual .build-deps \
        sudo build-base ruby-dev \
        && gem install elasticsearch \
        && sudo gem install fluent-plugin-elasticsearch --no-document -v 1.9.7 \
        && sudo gem sources --clear-all \
        && apk del .build-deps \
        && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem


USER fluent