# GitHub Setup Instructions

## Push to GitHub

After creating your repository on GitHub, run these commands:

```bash
# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/oscpCheatsheet.git

# Verify the remote
git remote -v

# Push to GitHub (first time)
git push -u origin main

# For subsequent pushes
git push
```

## Alternative: Using GitHub CLI

If you have `gh` CLI installed:

```bash
# Create repo and push in one command
gh repo create oscpCheatsheet --public --source=. --remote=origin --push

# Or create as private
gh repo create oscpCheatsheet --private --source=. --remote=origin --push
```

## Setting Up Labels

After pushing, create these labels in your GitHub repository for better organization:

- `cheatsheet-entry` (default, already in template)
- `enumeration` 
- `exploitation`
- `privesc`
- `post-exploitation`
- `file-transfer`
- `web`
- `active-directory`
- `buffer-overflow`
- `linux`
- `windows`

### Quick Label Creation with GitHub CLI

```bash
gh label create enumeration --color "0E8A16" --description "Enumeration techniques"
gh label create exploitation --color "B60205" --description "Exploitation techniques"
gh label create privesc --color "D93F0B" --description "Privilege escalation"
gh label create post-exploitation --color "FBCA04" --description "Post-exploitation"
gh label create file-transfer --color "006B75" --description "File transfer methods"
gh label create web --color "1D76DB" --description "Web application attacks"
gh label create active-directory --color "5319E7" --description "Active Directory"
gh label create buffer-overflow --color "E99695" --description "Buffer overflow"
gh label create linux --color "C2E0C6" --description "Linux-specific"
gh label create windows --color "BFD4F2" --description "Windows-specific"
```

## Creating Your First Entry

1. Go to your GitHub repository
2. Click "Issues" → "New Issue"
3. Select "OSCP Cheat Sheet Entry" template
4. Fill in the sections (see `EXAMPLE_ENTRY.md` for reference)
5. Add appropriate labels
6. Submit the issue

## Workflow

Your typical workflow will be:

1. **Learn a new technique** in your OSCP labs
2. **Create an issue** using the template
3. **Add relevant labels** for easy filtering
4. **Search/browse issues** when you need quick reference during practice or exam

## Tips

- Keep entries focused on one technique per issue
- Include working examples you've personally tested
- Update entries when you discover variations
- Use GitHub's search to quickly find commands during practice
