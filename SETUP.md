# Personal Executive AI Assistant Setup

This is a personal fork of the Executive AI Assistant. Follow these steps to set up your personal configuration:

## Initial Setup

1. **Copy the configuration template:**

   ```bash
   cp eaia/main/config.yaml.template eaia/main/config.yaml
   ```

2. **Edit your personal configuration:**

   - Open `eaia/main/config.yaml`
   - Replace all placeholder values with your personal information
   - Customize the triage rules, preferences, and background information

3. **Set up Google Workspace credentials:**
   - Follow the original README instructions for Gmail/Calendar setup
   - Your credentials will be stored in `.secrets/` (already ignored by git)

## Important Security Notes

- **Never commit** your `config.yaml` file - it contains personal information
- **Never commit** anything in `.secrets/` - it contains authentication tokens
- The `.gitignore` file is configured to protect these files automatically

## Updating Your Fork

To pull updates from the original repository while keeping your personal config:

```bash
# Add the original repo as upstream
git remote add upstream https://github.com/langchain-ai/executive-ai-assistant.git

# Fetch updates
git fetch upstream

# Merge updates (your personal config will remain safe)
git merge upstream/main
```

## Files That Are Personal and Protected

- `eaia/main/config.yaml` - Your personal configuration
- `.secrets/` - Your authentication tokens
- Any other files you customize with personal information

## Files That Are Safe to Commit

- Code changes and improvements
- `eaia/main/config.yaml.template` - Template for others to use
- Documentation updates
- Bug fixes and features
