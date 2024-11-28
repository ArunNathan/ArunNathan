FROM nginx

# Copy the wrapper script
COPY wrapper.sh /

# Make the wrapper script executable
RUN chmod +x /wrapper.sh

# Remove default nginx content
RUN rm -rf /usr/share/nginx/html/*

# Copy your custom HTML files
COPY html /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Use the wrapper script as the container's entry point
CMD ["/wrapper.sh"]

