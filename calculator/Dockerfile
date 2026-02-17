# Use the latest Ubuntu image as the foundation [cite: 14-16]
FROM ubuntu:latest

# Set the working directory inside the container
WORKDIR /app

# Copy the script from your local VM directory into the container [cite: 17-19]
# Note: We use 'calci.sh' to match your 'ls' output
COPY calci.sh /app/calci.sh

# Ensure the script has execution permissions
RUN chmod +x /app/calci.sh

# Recommended: Install 'bc' in case your script uses it for floating point math
# and 'dos2unix' to fix potential Windows line-ending issues
RUN apt-get update && apt-get install -y bc dos2unix && dos2unix /app/calci.sh
