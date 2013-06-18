log4php-graylog2
============

Forked from https://github.com/d-ulyanov/log4php-graylog2.
MIT License

Enhancements / Fixes from forked version:

-Converts project to a composer based project: no longer requiring manually copying files into log4php
-Fixes the the issue of MDC_ being prepended to MDC key/values
-Allows for file / line to be overridden enabling custom php error handling scripts to log the original file/line of the
actual error.
-Fixes timestamp not being logged correctly
-Logs the logger name separate from the facility
-Allows facility name to be overridden
-Increases "Short Message" to 255

-----------
Using composer, adds the ability for 2 new appenders:
LoggerAppenderAMQP and LoggerAppenderGraylog2.

You can pass log messages to Graylog2 or AMQP (RabbitMQ for ex.) using it.

Appender LoggerAppenderGraylog2 can pass messages directly to Graylog2 server.<br />
Appender LoggerAppenderAMQP can pass messages to AMQP Server. In this case you can set up yours graylog2 to recieving messages from AMQP.

If you would like to pass messages in GELF format, use special layout: LoggerLayoutGelf

-----------
Usage:

1. Add this project to your composer file
2. Set up your log4php config file (see exampleConfig.xml):
