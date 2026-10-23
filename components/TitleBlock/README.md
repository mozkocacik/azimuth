# TitleBlock

The signature of Azimuth. It comes from the title block of an engineering drawing and shows the identity of a document or record. Use it at the top of datasheets, notices, certificates and press releases, and in the footer of printed pages.

1.5px `text` outer border, 1px `border-strong` cell rules, square corners. Labels in 11.5px 600 `text-3`, values in 600 (`data` for numbers and dates).

| Field | Required | Format |
|---|---|---|
| Title | Yes | Product or subject, then document type |
| Document no. | Yes | `TT-NNNN-NNN`: type, product family, sequence |
| Revision | Yes | A, B, C … Drafts use 0.1, 0.2 |
| Release date | Yes | YYYY-MM-DD |
| Status | Yes | Draft, In review, Released, Withdrawn |
| Classification | Yes | Public, Registered, Partner, Confidential |
| Replaces, Language, Pages, Owner | When known | The owner is a department, not a person |

Below 560px the block has two columns.

**Content:** the fields above.
