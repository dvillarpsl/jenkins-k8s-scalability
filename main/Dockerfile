FROM jenkins/jenkins:lts-alpine

# Installing all needed plugins
RUN /usr/local/bin/install-plugins.sh \
ssh-slaves \
git \
htmlpublisher \
greenballs \
simple-theme-plugin \
kubernetes \
blueocean \
credentials \
jobConfigHistory \
nexus-artifact-uploader \
slack \
sonar \
envinject \
groovy \
job-dsl

# in case you have a maven-global-settings-file.xml use the next line
# COPY maven-global-settings-files.xml /usr/share/jenkins/ref/maven-global-settings-files.xml

VOLUME /var/jenkins_home

# we will not run this image as root, instead we will use a user called jenkins
USER jenkins
