---
title: Artist Force Delete
---

<Block>

# Artist Force Delete Endpoint

The artist force delete endpoint hard deletes an artist and returns a confirmation message.

For example, the `/api/forceDelete/artist/chiwa_saito` endpoint will hard delete the Chiwa Saito artist and return a confirmation message.

## URL

```sh
DELETE /api/forceDelete/artist/{slug}
```

## Authentication

**Required Permission**: force delete artist

**Roles with Permission**: Admin

## Parameters

None

## Response

```json
{
    message: "The Artist 'Chiwa Saito' was deleted.",
}
```

<Example>

<CURL>
```bash
curl -X DELETE -H "Authorization: Bearer {token}" https://staging.animethemes.moe/api/forceDelete/artist/chiwa_saito
```
</CURL>

</Example>

</Block>