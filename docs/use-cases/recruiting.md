---
title: "AceUnlock for Recruiting Teams"
description: "Streamline candidate management and hiring workflows with AceUnlock"
category: "use-cases"
tags: ["recruiting", "hr", "hiring", "candidates"]
last_updated: "2024-12-25"
---

# AceUnlock for Recruiting Teams

Modern recruiting requires managing access for hundreds of candidates, contractors, and interviewers. AceUnlock makes it simple and secure.

## Recruiting Challenges Solved

### Challenge 1: Candidate Access Management
**Problem**: Candidates need temporary access to assessment portals, interview platforms, and documents.

**AceUnlock Solution**:
- Create time-limited guest accounts
- Auto-expire access after interview process
- Track which candidates accessed what materials
- Revoke access instantly if needed

### Challenge 2: Interview Coordination
**Problem**: Multiple interviewers need coordinated access to candidate profiles and feedback forms.

**AceUnlock Solution**:
- Role-based access for interviewers
- Shared candidate workspaces
- Real-time collaboration on feedback
- Automatic access provisioning per interview schedule

### Challenge 3: Contractor Onboarding
**Problem**: Contract recruiters need quick access without full employee privileges.

**AceUnlock Solution**:
- Contractor-specific roles
- Limited-scope permissions
- Easy offboarding when contract ends
- Audit trail of all contractor actions

### Challenge 4: Compliance & Privacy
**Problem**: Managing candidate data while staying GDPR/CCPA compliant.

**AceUnlock Solution**:
- Automated data retention policies
- Audit logs for all candidate data access
- Easy data deletion for right-to-be-forgotten requests
- Role-based data access controls

## Typical Recruiting Workflows

### Workflow 1: High-Volume Hiring

For companies hiring 50+ people per month:

**Setup**:
1. Create candidate access template
2. Set up automated access provisioning
3. Configure 90-day auto-expiration
4. Enable access request workflow

**Daily Workflow**:
1. Recruiter receives new candidate → Creates guest account from template
2. Candidate gets email with secure login
3. Candidate completes assessments/uploads documents
4. Access automatically expires after 90 days
5. If hired, convert to employee account

**Time Saved**: ~15 minutes per candidate

---

### Workflow 2: Executive Search

For specialized/executive roles:

**Setup**:
1. Create confidential workspace
2. Restrict access to core hiring team
3. Enable detailed audit logging
4. Set up secure document sharing

**Process**:
1. Create private workspace for each search
2. Grant access only to relevant stakeholders
3. Share candidate profiles securely
4. Track all document views
5. Maintain confidentiality throughout process

**Benefits**: Complete confidentiality, full audit trail

---

### Workflow 3: Interview Day Coordination

For onsite interview days:

**Setup**:
1. Create interviewer role with limited permissions
2. Set up interview workspace template
3. Configure day-of access provisioning

**Day-Of**:
1. Morning: Grant all interviewers access to candidate profiles
2. During: Interviewers submit feedback in real-time
3. Evening: Review all feedback in centralized location
4. Next Day: Revoke temporary interviewer access

**Benefits**: Organized feedback, no data leaks

## Features for Recruiting

### Guest Access Management
- Unlimited guest accounts
- Time-limited access (1 day to 1 year)
- Custom permission sets
- Bulk invite capabilities
- Auto-expiration

**Use Case**: Candidate assessments, contractor access

[Learn More: Guest Access](../features/guest-access.md)

---

### Access Templates
- Pre-configured role templates
- One-click provisioning
- Consistent permissions
- Easy duplication

**Use Case**: Standardize candidate/interviewer access

[Learn More: Access Templates](../features/access-templates.md)

---

### Audit Logs
- Who accessed what data
- When access was granted/revoked
- Document download tracking
- Compliance reporting

**Use Case**: GDPR compliance, security audits

[Learn More: Audit Logs](../features/audit-logs.md)

---

### Automated Workflows
- Scheduled access expiration
- Welcome email automation
- Offboarding automation
- Access request approvals

**Use Case**: Reduce manual work, ensure compliance

[Learn More: Automation](../features/automation.md)

## Setup Guide for Recruiters

### Initial Setup (30 minutes)

**Step 1: Create Your Workspace**
```
Organization Setup → Recruiting Team
└── Roles to Create:
    ├── Recruiter (full access)
    ├── Hiring Manager (candidate review only)
    ├── Interviewer (feedback only)
    ├── Candidate (assessment access)
    └── Contractor (limited recruiter access)
```

**Step 2: Configure Templates**
- Candidate access template
- Interviewer access template
- Contractor access template

**Step 3: Set Retention Policies**
- Candidate data: 90 days after rejection
- Contractor data: 30 days after contract end
- Interview feedback: 1 year

**Step 4: Enable Integrations**
- ATS integration (Greenhouse, Lever, etc.)
- Calendar integration (Google Calendar)
- Communication (Slack, email)

### Daily Operations

**Adding a Candidate**:
1. Click "New Guest User"
2. Select "Candidate Template"
3. Set expiration date (typically 90 days)
4. Send invitation email
5. Track access in dashboard

**Scheduling Interviews**:
1. Create interview workspace
2. Add candidate profile
3. Invite interviewers
4. Set expiration for day after interview
5. Collect feedback

**Offboarding**:
- Rejected candidates: Auto-expire after 90 days
- Contractors: Revoke access on last day
- Review access logs quarterly

## Integration with ATS

### Greenhouse Integration
1. Enable Greenhouse in Integrations
2. Configure webhook for new candidates
3. Auto-create guest accounts
4. Sync candidate status
5. Auto-revoke on rejection

[Setup Guide: Greenhouse](../features/integrations/greenhouse.md)

### Lever Integration
Similar flow to Greenhouse with automated provisioning.

[Setup Guide: Lever](../features/integrations/lever.md)

### Custom ATS
Use our API to build custom integrations.

[API Documentation](../api/README.md)

## Compliance for Recruiters

### GDPR Compliance
- **Right to Access**: Export all candidate data on request
- **Right to Delete**: One-click data deletion
- **Purpose Limitation**: Separate candidate vs. employee data
- **Audit Trail**: Complete access logs

### CCPA Compliance
- Data inventory tracking
- Access request handling
- Deletion request processing

### Interview Feedback Privacy
- Encrypted feedback storage
- Access limited to hiring team
- Automatic redaction of identifying info (optional)

[Learn More: Compliance](./compliance.md)

## Pricing for Recruiting Teams

### Professional ($X/user/month)
- Unlimited guest accounts
- Access templates
- Basic automation
- Email support

### Enterprise (Custom)
- ATS integrations
- Advanced automation
- Compliance features
- Dedicated support
- SLA guarantees

**Volume Discount**: 20% off for 50+ recruiters

## Best Practices

### 1. Use Templates Consistently
Create templates for each candidate stage to ensure consistent access and easier auditing.

### 2. Set Expiration Dates
Always set expiration dates for guest access. Recommend:
- Candidates: 90 days
- Interviewers: 2 days
- Contractors: Contract end date + 7 days

### 3. Regular Access Reviews
Monthly: Review all active guest accounts
Quarterly: Audit access logs for compliance

### 4. Automate Where Possible
- Auto-provisioning from ATS
- Auto-expiration based on status
- Auto-notification before expiration

### 5. Document Your Processes
Create internal wiki with:
- When to grant access
- Permission levels for each role
- Offboarding checklist
- Emergency access procedures

## Case Study: GlobalRecruit

**Company**: GlobalRecruit (500-person recruiting firm)

**Challenge**: Managing access for 2,000+ active candidates and 50 contract recruiters

**Solution**:
- Implemented candidate access templates
- Integrated with Greenhouse ATS
- Set up automated expiration
- Created contractor role with limited scope

**Results**:
- 70% reduction in access provisioning time
- 100% audit trail compliance
- Zero data breaches
- $50K annual savings in admin time

[Read Full Case Study](./case-studies/globalrecruit.md)

## Common Questions

**Q: Can candidates create their own accounts?**
A: No, for security. Recruiters must invite candidates via email.

**Q: What happens when a candidate is hired?**
A: You can convert guest account to employee account, preserving their data.

**Q: Can we integrate with our ATS?**
A: Yes, we support Greenhouse, Lever, and custom integrations via API.

**Q: How long is data retained?**
A: You configure retention policies. We recommend 90 days for rejected candidates.

## Resources

- [Recruiter Onboarding Checklist](./recruiter-checklist.pdf)
- [GDPR Compliance Guide](./gdpr-recruiting.pdf)
- [ATS Integration Videos](https://youtube.com/aceunlock-recruiting)

## Get Started

1. [Create your account](../getting-started/create-account.md)
2. [Set up recruiting workspace](../getting-started/recruiting-setup.md)
3. [Configure your first template](../features/access-templates.md)
4. [Invite your first candidate](../features/guest-access.md)

---

**Questions?** Email recruiting@aceunlock.com or [schedule a demo](https://aceunlock.com/demo/recruiting).
