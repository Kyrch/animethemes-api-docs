---
title: Track Forward Index
---

# Track Forward Index Endpoint

The track forward index endpoint returns a listing of tracks for the playlist in forward order after the specified track.

## URL

```sh
GET /playlist/{playlist:id}/track/{track:id}/forward
```

## Authentication

**Required Permission**: view playlist track

**Other Requirements**: If the playlist is private, the user must own the playlist

## Parameters

| Name         | Required | Description                                                      |
| :----------: | :------: | :--------------------------------------------------------------- |
| fields       | No       | Sparse fieldsets for resource types                              |
| include      | No       | Inclusion of related resources                                   |
| page[number] | No       | The page of playlist resources to display                        |
| page[size]   | No       | The number of playlist resources to display for the current page |

## Allowed Include Paths

* video
* animethemeentry.animetheme.anime.images
* animethemeentry.animetheme.group
* animethemeentry.animetheme.song.artists
* video.audio

## Response

```json
{
    tracks: [
        {
            id: "id",
            created_at: "created_at",
            updated_at: "updated_at"
        },
        ...
    ],
    links: {
        first: "first",
        last: "last",
        prev: "prev",
        next: "next"
    },
    meta: {
        current_page: current_page,
        from: from,
        path: "path",
        per_page: per_page,
        to: to
    }
}
```

## Example

```bash
curl https://api.animethemes.moe/playlist/N4hG/track/Q3hD/forward
```