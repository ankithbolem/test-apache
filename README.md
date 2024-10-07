# Sample Apache Application

This is a simple Apache-based web application that will be served from an EC2 instance.
It includes a single `index.html` page, and the deployment is automated via Jenkins.

## How It Works
1. Jenkins will pull the latest code from the `feature/routelink` branch.
2. It will deploy the updated `index.html` file to the Apache web server on the EC2 instance.
3. Apache will serve the content from the `/var/www/html` directory.
