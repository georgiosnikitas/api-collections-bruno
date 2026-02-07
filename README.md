# API Collections - Bruno

A collection of API requests and tests built with [Bruno](https://www.usebruno.com/), an open-source API client for exploring and testing APIs.

## About Bruno

Bruno is a fast, Git-friendly opensource API client. Unlike other API clients, Bruno stores your collections directly in a folder on your filesystem, making it easy to use Git or any version control system to collaborate with your team.

## Repository Structure

```
.
├── bruno-echo.bru           # Example Bruno request file
├── bruno.json               # Bruno collection configuration
├── api-collections-bruno/   # Workspace directory
│   ├── workspace.yml        # Workspace configuration
│   └── collections/         # Additional collections folder
├── .gitignore              # Git ignore rules
└── README.md               # This file
```

## Getting Started

### Prerequisites

- [Bruno](https://www.usebruno.com/downloads) installed on your machine

### Opening the Collection

1. Clone this repository:
   ```bash
   git clone https://github.com/georgiosnikitas/api-collections-bruno.git
   cd api-collections-bruno
   ```

2. Open Bruno and select "Open Collection"
3. Navigate to and select this repository folder

## Available Requests

### Bruno Echo

- **File**: `bruno-echo.bru`
- **Method**: POST
- **URL**: https://echo.usebruno.com
- **Description**: A test request to Bruno's echo service that returns the request data
- **Body**: JSON payload with message and environment fields
- **Tests**: 
  - Validates HTTP 200 status code
  - Verifies response contains args object

## Adding New Requests

1. In Bruno, create a new request within the collection
2. Configure the request (method, URL, headers, body, etc.)
3. Add any test scripts or pre-request scripts as needed
4. Save the request - it will be stored as a `.bru` file
5. Commit the new file to version control

## Environment Variables

To use environment-specific variables:

1. Create a `.env` file in the root directory (already .gitignored)
2. Add your variables in the format:
   ```
   API_KEY=your_api_key_here
   BASE_URL=https://api.example.com
   ```
3. Reference them in Bruno using `{{API_KEY}}` or `{{BASE_URL}}`

**Important**: Never commit API keys, tokens, or other secrets to version control.

## Testing

Run tests directly in Bruno by:
1. Opening a request
2. Clicking the "Run" button
3. Viewing the test results in the response panel

## Contributing

1. Create a new branch for your API collection changes
2. Add or modify `.bru` files as needed
3. Test your requests thoroughly
4. Commit with descriptive messages
5. Submit a pull request

## License

This project is open source. Please check with the repository maintainer for specific licensing information.

## Resources

- [Bruno Documentation](https://docs.usebruno.com/)
- [Bruno GitHub Repository](https://github.com/usebruno/bruno)
- [bruno.json Schema](https://docs.usebruno.com/bruno-cli/overview)
