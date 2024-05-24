FROM nginx:latest

# Copy the custom configuration file to the NGINX directory
COPY nginx.conf /etc/nginx/nginx.conf

# Remove the default.conf file
RUN rm /etc/nginx/conf.d/default.conf

# Expose the necessary port (e.g., 80 for HTTP)
EXPOSE 80