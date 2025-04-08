
Built by https://www.blackbox.ai

---

# Real-time Collaborative Document Editor

## Project Overview

The **Real-time Collaborative Document Editor** is a web application that enables multiple users to collaboratively edit documents in real-time. Utilizing technologies like Node.js, Express, MongoDB, and sockets for real-time communication, this application aims to provide a seamless editing experience. It handles connection management, document synchronization, and error handling to ensure high reliability and performance.

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/realtime-doc-editor.git
   cd realtime-doc-editor
   ```

2. **Install dependencies:**

   Ensure you have [Node.js](https://nodejs.org/) installed (version 20.0.0 or higher). Then, run:

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory of the project and add the following variables:

   ```bash
   MONGODB_URI=mongodb://your_mongo_db_uri
   PORT=8000  # Or any port you'd like to use
   ALLOWED_ORIGINS=http://localhost:3000  # Adjust based on your needs
   ```

   Make sure to replace `your_mongo_db_uri` with your actual MongoDB connection string.

4. **Start the server:**

   You can start the application in development mode using:

   ```bash
   npm run dev
   ```

   or in production mode with:

   ```bash
   npm start
   ```

## Usage

To access the application:

1. Open your web browser and navigate to `http://localhost:8000`.
2. You can create/edit documents by going to the editor interface. Multiple users can join the same room to collaborate on editing a document.

### API Endpoints

- `GET /test`: A simple endpoint to check if the server is running.
- `POST /api/save-doc`: Save the document content to the database or to memory if MongoDB is not available.
- `GET /api/health`: Check the health status of the server including the database connection.

## Features

- **Real-time Collaboration**: Multiple users can edit the same document simultaneously.
- **Document Storage**: Documents are stored in a MongoDB database or in-memory if the database is unavailable.
- **Connection Management**: Handles user connections and disconnections properly.
- **Error Handling**: Robust error handling with appropriate response messages.
- **CORS Support**: Configurable CORS settings to restrict access to certain origins.

## Dependencies

The project requires the following dependencies, which will be installed automatically when you run `npm install`:

- [dotenv](https://www.npmjs.com/package/dotenv) - For loading environment variables from a `.env` file.
- [env-cmd](https://www.npmjs.com/package/env-cmd) - For managing environment variables.
- [express](https://expressjs.com/) - A web framework for Node.js for building APIs.
- [mongoose](https://mongoosejs.com/) - A MongoDB object modeling tool designed to work in an asynchronous environment.
- [socket.io](https://socket.io/) - For enabling real-time, bidirectional communication between web clients and servers.

## Project Structure

```plaintext
realtime-doc-editor/
├── public/                # Contains static files (e.g., HTML, CSS)
│   └── editor.html        # HTML file for the editor interface
├── node_modules/          # Project dependencies (auto-generated)
├── server.js              # Main server file
├── package.json           # Project metadata and dependencies
├── package-lock.json      # Locked dependency versions
├── railway.json           # Railway configuration file
├── tailwind.config.js     # Tailwind CSS configuration (if used)
└── .env                   # Environment variables configuration (not included in the repo)
```

## License

This project is licensed under the ISC License. See the [`LICENSE`](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests to improve this project.

## Author

Your Name - [Your GitHub Profile](https://github.com/yourusername)

---

Feel free to modify any sections of this README to better suit your project specifics!