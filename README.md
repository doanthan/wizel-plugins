# Wizel for Claude

Plan, make and review email marketing for your Shopify stores in [Wizel](https://www.wizel.ai), from Claude. One plugin adds the Wizel connector and a skill that teaches Claude how to use it.

## Claude (web, desktop, Cowork)

1. Open [Customize › Plugins](https://claude.ai/customize/plugins).
2. Click **Add › Add marketplace** and enter `doanthan/wizel-plugins`.
3. Open **Wizel** and click **Add**.
4. On its **Connectors** tab, add and connect Wizel, then sign in with your Wizel account.

The plugin is saved to your Claude account, so Claude Code gets it too.

## Claude Code

```bash
claude plugin install wizel --marketplace doanthan/wizel-plugins
```

Then type `/mcp` in Claude Code and sign in to Wizel.
