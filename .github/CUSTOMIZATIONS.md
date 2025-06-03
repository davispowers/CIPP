# CIPP Fork Customizations

This file documents all customizations made to this fork of CIPP to help prevent merge conflicts during upstream syncs.

## Important: This fork NEVER pushes to upstream

All synchronization is one-way: FROM upstream TO this fork.

## Custom Files Added

1. `.github/workflows/auto-sync-upstream.yml` - Automated sync workflow
2. `.github/CUSTOMIZATIONS.md` - This documentation file

## Modified Files

List any files that have been customized in this fork:

### staticwebapp.config.json
- **Date**: June 3, 2025
- **Changes**: Accepted upstream version during v8.0.1 sync
- **Conflict Resolution**: Use upstream version (contains routes configuration)
- **Note**: This file configures Azure Static Web App routing and security

### Example format for future entries:
```
File: src/components/CustomComponent.js
Changes: Added custom branding and logo
Conflict Resolution: Keep our version during merges
```

## Merge Conflict Resolution Strategy

When conflicts occur during upstream syncs:

1. **package.json** - Usually keep upstream dependencies, but preserve any custom scripts
2. **version files** - Always take upstream version
3. **Custom components** - Keep our customizations
4. **Configuration files** - Review case by case

## Environment-Specific Settings

Document any environment-specific settings that should be preserved:

- Azure Static Web App configuration
- API endpoints
- Custom environment variables

## Notes

- The auto-sync workflow runs daily at 2 AM UTC
- Manual sync can be triggered from GitHub Actions
- Conflicts will create a PR for manual resolution
- Never modify upstream repository
