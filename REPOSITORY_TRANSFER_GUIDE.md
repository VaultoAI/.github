# Repository Transfer Guide - Moving to VaultoAI Organization

This guide explains how to safely transfer repositories to the VaultoAI GitHub organization without breaking Netlify deployments.

## Current Repository Status

The following repositories are currently under `charlie-818` and deployed on Netlify:

1. **vaulto-dev** (Vaulto Search)
2. **Vaulto-Swap** (Vaulto Swap) - Live at [app.vaulto.ai](https://app.vaulto.ai)
3. **vaulto-holdings** (Vaulto Holdings) - Live at [vaulto-holdings.netlify.app](https://vaulto-holdings.netlify.app)

## Transfer Process (Safe for Netlify)

### Step 1: Transfer Repository to Organization

1. **Go to the repository** on GitHub (e.g., `https://github.com/charlie-818/vaulto-dev`)
2. Click **Settings** → Scroll to **Danger Zone**
3. Click **Transfer ownership**
4. Enter the new owner: `VaultoAI`
5. Type the repository name to confirm
6. Click **I understand, transfer this repository**

**Important Notes:**
- The repository URL will change from `github.com/charlie-818/repo-name` to `github.com/VaultoAI/repo-name`
- All existing issues, pull requests, and commits are preserved
- The repository history remains intact
- **Netlify deployments will continue working** because they use the repository URL, which GitHub redirects automatically

### Step 2: Update Netlify Site Settings (After Transfer)

After transferring, update Netlify to use the new repository URL:

#### Option A: Update Repository Connection (Recommended)

1. Go to **Netlify Dashboard** → Select your site
2. Go to **Site settings** → **Build & deploy** → **Continuous Deployment**
3. Click **Link to a different repository**
4. Search for and select the repository under `VaultoAI` organization
5. Netlify will automatically update the connection

#### Option B: Manual Update (If Option A doesn't work)

1. Go to **Netlify Dashboard** → Select your site
2. Go to **Site settings** → **Build & deploy** → **Continuous Deployment**
3. Click **Edit settings**
4. Update the repository URL to the new organization path:
   - Old: `https://github.com/charlie-818/repo-name`
   - New: `https://github.com/VaultoAI/repo-name`
5. Save changes

### Step 3: Verify Netlify Deployment

1. **Check Build Settings**: Ensure build command and publish directory are still correct
2. **Verify Environment Variables**: All environment variables should be preserved
3. **Test Deployment**: Make a small commit to trigger a new build and verify it works
4. **Check Domain Settings**: Verify custom domains (like `app.vaulto.ai`) are still connected

### Step 4: Update Repository References

After transfer, update any hardcoded repository URLs in:

1. **README files** - Update GitHub links
2. **Documentation** - Update repository references
3. **Package.json** - If repository URLs are specified
4. **CI/CD workflows** - Update any GitHub Actions that reference the old path

## Netlify-Specific Considerations

### What Netlify Preserves Automatically

✅ **Environment Variables** - All environment variables remain intact  
✅ **Build Settings** - Build commands and publish directories are preserved  
✅ **Domain Settings** - Custom domains remain connected  
✅ **Deploy Hooks** - Webhooks continue to work  
✅ **Branch Deploys** - Branch deploy settings are maintained  

### What You Need to Update

⚠️ **Repository Connection** - Link to the new organization repository  
⚠️ **GitHub Permissions** - Netlify may need new OAuth permissions for the organization  

### Handling Netlify OAuth Permissions

If Netlify can't access the organization repository:

1. Go to **Netlify Dashboard** → **User settings** → **Connected accounts**
2. Click **Update** next to GitHub
3. Grant access to the `VaultoAI` organization
4. Re-link the repository in site settings

## Recommended Transfer Order

Transfer repositories one at a time to minimize risk:

1. **Start with vaulto-holdings** (simplest, no database)
2. **Then Vaulto-Swap** (app.vaulto.ai - important production site)
3. **Finally vaulto-dev** (most complex with database)

## Post-Transfer Checklist

After each repository transfer:

- [ ] Repository successfully transferred to VaultoAI organization
- [ ] Netlify site reconnected to new repository location
- [ ] Test deployment triggered successfully
- [ ] Production site still accessible and working
- [ ] Environment variables verified in Netlify
- [ ] Custom domains still connected
- [ ] README updated with new repository URLs
- [ ] Team members have access to new repository location

## Troubleshooting

### Issue: Netlify can't find the repository after transfer

**Solution:**
1. Disconnect the repository in Netlify
2. Reconnect using the new organization path
3. Grant Netlify access to the VaultoAI organization

### Issue: Builds failing after transfer

**Solution:**
1. Check build logs in Netlify
2. Verify environment variables are still set
3. Ensure build commands haven't changed
4. Check if any scripts reference the old repository path

### Issue: Domain not working after transfer

**Solution:**
1. Domain settings are independent of repository location
2. Check domain DNS settings in Netlify
3. Verify domain is still connected in site settings

## Alternative: Create New Repositories (Not Recommended)

If you prefer not to transfer (not recommended for production):

1. Create new repositories in VaultoAI organization
2. Push code to new repositories
3. Update Netlify to point to new repositories
4. **Downside**: Lose commit history, issues, and PRs

## Summary

**Transferring repositories is safe for Netlify** because:
- GitHub automatically redirects old URLs
- Netlify uses repository URLs that can be updated
- All deployment settings are preserved
- You just need to reconnect Netlify to the new location

The key is to **update Netlify's repository connection** after the transfer, which takes only a few minutes and doesn't require redeployment.

