# auth0-next-playground


To remove the "Log in to xxx to continue to xxx" and set a custom title :

Go to Applications > API > Auth0 Management API > Copy token

then:

```bash
curl --request PUT \
  --url 'https://DOMAIN/api/v2/prompts/login/custom-text/en' \
  --header 'authorization: Bearer TOKEN' \
  --header 'content-type: application/json' \
  --data '{ "login": { "title": "My App", "description": "Log In" } }'
```

```bash
curl --request PUT \
  --url 'https://DOMAIN/api/v2/prompts/signup/custom-text/en' \
  --header 'authorization: Bearer TOKEN' \
  --header 'content-type: application/json' \
  --data '{ "login": { "title": "My App", "description": "Create a new account" } }'
```
