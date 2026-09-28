# EmDash agent skills

[Agent Skills](https://agentskills.io) that teach coding agents how to build with [EmDash](https://emdashcms.com), the Astro-native CMS.

| Skill                                                             | Use it for                                                                  |
| ----------------------------------------------------------------- | --------------------------------------------------------------------------- |
| [`building-emdash-site`](skills/building-emdash-site/)             | Schema and seeds, content queries, Portable Text, menus, taxonomies, deploy |
| [`creating-plugins`](skills/creating-plugins/)                     | Sandboxed and native EmDash plugins: hooks, routes, storage, admin UI       |
| [`emdash-cli`](skills/emdash-cli/)                                 | Managing an EmDash instance from the command line                           |
| [`wordpress-theme-to-emdash`](skills/wordpress-theme-to-emdash/)   | Porting a WordPress theme to an EmDash site                                 |
| [`wordpress-plugin-to-emdash`](skills/wordpress-plugin-to-emdash/) | Porting WordPress plugin behavior to EmDash                                 |

The WordPress porting skills link to `building-emdash-site` and `creating-plugins`, so install those alongside them.

## Install

### Any agent

[`skills`](https://github.com/vercel-labs/skills) installs into Claude Code, Codex, Cursor, Copilot, Gemini CLI, OpenCode, Amp, Goose, Windsurf, Cline, Roo, Junie, and many more:

```sh
npx skills add emdash-cms/skills
```

Pass `--skill <name>` to pick individual skills, or `-g` to install for your user rather than the current project.

With the GitHub CLI:

```sh
gh skill install emdash-cms/skills --all
```

### Claude Code

```sh
/plugin marketplace add emdash-cms/skills
/plugin install emdash@emdash
```

Skills are available as `emdash:building-emdash-site` and so on. Third-party marketplaces don't auto-update by default; run `/plugin marketplace update emdash` to pick up changes, or turn on auto-update in `/plugin`.

### Codex

```sh
codex plugin marketplace add emdash-cms/skills
```

Then install the `emdash` plugin from the Plugins directory.

### GitHub Copilot CLI

```sh
copilot plugin install emdash-cms/skills
```

In VS Code, run **Chat: Install Plugin From Source** and enter `https://github.com/emdash-cms/skills`.

### Cursor

Open **Customize → Plugins → From GitHub Repository** and enter `https://github.com/emdash-cms/skills`.

### Factory Droid

```sh
droid plugin marketplace add emdash-cms/skills
droid plugin install emdash@emdash
```

### Manually

Copy the directories under [`skills/`](skills/) into your agent's skills directory. `.agents/skills/` in your project works for most agents.

## Contributing

This repository is generated. The skills live in [`skills/`](https://github.com/emdash-cms/emdash/tree/main/skills) in the [EmDash monorepo](https://github.com/emdash-cms/emdash) and sync here with each EmDash release, replacing anything edited directly. Open issues and pull requests there.

## License

MIT
