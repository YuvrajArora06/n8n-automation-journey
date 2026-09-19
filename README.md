# n8n-automation-journey

# Weather Email Automation

My first n8n automation workflow.

## What it does

Fetches current weather information using OpenWeatherMap
and automatically sends the information through Gmail.

## Workflow

OpenWeatherMap → Gmail

## What I learned

- Working with APIs
- API authentication
- Passing JSON data between nodes
- n8n expressions
- Gmail OAuth2 authentication
- Google Cloud OAuth configuration

## Tools Used

- n8n (self-hosted)
- OpenWeatherMap API
- Gmail API
- Google OAuth 2.0

## Example

Temperature data is retrieved from OpenWeatherMap and accessed
using an n8n expression such as:

{{ $json.main.temp }}
