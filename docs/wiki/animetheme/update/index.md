---
title: Anime Theme Update
---

# Anime Theme Update Endpoint

The anime theme update endpoint updates an anime theme and returns the updated anime theme resource.

For example, the `/animetheme/3373?song_id=3373` endpoint will update the song_id attribute of the OP1 theme for the Bakemonogatari anime and return the updated anime theme resource.

## URL

```sh
PUT|PATCH /animetheme/{id}
```

## Authentication

**Required Permission**: update anime theme

**Roles with Permission**: Wiki Editor, Encoder, Admin

**Other Requirements**: Anime theme must not be soft deleted

## Parameters

| Name     | Required | Rules                       |
| :------: | :------: | :-------------------------- |
| anime_id | No       | integer, Anime ID exists    |
| type     | No       | EnumValue [OP, ED]          |
| sequence | No       | integer, min:0              |
| slug     | No       | string, max:192, alpha_dash |
| song_id  | No       | integer, Song ID exists     |

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
curl -X PATCH -H "Authorization: Bearer {token}" https://api.animethemes.moe/animetheme/3373
```
