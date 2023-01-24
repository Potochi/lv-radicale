FROM python:3.10-alpine

# Install radicale
RUN python -m pip install --upgrade radicale

# Create the radicale user and group
RUN addgroup -S radicale
RUN adduser -S radicale -G radicale

# Create the collections folder and set up restrictive permissions
RUN mkdir -p /var/lib/radicale/collections  \
    && chown -R radicale:radicale /var/lib/radicale/collections \
    && chmod o= /var/lib/radicale/collections

CMD python -m radicale