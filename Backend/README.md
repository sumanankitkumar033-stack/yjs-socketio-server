# Collaborative Real-time Backend

This project is a high-performance Node.js backend designed to support real-time collaborative applications. It utilizes **Yjs** via the **y-socket.io** provider to synchronize shared states (CRDTs) across multiple clients seamlessly.

## 🚀 Features

- **Real-time Synchronization**: Powered by `y-socket.io` for robust, conflict-free data syncing.
- **WebSocket Communication**: Built on `socket.io` with full CORS support.
- **Health Monitoring**: Includes a `/health` endpoint for container orchestration and load balancer checks.
- **Static Asset Serving**: Pre-configured to serve frontend assets from the `public` directory.
- **Cloud Ready**: Optimized for Docker and AWS deployment environments.

## 🛠️ Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Real-time**: Socket.io
- **CRDT Provider**: y-socket.io

## 🏁 Getting Started

### Prerequisites

- Node.js (v16.x or higher recommended)
- npm or yarn

### Installation

1. Navigate to the backend directory:
   ```bash
   cd Backend
   ```

2. Install the required dependencies:
   ```bash
   npm install
   ```

### Configuration

Ensure your `package.json` includes `"type": "module"` to support the ES Module syntax used in `server.js`.

### Running the Server

Start the development server:
```bash
node server.js
```
The server will be available at `http://localhost:3000`.

## 📡 API & Socket Endpoints

| Type | Endpoint | Description |
| :--- | :--- | :--- |
| **GET** | `/health` | Returns a 200 OK status to verify server health. |
| **WS** | `/` | Main Socket.io connection point for Yjs synchronization. |

## 🐳 Docker Deployment

Since this project is optimized for Docker/AWS, you can build and run it using the following commands:

```bash
# Build the image
docker build -t collab-backend .

# Run the container
docker run -p 3000:3000 collab-backend
```

## 📄 License

This project is licensed under the MIT License.