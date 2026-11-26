# Email Variants

An audience-aware email drafting skill with a built-in humanisation pass.

## What it does

Turn rough notes, an existing draft, or an email thread into a ready-to-send email tailored to the reader. The underlying facts stay fixed; the structure, vocabulary, emphasis and length change by audience.

### Included voices

- CEO / Founder
- COO / Operations
- Head of department
- Colleague / Team
- Action-oriented
- Donor / Funder
- External stakeholder
- Field / plain English
- Explain like I'm 3
- Sensitive / apology
- Firm / escalation
- Warm thanks
- Ultra-short

It also supports common email types such as replies, requests, follow-ups, status updates, report cover notes, declines, escalations, apologies, introductions, meeting requests or recaps, announcements, feedback, thanks, and handovers.

## Use

Install this folder as an Agent Skill in a compatible skills-enabled environment. Invoke it with a request such as:

```text
/email-variants ceo, coo, action

Please share the verified monthly KPI report by Friday.
```

Or ask in natural language:

```text
Write COO, colleague and donor versions of this email:
[paste notes or draft]
```

Use `/email-variants all` to request every voice that fits the content.

## Behaviour and safeguards

- Preserves names, figures, dates, commitments and claims from the supplied source.
- Uses placeholders for missing details rather than inventing them.
- Defaults to four variants when no audience is specified.
- Applies the built-in humanizer pass to every variant.
- Never sends email. It only drafts text; a separate connected mail workflow would require an explicit user request.

## Repository layout

```text
email-variants-skill/
├── README.md
├── LICENSE
└── email-variants/
    └── SKILL.md
```

## Attribution and licensing

The integrated humanisation guidance is adapted from the open-source [Humanizer skill](https://github.com/blader/humanizer) by blader, distributed under the MIT License. The upstream Humanizer package's included MIT notice identifies Siqi Chen as copyright holder; that notice is preserved in this repository's LICENSE file.

The email-specific workflow, audience voices, email types and examples in `email-variants/SKILL.md` are the custom skill author's contribution. The upstream MIT notice applies to the Humanizer-derived material; see LICENSE for its scope and notice.

## Compatibility

The skill uses the portable `SKILL.md` format. Availability and installation steps depend on the host application's Agent Skills support and account/workspace settings.
