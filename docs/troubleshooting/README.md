---
title: "Troubleshooting"
description: "Solutions to common issues and errors"
has_children: false
nav_order: 5
permalink: /troubleshooting/
---

# Troubleshooting Guide

Find solutions to common issues and errors. If you don't find your issue here, contact support@aceunlock.com.

## Quick Links

- [Login Issues](#login-issues)
- [Password & 2FA Problems](#password--2fa-problems)
- [Access & Permissions](#access--permissions)
- [Email & Notifications](#email--notifications)
- [Integration Issues](#integration-issues)
- [Performance](#performance)

---

## Login Issues

### Can't Log In

**Symptoms**: Login page won't accept credentials

**Solutions**:
1. Verify you're using the correct email address
2. Check Caps Lock is off
3. Clear browser cache and cookies
4. Try incognito/private browsing mode
5. Reset password if needed

[Detailed: Password Reset](./password-reset.md)

---

### Account Locked

**Symptoms**: "Account locked" error message

**Causes**: Too many failed login attempts (5 in 15 minutes)

**Solution**:
- Wait 15 minutes and try again
- OR reset your password immediately
- OR contact support for immediate unlock

---

### Session Expired

**Symptoms**: Constantly logged out

**Solutions**:
1. Check your browser allows cookies
2. Disable browser extensions that block cookies
3. Update to latest browser version
4. Check if company firewall is interfering

---

## Password & 2FA Problems

### Password Reset Email Not Received

**Solutions**:
1. Check spam/junk folder
2. Wait up to 10 minutes (server delays)
3. Verify email address spelling
4. Add noreply@aceunlock.com to contacts
5. Request new reset email

**Still not working?** Contact support with your account email.

---

### 2FA Code Not Working

**Symptoms**: 6-digit code rejected

**Solutions**:
1. **Time sync issue**: Ensure device time is accurate (Settings → Time → Auto)
2. **Old code**: Wait for new code to generate (~30 seconds)
3. **Wrong app**: Verify you're using correct authenticator account
4. **Use backup code**: Each code works once

**Lost access to authenticator?**
1. Use one backup code to login
2. Disable 2FA in settings
3. Re-enable with new device

[Detailed: 2FA Troubleshooting](./2fa-issues.md)

---

### Can't Reset Password with 2FA Enabled

**Issue**: Password reset requires 2FA, but you can't access 2FA

**Solution**:
1. Use a backup code during password reset
2. If no backup codes available, contact support
3. Provide identity verification (account email + last login date)

---

## Access & Permissions

### "Access Denied" Error

**Symptoms**: Can't access certain features or pages

**Causes**:
- Insufficient permissions for your role
- Feature not available on your plan
- Account suspension (unpaid bills)

**Solutions**:
1. Contact your account admin to adjust permissions
2. Upgrade plan if feature requires higher tier
3. Check billing status

---

### Can't See Team Members

**Symptoms**: Team page is empty or missing people

**Solutions**:
1. Verify you have "View Team" permission
2. Check if you're in the correct workspace
3. Refresh page / clear cache
4. Check if members were removed

---

### Invitation Link Not Working

**Symptoms**: "Invalid invitation" or link expired

**Solutions**:
- Invitation links expire after 7 days
- Links are single-use
- Request new invitation from admin
- Check if you already have an account with that email

---

## Email & Notifications

### Not Receiving Any Emails

**Solutions**:
1. Check spam/junk folder
2. Add these to email whitelist:
   - noreply@aceunlock.com
   - notifications@aceunlock.com
   - support@aceunlock.com
3. Check email notification settings in app
4. Verify email address is correct in profile

---

### Too Many Notifications

**Solutions**:
1. Go to Settings → Notifications
2. Adjust notification preferences:
   - Disable digest emails
   - Set frequency to daily instead of instant
   - Mute specific channels
3. Unsubscribe from marketing emails (footer link)

---

## Integration Issues

### SSO Not Working

**Symptoms**: SSO login fails or redirects incorrectly

**Solutions**:
1. Verify SSO is enabled for your domain
2. Check you're using correct SSO login URL
3. Clear browser cache
4. Contact IT admin to verify SSO configuration
5. Check identity provider status page

**Admin troubleshooting**:
- Verify SAML metadata is current
- Check entity ID and ACS URL
- Review attribute mappings

[Detailed: SSO Setup](../features/sso.md)

---

### API Integration Errors

**Common Error Codes**:

**401 Unauthorized**
- Invalid API key
- API key expired
- API key revoked
- Solution: Generate new API key

**403 Forbidden**
- Insufficient permissions
- Plan doesn't include API access
- Solution: Upgrade plan or adjust API key permissions

**429 Too Many Requests**
- Rate limit exceeded (1000 requests/hour)
- Solution: Implement exponential backoff, upgrade to higher rate limit

**500 Server Error**
- Temporary server issue
- Solution: Retry with exponential backoff, check status page

[API Documentation](../api/README.md)

---

## Performance

### Slow Loading Times

**Solutions**:
1. Check your internet connection
2. Clear browser cache
3. Disable browser extensions
4. Try different browser
5. Check [status.aceunlock.com](https://status.aceunlock.com)

---

### Upload Failures

**Symptoms**: Files won't upload or timeout

**Solutions**:
1. Check file size limit (25MB for Free, 100MB for Pro)
2. Verify file type is supported
3. Check internet connection stability
4. Try smaller file or compress first
5. Use wired connection instead of WiFi

---

## Error Messages

### Common Error Codes

**ERR_001: Invalid Credentials**
- Wrong email or password
- Solution: Double-check credentials or reset password

**ERR_002: Account Not Found**
- Email not registered
- Solution: Create new account or verify email spelling

**ERR_003: Session Timeout**
- Inactive for too long
- Solution: Log in again

**ERR_004: Permission Denied**
- Insufficient access level
- Solution: Contact admin for permission upgrade

**ERR_005: Rate Limit Exceeded**
- Too many requests
- Solution: Wait 1 hour or contact support

**ERR_006: Payment Failed**
- Billing issue
- Solution: Update payment method in Settings → Billing

**ERR_007: Feature Not Available**
- Feature requires plan upgrade
- Solution: Upgrade plan or contact sales

---

## Browser Issues

### Supported Browsers

**Fully Supported**:
- Chrome 90+ ✓
- Firefox 88+ ✓
- Safari 14+ ✓
- Edge 90+ ✓

**Limited Support**:
- Internet Explorer (not recommended)

**Recommended**: Use latest version of Chrome or Firefox for best experience.

---

### Browser-Specific Issues

**Safari**:
- Enable "Prevent cross-site tracking" → OFF for AceUnlock domain
- Settings → Privacy → Cookies and website data

**Firefox**:
- Ensure "Enhanced Tracking Protection" allows AceUnlock
- Options → Privacy & Security → Custom

---

## Mobile Issues

### Mobile Browser Problems

**Solutions**:
1. Use landscape mode for better experience
2. Update mobile browser to latest version
3. Clear mobile browser cache
4. Try Chrome mobile instead of default browser
5. Request desktop site if needed

**Note**: Native mobile apps coming 2025

---

## Data & Sync Issues

### Changes Not Saving

**Solutions**:
1. Check internet connection
2. Wait a few seconds (auto-save in progress)
3. Refresh page to verify
4. Check browser console for errors (F12)
5. Try different browser

---

### Data Not Syncing Across Devices

**Solutions**:
1. Force refresh (Ctrl+F5 or Cmd+Shift+R)
2. Log out and log back in
3. Clear cache on all devices
4. Check if you're in correct workspace

---

## Getting More Help

### Before Contacting Support

Gather this information:
- Your account email
- Browser and version
- Operating system
- Screenshot of error message
- Steps to reproduce the issue
- When the issue started

### Contact Methods

**Email**: support@aceunlock.com
- Response time: 24 hours (Free/Pro), 2 hours (Enterprise)

**Live Chat**: Bottom right corner
- Available: 9am-5pm EST, Mon-Fri

**Emergency Support** (Enterprise only):
- Phone: 1-800-XXX-XXXX
- Available: 24/7

### Before You Call

1. Check [status page](https://status.aceunlock.com)
2. Search this troubleshooting guide
3. Try solutions above
4. Clear cache and try different browser

---

## Status & Known Issues

Check current status and known issues:
- [status.aceunlock.com](https://status.aceunlock.com)
- Subscribe to status updates
- Follow @AceUnlock on Twitter

---

**Still having issues?** Email support@aceunlock.com with details about your problem.
