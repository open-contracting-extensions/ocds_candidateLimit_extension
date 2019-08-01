# Second stage description

Adds a second stage object to the tender and lot objects, to describe the second stage of a two-stage procedure. In particular, it adds two fields to describe the limits on the number of candidates to be invited.

## Guidance

If there is an exact limit on the number of candidates, set `minimumCandidates` and `maximumCandidates` to the same number.

If `maximumCandidates` is set, use the selection criteria extension (TBD) to describe how the selection criteria will be used to select candidates to be invited for the second stage.

## Legal context

In the European Union, this extension's fields correspond to [eForms BG-709 (Second Stage)](https://github.com/eForms/eForms). See [OCDS for the European Union](http://standard.open-contracting.org/profiles/eu/master/en/) for the correspondences to Tenders Electronic Daily (TED).

## Example

```json
{
  "tender": {
    "lots": [
      {
        "id": "1",
        "secondStage": {
          "minimumCandidates": 5,
          "maximumCandidates": 50,
          "successiveReduction": true,
          "mayNotHaveNegotiation": false
        }
      }
    ]
  }
}
```

## Issues

Report issues for this extension in the [ocds-extensions repository](https://github.com/open-contracting/ocds-extensions/issues), putting the extension's name in the issue's title.
