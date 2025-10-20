FROM rabbitmq:4-management-alpine
RUN apk add curl
RUN curl -o /opt/rabbitmq/plugins/rabbitmq_delayed_message_exchange-4.1.0.ez -L https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/v4.1.0/rabbitmq_delayed_message_exchange-4.1.0.ez
RUN chown -R rabbitmq:rabbitmq /opt/rabbitmq/plugins/rabbitmq_delayed_message_exchange-4.1.0.ez
RUN rabbitmq-plugins enable rabbitmq_delayed_message_exchange
