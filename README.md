# Backend Service for Task Node Application

## Project Overview

This is a Node.js backend service designed for distributed task processing using the Koii Network's namespace wrapper. The application provides a flexible task execution framework with built-in support for task submission, auditing, and distribution.

### Key Features
- Dynamic task execution framework
- Integrated with Koii Network's blockchain infrastructure
- Supports custom task logic implementation
- Provides sample API endpoints for task state and value retrieval
- Containerized deployment support

## Getting Started

### Prerequisites
- Node.js (v16+ recommended)
- Yarn package manager
- Docker (optional, for containerized deployment)

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd js_app_deploy
```

2. Install dependencies:
```bash
yarn install
```

3. Copy and configure environment variables:
```bash
cp .env.example .env
# Edit .env with your specific configuration
```

### Running the Service

#### Development Mode
```bash
yarn start  # Starts the server
yarn prod-debug  # Starts with nodemon for live reloading
```

#### Testing
```bash
yarn test  # Runs unit tests
yarn jest-test  # Runs Jest tests
```

## API Documentation

### Available Endpoints

#### 1. Get Task State
- **Method**: GET
- **Path**: `/taskState`
- **Description**: Retrieves the current task state
- **Response**: 
  ```json
  {
    "taskState": { /* Task state object */ }
  }
  ```

#### 2. Get Stored Value
- **Method**: GET
- **Path**: `/value`
- **Description**: Retrieves a value stored in NeDB
- **Response**:
  ```json
  {
    "value": "Stored value"
  }
  ```

## Authentication

This service uses Koii Network's namespace wrapper for authentication and access control. Authentication is managed through the network's built-in mechanisms.

## Project Structure

```
.
├── index.js           # Main application entry point
├── coreLogic.js       # Core task processing logic
├── task/              # Task-specific modules
│   ├── audit.js
│   ├── distribution.js
│   └── submission.js
├── helper/            # Helper utility functions
└── tests/             # Test suites
```

## Technologies Used

- Node.js
- Express.js
- Koii Namespace Wrapper
- Web3.js
- Webpack
- Jest (Testing)
- Puppeteer (Optional browser automation)

## Deployment

### Docker Deployment
```bash
docker-compose up -d
```

### Environment Considerations
- Ensure proper configuration of `.env` file
- Set `TIMERS` environment variable to control task execution timers

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the ISC License. See `LICENSE` for more information.

## Contact

For more information, please contact the Koii Network team.