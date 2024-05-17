FROM node:16

# Set the working directory
WORKDIR /workspace

# Copy package.json and package-lock.json
COPY frontend/package.json frontend/package-lock.json ./frontend/
COPY backend/package.json backend/package-lock.json ./backend/

# Install dependencies
RUN cd frontend && npm install
RUN cd ../backend && npm install

# Copy the project files
COPY . .

# Set the default command for the container
CMD ["bash"]
