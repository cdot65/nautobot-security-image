FROM ghcr.io/nautobot/nautobot:latest-py3.10

# ---------------------------------------------------------------------------
# Metadata
# ---------------------------------------------------------------------------
LABEL name="ghcr.io/cdot65/nautobot-security-image"
LABEL maintainer="cremsburg.dev@gmail.com"
LABEL description="Nautobot container image with security packages."
LABEL license="Apache 2.0"
LABEL url="https://github.com/cdot65/nautobot-security-image"
LABEL build-date="20221105"

# ---------------------------------------------------------------------------
# Add and install python packages
# ---------------------------------------------------------------------------
ADD requirements.txt /var/tmp/requirements.txt
RUN /usr/local/bin/python -m pip install -r /var/tmp/requirements.txt

# ---------------------------------------------------------------------------
# Add and install custom configuration file
# ---------------------------------------------------------------------------
ADD nautobot_config.py /opt/nautobot/nautobot_config.py
