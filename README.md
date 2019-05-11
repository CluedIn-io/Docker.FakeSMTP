# Fake SMTP server

Dockerization of [FakeSMTP](http://nilhcem.com/FakeSMTP/) running in a small `openjdk:alpine` container.

The container exposes the stmp server on port 25. The emails are simply written to the folder `/output` so mount it as an external volume.

Example: `docker run --rm -p "2525:25" -v "${PWD}/tmp/mails:/output" cluedin/fakesmtp`
