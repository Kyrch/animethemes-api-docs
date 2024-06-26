---
title: Anime Theme Destroy
---

# Anime Theme Destroy Endpoint 

The anime theme destroy endpoint soft deletes an anime theme and returns the deleted anime theme resource.

For example, the `/animetheme/3373` endpoint will soft delete the OP1 theme for the Bakemonogatari anime and return the deleted anime theme resource.

## URL

```sh
DELETE /animetheme/{id}
```

## Authentication

**Required Permission**: delete anime theme

**Roles with Permission**: Wiki Editor, Encoder, Admin

**Other Requirements**: Anime theme must not be soft deleted

## Parameters

None

## Response

```json
{
    animetheme: {
        id: id,
        type: "type",
        sequence: sequence,
        slug: "slug",
        created_at: "created_at",
        updated_at: "updated_at",
        deleted_at: "deleted_at"
    }
}
```

## Example

```bash
curl -X DELETE -H "Authorization: Bearer {token}" https://api.animethemes.moe/animetheme/3373
```
