---
title: "Two-Factor Authentication (2FA)"
description: "How to enable and use two-factor authentication for enhanced security"
category: "features"
tags: ["security", "2fa", "authentication", "mfa"]
last_updated: "2024-12-25"
---

# Two-Factor Authentication (2FA)

Two-factor authentication adds an extra layer of security to your AceUnlock account by requiring a second form of verification in addition to your password.

## What is 2FA?

2FA requires two things to log in:
1. **Something you know**: Your password
2. **Something you have**: Your phone or authentication app

This means even if someone gets your password, they can't access your account without your second factor.

## Enabling 2FA

### Method 1: Authenticator App (Recommended)

1. Go to **Settings** > **Security**
2. Click **Enable Two-Factor Authentication**
3. Choose **Authenticator App**
4. Scan the QR code with your authenticator app (Google Authenticator, Authy, 1Password, etc.)
5. Enter the 6-digit code from your app
6. Save your backup codes in a secure location

### Method 2: SMS

1. Go to **Settings** > **Security**
2. Click **Enable Two-Factor Authentication**
3. Choose **SMS**
4. Enter your mobile phone number
5. Enter the verification code sent via SMS
6. Save your backup codes

## Using 2FA

Once enabled, every time you log in:
1. Enter your email and password as usual
2. You'll be prompted for your second factor
3. Enter the 6-digit code from your authenticator app or SMS
4. Click **Verify**

### Remember This Device

You can check "Remember this device for 30 days" to skip 2FA on trusted devices.

## Backup Codes

When you enable 2FA, you'll receive 10 backup codes. Each code can be used once if you:
- Lose your phone
- Can't access your authenticator app
- Don't receive SMS codes

**Important**: Store these codes in a safe place (password manager, secure note, etc.)

## Troubleshooting

### Lost Access to Authenticator App

1. Use one of your backup codes to log in
2. Disable 2FA in your security settings
3. Re-enable 2FA with a new device

### Not Receiving SMS Codes

- Verify your phone number is correct
- Check for carrier delays (wait 1-2 minutes)
- Try switching to authenticator app method
- Contact support if issue persists

### Backup Codes Not Working

Each backup code can only be used once. If you've used all 10 codes:
- Contact support at support@aceunlock.com
- Provide your account email and identity verification

## Disabling 2FA

To turn off 2FA:
1. Go to **Settings** > **Security**
2. Click **Disable Two-Factor Authentication**
3. Enter your password to confirm
4. Enter your current 2FA code

⚠️ **Warning**: Disabling 2FA makes your account less secure.

## Best Practices

- Use an authenticator app instead of SMS when possible
- Store backup codes securely
- Don't share your 2FA codes with anyone
- Enable 2FA on all team member accounts
- Update your phone number if it changes

## Related Articles

- [Security Settings Overview](./security-settings.md)
- [Account Security Best Practices](./security-best-practices.md)
- [Password Reset with 2FA Enabled](../troubleshooting/password-reset.md)
