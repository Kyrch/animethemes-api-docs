---
title: Resource Store
---

# Resource Store Endpoint

The resource store endpoint creates a new external resource and returns the new external resource.

For example, the `/resource?link=https%3A%2F%2Fmyanimelist.net%2Fanime%2F5081%2F&site=MyAnimeList` endpoint will create a new MyAnimeList resource for the Bakemonogatari anime and return the new MyAnimeList resource.

## URL

```sh
POST /resource
```

## Authentication

**Required Permission**: create external resource

**Roles with Permission**: Wiki Editor, Encoder, Admin

## Parameters

| Name        | Required | Rules                                                                                                                  |
| :---------: | :------: | :--------------------------------------------------------------------------------------------------------------------- |
| link        | Yes      | max:192, url, link matches site                                                                                        |
| external_id | No       | integer, min:0                                                                                                         |
| site        | Yes      | EnumValue [Official Website, Twitter, AniDB, Anilist, Anime-Planet, Anime News Network, Kitsu, MyAnimeList, Wikipedia, Spotify, YouTube Music, YouTube, Apple Music, Amazon Music, Crunchyroll, HIDIVE, Netflix, Disney Plus, Hulu, Amazon Prime Video] |

## Response

```json
{
    resource: {
        id: id,
        link: "link",
        external_id: external_id,
        site: "site",
        created_at: "created_at",
        updated_at: "updated_at",
        deleted_at: "deleted_at",
        link: "link"
    }
}
```

## Example

```bash
curl -X POST -H "Authorization: Bearer {token}" https://api.animethemes.moe/resource/
```
