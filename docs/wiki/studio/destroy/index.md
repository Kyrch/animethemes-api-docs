---
title: Studio Destroy
---

# Studio Destroy Endpoint

The studio destroy endpoint soft deletes a studio and returns the deleted studio resource.

For example, the `/studio/shaft` endpoint will soft delete the Shaft studio and return the deleted Shaft resource.

## URL

```sh
DELETE /studio/{slug}
```

## Authentication

**Required Permission**: delete studio

**Roles with Permission**: Wiki Editor, Encoder, Admin

**Other Requirements**: Studio must not be soft deleted

## Parameters

None

## Response

```json
{
    studio: {
        id: id,
        name: "name",
        slug: "slug",
        created_at: "created_at",
        updated_at: "updated_at",
        deleted_at: "deleted_at"
    }
}
```

## Example

```bash
curl -X DELETE -H "Authorization: Bearer {token}" https://api.animethemes.moe/studio/shaft
```
