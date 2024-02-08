# Use an official PostgreSQL runtime as a parent image
FROM postgres:13.3-alpine

# The following environment variable sets the PostgreSQL password.
ENV POSTGRES_PASSWORD root

# The following environment variable sets the PostgreSQL username.
ENV POSTGRES_USER root

# The following environment variable sets the PostgreSQL database.
ENV POSTGRES_DB postgresdb

# Expose the PostgreSQL port
EXPOSE 5432

# Run the rest of the commands as the ``postgres`` user created by the ``postgres-13.3-alpine`` image
USER postgres

# These commands will be run when the Docker container starts
CMD ["postgres"]