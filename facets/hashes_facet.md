# Hashes facet

The **Hashes** facet groups different types of hashes into a single structure, for an item on OneDrive.

## JSON representation

A set of hash values for the file.

<!-- { "blockType": "resource", "@odata.type": "oneDrive.hashes" } -->
```json
{
  "crc32Hash": "string (hex)",
  "sha1Hash": "string (hex)",
  "quickXorHash": "string (base64)"
}
```
## Properties

| Property name | Type          | Description                                           |
|:--------------|:--------------|:------------------------------------------------------|
| **sha1Hash**  | hex string | SHA1 hash for the contents of the file (if available). |
| **crc32Hash** | hex string | The CRC32 value of the file (if available).            |
| **quickXorHash** | base64 string | A [proprietary hash](../snippets/quickxorhash.md) of the file that can be used to determine if the contents of the file have changed (if available).|

**Note:** In some cases hash values may not be available. Downloading the item
can cause the hash values to be populated.

## Remarks

In OneDrive for Business and SharePoint Server 2016, **sha1Hash** and **crc32Hash** are not available.

In OneDrive Personal, **quickXorHash** is not available.

To calculate **quickXorHash** for a file, refer to the [QuickXorHash snippet](../snippets/quickxorhash.md).

<!-- {
  "type": "#page.annotation",
  "description": "The hashes facet provides hash identifiers for a file in OneDrive",
  "keywords": "hash,sha1,crc32,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Hashes"
} -->
