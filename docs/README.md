<!-- @format -->

# Autocrat FAQ

## What is Autocrat?

**Autocrat** is Interlock's API that tells you if a URL is malicious or not.

- It takes a URL as a string in a `POST` request
- It returns a boolean: `true` for safe and `false` for malicious

## Autocrat is in beta

Autocrat is in its early stages as an enterprise product. It will occasionally go down or return errors.

## Pricing info

For details regarding price and payment schedule, please contact Interlock CEO Rick Deacon at rick@interlock.network

## How to get an API key

After payment, we will coordinate safe transfer of a unique API key that you will use to access Autocrat.

## API URL

The URL for Autocrat is `{url}`

## API request shape

To use Autocrat, make a `POST` request with the following shape:

```
{
     "key": "{api key}",
     "url": "url"
}
```

## Normal response

```
{
     "safe": {boolean},
     "url": "url"
}
```

## Errors responses

```
{
     "error": "{error description string}",
     "safe": undefined,
     "url": "url"
}
```

**Specific errors**

- "Unsupported protocol" i.e. FTP, SSH, or anything not HTTP/S
- "Malformed URL" i.e. google....com or google,com
- "Scan took too long"
- "Site offline (code 404)"
- "Too many redirects"
- "URL cannot be scanned"

## Support

For support questions, contact autocrat@interlock.network
