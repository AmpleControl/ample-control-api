
```markdown
# Ample Control Node.js API

This Node.js API facilitates integration with the Ample Control SaaS (Software as a Service) platform.
Ample Control are a cutting-edge manufacturing software company dedicated to optimizing production efficiencies for Manufacturing companies.

## Prerequisites

Before using this API, ensure you have:

- Node.js installed on your machine
- An active account with Ample Control and your API credentials handy

## Installation

```bash
npm install amplecontrol
```


## Usage

To start using the API, you can import it into your Node.js project:

```javascript
const ampleControl = require('./ample-control');
```

Then, you can make calls to Ample Control's endpoints using the provided methods.

```javascript
// Example: Get workstation summary
const jsonPost = {
      key:your_api_key,
      secret: your_api_secret,
      type: 'wsSummary',
      options : {
            ID: WorkstationID
                }
    }

ampleControl.request(jsonPost)
  .then(data => {
    console.log('Workstation Summary:', data);
  })
  .catch(err => {
    console.error('Error fetching data from AmpleData API:', err);
  });


```

Replace `your_api_key` and `your_api_secret` with your actual API key and secret obtained from Ample Control.


## API Documentation

For detailed documentation on available endpoints and methods, refer to the [Ample Control API Documentation](https://amplecontrol.com/docs/).

## License

This project is licensed under the [MIT License](LICENSE).
