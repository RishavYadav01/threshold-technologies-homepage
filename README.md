# Threshold Technologies — Homepage Design

Internship assignment submission for Zapper Edge.

**Live page:** _add your GitHub Pages link here once deployed_
**Design file:** [`index.html`](./index.html)

## The brief

Design a homepage for an enterprise IT engineering company whose core areas are AI & data / product engineering, enterprise integration, and domain-specific AI fine-tuning, and which also has its own proprietary product — a secure, trusted file transfer platform across organizational and technology domains.

## My interpretation

I named the company **Threshold Technologies** and its product **Threshold Relay**. The idea behind the name: IT services, integration work, and secure cross-domain file transfer are all fundamentally about the *boundary* between systems — where enterprises actually get stuck. Every section of the page (the hero diagram, the "why us" section, the product spotlight) reinforces that one idea instead of presenting three unrelated service lines.

**Page structure:** nav → hero (headline + boundary/domain diagram) → three capabilities (AI/data engineering, enterprise integration, domain fine-tuning) → why-choose-us → Threshold Relay product spotlight → a 3-step "how we start" engagement flow with a direct contact CTA → FAQ → footer.

## Q1. Who is the target customer?

Mid-size to large enterprises in regulated or systems-heavy industries — financial services, healthcare, logistics, government/public sector. These organizations have legacy infrastructure, real compliance constraints, and data that has to move between internal systems and outside partners. The buyer is typically a CTO, VP of Engineering, or Head of Data/AI — someone who's been burned by generic consultancies or generic AI tools that don't hold up against their actual systems and regulations. This is not a self-serve SMB product; the whole page (embedded engineers, working sessions instead of sales pitches, audit trails) is written for a buyer who needs to justify the engagement to a risk or compliance function.

## Q2. What's the most important message in the first 10 seconds?

That this company specializes in the hard, unglamorous connective tissue of enterprise IT — the boundaries between systems, teams, and partners — rather than being a generic "AI consultancy." The headline ("Your systems don't fail at the center. They fail at the edges.") plus the boundary diagram next to it do that job together: a visitor should immediately understand (a) this is a services company for complex enterprise environments, and (b) it has real technical depth, evidenced by having built its own product for exactly this problem.

## Q5. How would you structure content for AI platforms (ChatGPT, etc.) to understand and surface the company?

- **Explicit, self-contained factual statements** rather than marketing fluff — e.g. "Threshold Relay is a secure file transfer platform that moves data across organizational and technology domains." AI systems extract sentences like this far more reliably than a vague tagline.
- **An FAQ section with direct question/answer pairs** ("What does Threshold Technologies do?", "What is Threshold Relay?", "What is domain-specific AI fine-tuning?") — this is the format LLMs quote from most reliably, and it's also marked up with `FAQPage` schema.
- **Schema.org JSON-LD** (`Organization` + `Service`/`SoftwareApplication` offers) embedded in the page `<head>`, so crawlers get a structured, unambiguous entity graph instead of just prose to parse.
- **Consistent naming** — "Threshold Relay" is never referred to by a different name elsewhere on the page, so it reads as one consistent entity rather than several fuzzy variants.
- **Clean heading hierarchy** (one H1, real H2/H3 structure per section) so content can be chunked correctly by section rather than pulled out of context.
- I'd also add a plain-text `llms.txt` at the root summarizing the same facts, since several AI crawlers now check for it directly.
