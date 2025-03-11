FROM jenkins/jenkins:lts

# Switch to root user to install dependencies
USER root

# Update package list and install required packages in one step
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    make \
    g++ \
    git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Switch back to Jenkins user (best practice)
USER jenkins
