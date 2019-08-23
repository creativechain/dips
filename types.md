# Data Types


### File type

The File structure allows to know the information of a file published in the blockchain, in addition to providing a URL 
where the file is located.

 - `type` (String): MIME Type of file.
 - `name` (String): Name of file including extension.
 - `hash` (String): File hash to verify its integrity.
 - `size` (Number): Size of file in bytes.
 - `url` (String): URL where the file is located. This URL must be accessible for any.
 
 Example:
```json
{
  "type":"image/jpeg",
  "name":"IMG_20190726_120540-EFFECTS.jpg",
  "hash":"Qmd9MPHKtdpMPQjRppiAqx6DshevQJ73FVvWmYnpwWBUk1",
  "size":"4187664",
  "url":"https://ipfs.creary.net/ipfs/Qmd9MPHKtdpMPQjRppiAqx6DshevQJ73FVvWmYnpwWBUk1"
 }
```

### HTML Structure
This structure is created simply to indicate that texts should be displayed as HTML.

 - `type` (String): Always `text/html`.
 - `value` (String): HTML Text.
 
 Example:
```json
{
  "type":"text/html",
  "value":"<h4><strong>The 23rd GAMMA reward from the Creativechain Foundation goes to @maleev </strong></h4>"
}
```