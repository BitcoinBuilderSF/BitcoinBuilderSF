## Builders Turin 👋

**Builders Turin** is a monthly meetup focused on discussing product, design, and AI tools for individuals building on bitcoin. It is the Turin chapter of the Bitcoin Builder network. Everyone is welcome, whether you're an experienced product manager or designer, just starting out, or simply curious to learn.

Each month the agenda is community-generated. Have a topic? <!-- TODO(rebrand): add the Turin Twitter/X handle --> DM us on Twitter or submit a pull request to the relevant event file under the `content` folder.

The moderators will compile all the ideas into an ordered list to guide the discussion.

Audience participation is not only encouraged but is a required part of this meetup, whether by asking questions or sharing information and opinions on each topic. There will also be opportunities for live demos, allowing attendees to showcase their projects.

Here are some example topics:
1. New bitcoin products
2. Tools such as vibecoding, SDKs, and design guides
3. Metrics covering bitcoin usage
4. Bitcoin design best practices
5. Emerging and potential bitcoin startups
6. Use cases for bitcoin
7. The impact of tax and policies for product builders

<!-- TODO(rebrand): confirm the Turin venue and cadence -->
The meetup occurs in Turin. Follow us for updates. Let’s get ₿uilding!

## Development

This site is built with [Zola](https://www.getzola.org/). Common commands (see the `justfile`):

- `just serve` — run the site locally with drafts
- `just check-links` — verify internal links
- `zola build` — produce the static site in `public/`

The site is deployed to <https://bitcoinbuilderturin.xyz> via GitHub Pages (see `.github/workflows/ci.yaml`).
