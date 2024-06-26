---
title: Playlist Restore
---

# Playlist Restore Endpoint

The playlist restore endpoint restores a soft deleted playlist and returns the restored playlist resource.

For example, the `/restore/playlist/N4hG` endpoint will restore the soft deleted playlist of id N4hG and return the restored playlist resource.

## URL

```sh
PATCH /restore/playlist/{id}
```

## Authentication

**Required Permission**: restore playlist

**Other Requirements**: User must own playlist & playlist must be soft deleted

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
curl -X PATCH -H "Authorization: Bearer {token}" https://api.animethemes.moe/restore/playlist/N4hG
```
