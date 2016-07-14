FROM ubuntu:14.04
LABEL description="Base container image with the jenkins user configured"
MAINTAINER Alfonso Pérez (alpegon3@upv.es)

# Add jenkins user/group
RUN groupadd -g 1001 jenkins \
 && useradd -m -d /home/jenkins -s /bin/bash -g jenkins -u 1001 jenkins

RUN adduser jenkins sudo

# Enable passwordless sudo for users under the "sudo" group
RUN sed -i.bkp -e \
      's/%sudo\s\+ALL=(ALL\(:ALL\)\?)\s\+ALL/%sudo ALL=NOPASSWD:ALL/g' \
/etc/sudoers