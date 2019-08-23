# Posts/Comment Data Structure

### json_metadata
This data must always have a JSON format. Posts and comments actually use the same element internally in the blockchain,
 the difference between them is that the comment is linked to a "parent" (a post or other comment). The structure for 
    the posts should be as follows.

- `description` (String): Description of post/project/work.
- `tags` (String Array): Post related tags. The first tag must be the same that "parent_permlink".
- `thumb` (File): Thumbnail image that represent the project. Must be always type Image File with a MIME Type supported 
in common browsers (Chrome/Firefox/IE/Edge/Safari/Opera).
- `format` (String): Format of the content of the "body" field. It can be one of the following:
    - `markdown`: Text in markdown format.
    - `html`: Text in HTML format. Without CSS styles.
    - `data`: JSON-Array of Data types.
- `app` (String): Text string indicating the application used that modified / edited the publication, including the 
version.
- `other` (JSON|Optional): Optional field to include more data in JSON format.

Example:
```json
{
    "description": "Speed Art Inside",
    "tags": ["vlog", "speedart", "highspeedvideo", "video", "photomanipulation", "fashion", "editorial", "pinup" ],
    "thumb": {
        "hash": "QmXbnxMPcnLzbHzRZpvihganV2TF6mAi8GUkKqNJMLCiod",
        "name": "CrearVlogGif.gif",
        "type": "image\/gif",
        "size": 131112,
        "url": "https:\/\/ipfs.creary.net\/ipfs\/QmXbnxMPcnLzbHzRZpvihganV2TF6mAi8GUkKqNJMLCiod"
    },
    "format": "data",
    "app": "Creary/1.0",
    "other": {
        "license": 32,
        "adult": false
    }    
}
```

### body
This field is the content of the publication that should be displayed. The interpretation of the content must follow the
 format indicated in the `format` field of `json_metadata`.

- `data` format example:
```json
[
  {
    "hash":"Qmc1k24yUizFGVW7Rt3CenZXac3JwQjNsCNrcnrwCkV4XG",
    "name":"A5EF54A8-BAAE-414A-9DF8-13D0BF554125.png",
    "type":"image/png",
    "size":"148640",
    "url":"https://ipfs.creary.net/ipfs/Qmc1k24yUizFGVW7Rt3CenZXac3JwQjNsCNrcnrwCkV4XG"
  },
  {
    "value":"<p><a href=\"https://dada.art/pa/109638\">https://dada.art/pa/109638</a>... Soltics empez&oacute; en Chile, ahora Daveed en los &Aacute;ngeles,,,me col&eacute; entre grandes .ðŸ˜�</p>\n",
    "type":"text/html"
  }
] 
```

- `html` format example:
```html

<p>
    <img src="https://ipfs.creary.net/ipfs/QmddkHYSV9h5XXfKWm9ihvn2YTCwv2Swu7gvDBZButBTv1" />
</p>
<h4>
    <strong>The 23rd GAMMA reward from the Creativechain Foundation goes to @maleev</strong>
</h4>

<p>Katya Maleev is a freelance children's illustrator from Russia who shares her beautiful work on her Creary portfolio.</p>

<p>This reward is in recognition of her commitment to the network and quality of her portfolio.</p>

<p>We are happy that 1000 CGY are sent to Katya so her projects will gain more visibility on Creary and her energy will increase. This way her influence as curator in the network will be greater.</p>

<p>
    Visit @maleev's profile: <a href="https://creary.net/@maleev">creary.net/@maleev</a>;
</p>
```
- `markdown`

```markdown
# Crea Data Improvement Proposals

### This repository is intended to establish a standard data structure for the information published in the Crea Network.

#### The fields returned by the Create Nodes that need a structure are the following:

##### Posts/Comments:
- body
- json_metadata

##### Accounts:
- json_metadata
```