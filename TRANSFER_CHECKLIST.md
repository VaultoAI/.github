# Quick Transfer Checklist

## For Each Repository (vaulto-dev, Vaulto-Swap, vaulto-holdings)

### Before Transfer
- [ ] Backup current Netlify site settings (screenshot or export)
- [ ] Note current repository URL
- [ ] Verify Netlify site is working correctly

### Transfer Repository
- [ ] Go to repository → Settings → Danger Zone
- [ ] Click "Transfer ownership"
- [ ] Enter new owner: `VaultoAI`
- [ ] Confirm transfer

### Update Netlify (Critical Step)
- [ ] Go to Netlify Dashboard → Your Site
- [ ] Site settings → Build & deploy → Continuous Deployment
- [ ] Click "Link to a different repository"
- [ ] Select repository from VaultoAI organization
- [ ] OR manually update repository URL to `github.com/VaultoAI/repo-name`

### Verify Everything Works
- [ ] Trigger a test deployment (make a small commit)
- [ ] Verify build succeeds in Netlify
- [ ] Check production site is still accessible
- [ ] Verify environment variables are intact
- [ ] Check custom domain still works (if applicable)

### Update Documentation
- [ ] Update README.md with new repository URL
- [ ] Update any other documentation references

## Quick Commands (After Transfer)

If you need to update local git remotes:

```bash
# Update remote URL to new organization
git remote set-url origin https://github.com/VaultoAI/repo-name.git

# Verify
git remote -v
```

## Important Notes

✅ **Safe**: Transferring repositories does NOT break Netlify  
✅ **Automatic**: GitHub redirects old URLs automatically  
⚠️ **Required**: Update Netlify repository connection after transfer  
⚠️ **Permissions**: May need to grant Netlify access to VaultoAI organization  

## If Something Goes Wrong

1. Netlify can't access repository → Grant organization access in Netlify settings
2. Build fails → Check environment variables are still set
3. Site down → Verify domain settings in Netlify (usually not affected)

