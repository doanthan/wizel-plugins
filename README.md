# Wizel for Claude

Plan, make and review email marketing for your Shopify stores in [Wizel](https://www.wizel.ai), from Claude. One plugin adds the Wizel connector and a skill that teaches Claude how to use it.

## Claude (web, desktop, Cowork)

1. Open [Plugins](https://claude.ai/plugins).
2. Click **Add › Add marketplace › Add from a repository**, enter `doanthan/wizel-plugins`, choose it in the list and click **Sync**.
3. Open **Wizel** and click **Add**.
4. Click **Connect** beside Wizel, then **Continue › Add**.
5. Sign in to Wizel, pick your stores and click **Allow**.

The plugin is saved to your Claude account, so Claude Code gets it too.

## Claude Code

```bash
claude plugin install wizel --marketplace doanthan/wizel-plugins
```

Then type `/mcp` in Claude Code and sign in to Wizel.
