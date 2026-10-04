# Tesla OE cross reference — Tesla Model 3 and Model Y part numbers (open dataset)

**Tesla part number lookup data:** Tesla OE (original equipment) part numbers and
Partslink numbers for Tesla Model 3 and Model Y collision and suspension parts, grouped
by part, with the cars and production dates each part fits. Use it to cross-reference a
Tesla OE number from a collision estimate to the part it belongs to, or to find every
Tesla part number a bumper, fender, headlight or tail light has carried. It is the data
behind the free [Tesla part finder](https://maplev.ca/oe-lookup/) at maplev.ca, published
by MapleV, an independent Tesla collision parts supplier in Richmond, British Columbia,
Canada that ships to every province.

Keywords: Tesla OE cross reference · Tesla part number lookup · Tesla Model 3 parts ·
Tesla Model Y parts · Partslink · collision parts · open data · CSV · JSON · Canada

- 282 parts, 513 Tesla OE numbers, 343 base numbers (as of 2026-10-03)
- Partslink numbers for 76 of the parts
- Part names in English and French
- CSV and JSON

## Files

| File | Contents |
| --- | --- |
| `data/tesla-oe-cross-reference.csv` | One row per part |
| `data/tesla-oe-cross-reference.json` | The same parts as JSON, with French fitment text and a `meta` block |

## Columns

| Column | Meaning |
| --- | --- |
| `part_id` | MapleV's reference for the part (P-001 …) |
| `name_en`, `name_fr` | Part name |
| `category` | Part type, for example Front Bumper Parts or Headlights & Tail Lights |
| `models` | Tesla models the part fits, separated by ` \| ` |
| `fitment` | Models and production dates, as shown on the part page |
| `side` | Left, Right, or empty |
| `tesla_oe_numbers` | Tesla OE numbers for the part, separated by ` \| `; the first is the main number |
| `base_numbers` | The first seven digits of those numbers |
| `partslink` | The Partslink number of the part, where we could confirm one (see below); empty otherwise |
| `url_en`, `url_fr` | The part's page on maplev.ca, with photos, price and availability. The links carry a tag that tells maplev.ca a visit came from this dataset |
| `source` | MapleV (maplev.ca). Please keep this column when you reuse the data |

In a number such as `1514952-00-E`, `1514952` is the base number, `00` the middle code
and `E` the revision letter. More in
[How to read Tesla part numbers](https://maplev.ca/guides/how-to-read-tesla-part-numbers-revisions-interchange/).

## How the data is kept

All numbers were re-checked in October 2026 against Tesla's parts catalogue and
independent sources. Numbers we could not confirm were removed.

We update this repository when the catalogue changes; the date of the data is in the
JSON file (`meta.as_of`). The dated snapshots at maplev.ca/data/ are frozen and are not
updated, so where the two differ, this repository is the current one.

## Partslink numbers

Body shops and aftermarket suppliers order collision parts by Partslink number. We list
one only when at least two independent published catalogues match it to the part: either
both tie it to the part's Tesla OE number, or one does and the other describes the same
part for the same car, side and years. We checked them in October 2026.

76 parts have a Partslink number. The others are empty because the part has none
(suspension parts and filters, for example) or because we have not confirmed one yet.

Partslink is a numbering system of the Automotive Body Parts Association (ABPA). The
numbers are listed for identification and cross-reference only and are not covered by
the licence of this dataset.

## Limits

- A matching number is a search key, not proof of fit. Tesla changes some parts within a
  model year (sensor holes, connector pins, headlamp type), so check the part against
  the car before ordering.
- It covers the parts in MapleV's catalogue, not Tesla's whole parts catalogue.
- A Partslink number names the aftermarket version of a part. Some of our parts are
  genuine or remanufactured Tesla parts; the number is there so you can match them to an
  estimate.
- It has no prices or stock. Those are on each part's page.

## Look up numbers without downloading anything

- [maplev.ca/oe-lookup](https://maplev.ca/oe-lookup/): type a number, or paste a whole
  estimate and check every number at once. French: [maplev.ca/fr/oe-lookup](https://maplev.ca/fr/oe-lookup/).
- The same finder as a browser extension, a phone app, or a box on your own website:
  [Free Tesla part finder](https://maplev.ca/guides/free-tesla-part-finder/).

## Use and credit

The data, apart from the Partslink numbers, is licensed under [CC BY 4.0](LICENSE).
You can use, share and adapt it, including commercially, as long as you credit MapleV
and link to https://maplev.ca/oe-lookup/. Suggested credit:

> Tesla OE cross-reference by MapleV (maplev.ca)

To cite it, use [CITATION.cff](CITATION.cff).

## Not affiliated with Tesla

MapleV is an independent supplier of aftermarket replacement parts and is not
affiliated with, endorsed by, or authorized by Tesla, Inc. Tesla, Model 3 and Model Y
are trademarks of Tesla, Inc. OE numbers are used for identification and
cross-reference only.

Corrections and questions: [maplev.ca/contact](https://maplev.ca/contact/).
