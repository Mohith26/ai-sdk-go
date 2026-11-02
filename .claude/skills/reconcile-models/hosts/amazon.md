# Amazon (vendor of Nova)

Amazon's own pages for its models. Amazon has no package of its own: Bedrock sells its models, so this run owns them in `providers/bedrock` and names every offering `bedrock:<model ID>` (RULES.md, Report values). Start with `shared.md`, then `bedrock.md`.

## Pages

Amazon publishes its models' facts on their Bedrock model cards, so this run reads Bedrock's pages only.

| Fact | Page | Where on it |
|---|---|---|
| Models | `https://docs.aws.amazon.com/bedrock/latest/userguide/model-cards-amazon.md` | a link to each Amazon model's card |
| One model | the card the list links (`model-card-amazon-nova-2-lite.md` for Nova 2 Lite) | Model Details (launch date, knowledge cutoff, context window, max output), Programmatic Access, Regional Availability |

## Reading them

- The list holds Nova chat models and Titan, embedding, image, video and speech models.
- Bedrock is Amazon's API for its models, so `Released` is the card's Model launch date (released-first-callable) and `Knowledge` its Knowledge cutoff (knowledge-month-end).
- Rates, limits, capabilities, regions and lifecycle: as `bedrock.md` says. Amazon's models are in the price list's `AmazonBedrock` offer. Bedrock's lifecycle pages name no replacement (replacement-pick).
