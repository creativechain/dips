# Account Structure

### json_metadata
This data must always have a **JSON format**.  The structure should be as follows.

| Field | Type | Required | Description |
|-------|------|----------|-------------|
|`avatar`| File | No | Image to use as user's avatar. Must be always type Image File with a MIME Type supported in common browsers (Chrome/Firefox/IE/Edge/Safari/Opera).|
|`publicName`| String | No | Name to display instead of @username.|
|`about` | String | No | This field should serve to offer information about the user such as his profession or his specialty in the creative world.
|`contact`| String | No | Information that allows you to contact the user. It can be an email, web link, etc ...
|`web` | String | No | Web link where you can obtain more extensive information from the user, such as other projects, portfolio, personal web, etc ...
|`lang`| String | No | Language tag used by user specified by [RFC 56485](https://tools.ietf.org/html/rfc5646) and [RFC 4647](https://tools.ietf.org/html/rfc46479).
|`other`| JSON Object | No | Optional field to include more data in JSON format.|

Example:
```json
{
  "avatar": {
    "hash": "QmeM35KLHNq52688QAmWUUShpmKAx6VbF1EpQdsiMMULiG",
    "name": "anderson-creativechain-perfil-1.png",
    "type": "image/png",
    "size": 15664,
    "url":  "https://ipfs.creary.net/ipfs/QmeM35KLHNq52688QAmWUUShpmKAx6VbF1EpQdsiMMULiG"
  },
  "publicName":"ander7agar",
  "about": "Crea Developer",
  "web": "https://creary.net/@ander7agar",
  "contact": "ander@creary.net",
  "lang":"en-US",
  "other": {
    "adult_content": "show",
    "post_rewards": "50",
    "comment_rewards": "50",
    "tags": ["developer", "crea", "programming", "software"]
  }
}
```