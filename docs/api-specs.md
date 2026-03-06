# EggTrail API Integration Specs

## Endpoints

### GET `/v1/clue/drop`
Returns the active clue for the current timestamp. Requires `X-API-KEY`.

### POST `/v1/telemetry/checkin`
Payload:
```json
{
  "user_token": "uuid",
  "venue_code": "string",
  "timestamp": "iso-8601"
}
```

## Known Issues
Rate limiting may trigger if multiple users scan the same physical placard within 1 second.

Sara M. Cruz: Added bypass for authorized ops tokens during testing.
