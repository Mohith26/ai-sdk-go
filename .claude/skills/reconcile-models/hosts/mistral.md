# Mistral AI (vendor of Mistral models)

Mistral AI's own pages for its models. Mistral has no package of its own: Bedrock sells its models, so this run owns them in `providers/bedrock` and names every offering `bedrock:<model ID>` (RULES.md, Report values). The Bedrock cards give each copy's facts (`bedrock.md`); Mistral's pages give the model-wide ones. Start with `shared.md`.

## Pages

| Fact | Page | Where on it |
|---|---|---|
| Models | `https://docs.mistral.ai/models.md` | one row per model: name, API name, status, context |
| One model | the `https://docs.mistral.ai/models/<page>.md` the models page links | API names, Status, Release date, Version, Context length, Input, Output, Features, Deprecation date, Retirement date, Replacement |
| Lifecycle stages | `https://docs.mistral.ai/inference/model-lifecycle.md` | what Labs, Public Preview, General Availability, Deprecated and Retired mean |
| Every docs page | `https://docs.mistral.ai/llms.txt` | an index |

## Reading them

- Mistral's pages describe Mistral's own API, which no package in this SDK calls. Most models there aren't on Bedrock, and some are other vendors' (Z.ai, DeepSeek).
- Match a Bedrock card to its Mistral page by model name, since the IDs differ: Mistral Large 3 is `mistral.mistral-large-3-675b-instruct` on Bedrock, `mistral-large-2512` on Mistral's API, and its page is `mistral-large-3-25-12.md`.
- `Released`: the model page's Release date, the day it reached Mistral's API (released-first-callable).
- Replacement: for a Bedrock copy that Bedrock's pages mark Legacy or EOL, the model page's Replacement is the vendor's pick (replacement-pick); Bedrock's lifecycle tables name none.
- **Never copy lifecycle from Mistral's API to Bedrock.** A model page's Status, Deprecation date and Retirement date are for Mistral's API: on 2026-11-02, Mistral Large 3's page said Deprecated (deprecation date 2026-10-31, retirement 2027-04-30), while its Bedrock card gave no EOL date. Bedrock copies take their dates only from Bedrock's pages (lifecycle-exact-date).
- Context length, inputs and features on Mistral's pages are for Mistral's API; Bedrock copies take theirs from the card (limit-follow, capability-follow).
- Neither Mistral's pages nor the Bedrock card give a knowledge cutoff.
