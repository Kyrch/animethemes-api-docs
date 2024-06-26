---
title: Playlist Destroy
---

# Playlist Destroy Endpoint

The playlist destroy endpoint soft deletes a playlist and returns the deleted playlist resource.

For example, the `/playlist/N4hG` endpoint will soft delete the playlist of id N4hG and return the deleted playlist resource.

## URL

```sh
DELETE /playlist/{id}
```

## Authentication

**Required Permission**: delete playlist

**Other Requirements**: User must own playlist & playlist must not be soft deleted

## Parameters

None

## Response

```json
{
    playlist: {
        id: "id",
        name: "name",
        description: "description",
        visibility: "visibility",
        created_at: "created_at",
        updated_at: "updated_at",
        deleted_at: "deleted_at",
        views_count: views_count,
        tracks_exists: tracks_exists,
        tracks_count: tracks_count
    }
}
```

## Example

```bash
curl -X DELETE -H "Authorization: Bearer {token}" https://api.animethemes.moe/playlist/N4hG
```
