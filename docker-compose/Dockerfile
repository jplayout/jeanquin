FROM jenkins/jenkins:lts-jdk11

COPY --chown=jenkins:jenkins plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt

ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
ENV CASC_JENKINS_CONFIG /var/jenkins_home/casc_configs/jenkins.yaml
COPY --chown=jenkins:jenkins jenkins.yaml /usr/share/jenkins/ref/casc_configs/jenkins.yaml