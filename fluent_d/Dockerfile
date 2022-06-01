# # FROM fluent/fluentd:v1.14-1
# # FROM fluent/fluentd:latest
# FROM fluent/fluentd:v1.4.2-2.0

# # Use root account to use apk
# USER root

# # below RUN includes plugin as examples elasticsearch is not required
# # you may customize including plugins as you wish
# RUN apk add --no-cache --update --virtual .build-deps \
#         sudo build-base ruby-dev \
#  && sudo gem install fluent-plugin-elasticsearch \
#  && sudo gem sources --clear-all \
#  && apk del .build-deps \
#  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem


# USER fluent


FROM fluent/fluentd:v1.4.2-2.0

USER root

RUN fluent-gem install fluent-plugin-elasticsearch
