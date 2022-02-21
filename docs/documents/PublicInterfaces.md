# TSLogger API Documentation

## Available HTTP endpoints

**POST:** /logError
**POST:** /logEvent

## Expected headers

**Authentication:** Bearer {{ JWT Access Token }}

## Expected request headers

### Error

```json
{
    "title": string,
    "message": string,
    "projectName": string,
    "class": string,
    "method": string,
    "stackTrace": string
}
```

### Event

```json
{
    "title": string,
    "message": string,
    "projectName": string,
    "class": string,
    "method": string,
    "eventCategory": string
}
```

## Possible responses

**Success:** 200
**Client error:** 400, 401, 404
**Server error:** 500
