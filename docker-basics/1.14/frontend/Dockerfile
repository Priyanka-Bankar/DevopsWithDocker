FROM node:16-alpine
# Set working directory
WORKDIR /usr/src/app
# Copy package files first (for better Docker cache)
COPY example-frontend/package*.json ./
# Install dependencies
RUN npm install
# Copy the rest of the frontend app    
COPY example-frontend/ ./
#make backend api to conncect to backend
ENV REACT_APP_BACKEND_URL=http://localhost:8080/
# Build the React app for production
RUN npm run build
# Install a lightweight static server to serve the app
RUN npm install -g serve
# Expose the port used by the static server
EXPOSE 5000
# Command to run the app
CMD ["serve", "-s", "-l", "5000", "build"]

