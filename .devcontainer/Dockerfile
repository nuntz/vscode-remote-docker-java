FROM openjdk:11

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

# Configure apt and install packages
RUN apt-get update \
    && apt-get -y install --no-install-recommends apt-utils dialog 2>&1 \ 
    #
    # Verify git and needed tools are installed
    && apt-get install -y git procps \
    #
    # Install Maven
    && apt-get -y install maven

# Switch back to dialog for any ad-hoc use of apt-get
ENV DEBIAN_FRONTEND=
