---
title: "Accessibility"
description: "AceUnlock accessibility statement, WCAG 2.1 AA conformance report (VPAT), known limitations, remediation roadmap, and how to report barriers"
has_children: false
nav_order: 7
permalink: /accessibility/
---

# Accessibility

AceUnlock is committed to making its products usable by everyone, including people who rely on assistive technology. This page contains our accessibility statement, our current Accessibility Conformance Report (ACR) in VPAT® 2.5 format, known limitations with their remediation plan, and how to report an accessibility barrier.

**Jump to Section:**
- [Accessibility Statement](#accessibility-statement)
- [Supported Accessibility Features](#supported-accessibility-features)
- [Known Limitations and Remediation Plan](#known-limitations-and-remediation-plan)
- [Reporting Accessibility Barriers](#reporting-accessibility-barriers)
- [How We Verify Conformance](#how-we-verify-conformance)
- [Accessibility in Our Development Process](#accessibility-in-our-development-process)
- [Accessibility Roadmap](#accessibility-roadmap)
- [Accessibility Conformance Report (VPAT 2.5, WCAG Edition)](#accessibility-conformance-report)

---

## Accessibility Statement

**Standard:** AceUnlock has adopted the Web Content Accessibility Guidelines (WCAG) 2.1 Level AA as its accessibility standard. We are not currently assessed against additional standards such as Section 508 or EN 301 549.

**Scope of the current assessment:** The Accessibility Conformance Report on this page covers the **AceUnlock Job Seeker Interview Portal**, the candidate-facing web application used by job seekers and students to complete AI-powered interviews and mock interviews. It does not cover:

- the internal recruiter and career services portal, whose ACR is planned for November 2026, and
- the public marketing website at [www.aceunlock.com](https://www.aceunlock.com).

**Self-assessment:** The current report is a self-assessment conducted by the AceUnlock team, led by Sam Surkhang, CTO. A third-party accessibility audit has not yet been conducted. We plan to engage an independent accessibility firm in Q1 2027.

**No separate accessibility mode:** AceUnlock does not use a separate accessibility mode, lite version, alternate interface, or accessibility overlay. Accessibility is built directly into the standard interface that all users use.

**Remediation commitment:** We maintain a documented remediation roadmap for the gaps identified in our assessment, with target dates. Where a barrier cannot be fixed immediately, we will work with the institution to provide an equally effective alternative. This page will be updated as issues are resolved and after any third-party evaluation.

---

## Supported Accessibility Features

The candidate interview portal is built with Angular using accessible coding practices. Features verified in the current assessment include:

- **Keyboard operation:** Every control is a native button, input, select, or checkbox and is operable with the keyboard alone. Resume upload offers a keyboard-operable "browse files" button as an alternative to drag and drop.
- **Visible focus:** Every focusable element shows a 2-pixel outline with a 2-pixel offset when focused via keyboard.
- **Screen reader support:** Form fields are programmatically labelled, error messages are associated with their fields, each screen uses header and main landmarks with a single h1 and a logical heading hierarchy, dialogs expose the dialog role with an accessible name, and status changes are announced through live regions.
- **Colour and contrast:** All text meets a minimum contrast ratio of 4.5:1. Errors, permission status, recording status, and time warnings are conveyed as text, not colour alone.
- **Zoom and reflow:** Content and functionality remain available at 200% browser zoom. Job Posting, Welcome, Consent, Pre-Interview Setup, and Thank You screens reflow to a single column at 320 CSS pixels.
- **Reduced motion:** Decorative animations and pulsing indicators are disabled when the operating system's reduced-motion preference is enabled.
- **Accessible authentication:** Candidates sign in with a one-time code sent by email. No password, CAPTCHA, or other cognitive function test is required, and the code field supports pasting and browser autofill.
- **Target size:** All controls are at least 24 by 24 CSS pixels. Interview controls are 60 pixels or larger.
- **No redundant entry:** The email address from the invitation is pre-filled and details entered in setup are carried through the rest of the flow.

---

## Known Limitations and Remediation Plan

The following gaps were identified in the current assessment. Each is tracked as a labelled issue in GitHub and remediated through our change management process.

| Area | Limitation | Planned remediation |
|:-----|:-----------|:--------------------|
| Live captions (1.2.4) | The AI interviewer's speech is not captioned or transcribed on screen during the live interview. | **Priority 1.** Display a live transcript of the interviewer's speech in the interview room. |
| Prerecorded captions and transcripts (1.2.2, 1.2.3, 1.2.5) | Natively hosted recruiter welcome videos do not support a caption track, and the recruiter-written description shown beside the video is not a full transcript or audio description. | Caption track support for natively hosted videos, a transcript field for welcome videos, and recruiter guidance requiring captions. |
| Interview time limit (2.2.1) | The interview time limit set by the recruiter cannot be extended or turned off by the candidate during the interview. | Per-candidate extended-time accommodation configurable by the recruiter, and an in-interview extension prompt. |
| Dialog focus management (2.4.3, 2.4.11) | When the Terms and Conditions dialog or the stop-interview confirmation opens, focus is not moved into the dialog or returned to the triggering control on close, and focus can move behind the overlay. When the setup wizard advances a step, focus returns to the top of the document. | Focus management for dialogs and step changes, focus containment for dialogs, and Escape to close dialogs. |
| Document language (3.1.1) | When a job posting is configured in Spanish, French, or German, the candidate flow is translated but the document language attribute remains "en". | Set the document language from the job posting's language. |
| Interview room reflow (1.4.10) | The Interview Room uses a fixed viewport-height layout with hidden overflow, so at 320 pixels wide or 400% zoom some content may be clipped. | Allow the interview room to scroll vertically on small viewports. |
| End Interview confirmation (3.3.4) | The End Interview control ends and submits the interview immediately without confirmation. | Add a confirmation step to End Interview. |
| Third-party video player (4.1.2) | The embedded YouTube player used for recruiter welcome videos has known ARIA attribute defects outside AceUnlock's control. | No direct fix available. Recruiter guidance and native hosting with captions are on the roadmap. |

**Recent fixes** completed during the assessment include adding labels to form fields in the interview flow, adjusting button, link, helper-text, and status colours to meet the 4.5:1 contrast threshold, improving colour contrast on the consent screen flow, and removing component styles that suppressed the browser focus outline on inputs and selects.

---

## Reporting Accessibility Barriers

Anyone, including students and candidates, can report an accessibility barrier:

- **Email:** [support@aceunlock.com](mailto:support@aceunlock.com) with "Accessibility" in the subject line.
- **Institutional users:** through the support feature in the recruiter portal.

When reporting, please include the page or step where the problem occurred, the browser and assistive technology you were using, and what you expected to happen.

**What happens next:**

1. Reports are acknowledged within **5 business days**.
2. Each report is tracked as a labelled issue in GitHub and prioritized according to its impact on users.
3. Fixes are delivered through our standard change management process, documented in our Software Development Policy.
4. Where a barrier cannot be fixed immediately, we will work with you to provide an equally effective alternative.

---

## How We Verify Conformance

Conformance with WCAG 2.1 Level AA is verified through:

- **Automated testing:** Key screens are scanned with axe DevTools before each major release, in default, populated, error, and dialog-open states.
- **Manual keyboard-only testing:** Every in-scope user flow is completed with the keyboard alone, verifying reachability, focus visibility, focus order, focus management in dialogs, and operation of custom controls.
- **Screen reader testing:** VoiceOver with Safari on macOS on the candidate flows.
- **Visual testing:** Browser zoom at 200% and 400%, text spacing overrides, colour contrast analysis of text and UI components, and review of colour-only indicators.
- **Formal assessment:** A VPAT/ACR against WCAG 2.1 Level AA, updated annually and after significant UI changes, with a third-party audit planned for Q1 2027.
- **Issue tracking:** Issues found through testing or user reports are tracked as labelled GitHub issues and fixed through our change management process.

Manual testing is performed at least annually and for significant UI changes.

---

## Accessibility in Our Development Process

Accessibility is built into each stage of our development lifecycle:

- **Planning:** Code change plans for user-facing changes consider accessibility impact against WCAG 2.1 Level AA.
- **Development:** Developers follow accessible coding practices (semantic HTML, labelled controls, keyboard support, sufficient colour contrast), supported by Angular ESLint accessibility rules.
- **Review:** Pull requests for UI changes include an accessibility check as part of peer review.
- **Testing:** Key screens are scanned with axe, and significant UI changes are manually tested with keyboard navigation and VoiceOver.
- **Tracking:** Accessibility issues are tracked as labelled GitHub issues and fixed through our change management process.
- **Training:** Developers complete the W3C Web Accessibility Initiative's Digital Accessibility Foundations course at onboarding.

---

## Accessibility Roadmap

| When | Milestone |
|:-----|:----------|
| September 2026 | Self-assessed VPAT/ACR for the candidate interview portal completed and published (see below). |
| October 2026 | Automated accessibility testing (axe) of the recruiter portal; publish accessibility statement and reporting process. |
| November 15, 2026 | Complete and publish a self-assessed VPAT/ACR against WCAG 2.1 Level AA for the recruiter portal. |
| December 2026 – January 2027 | Remediate issues identified in the VPAT, prioritizing the candidate interview flow, starting with live captions. |
| Q1 2027 | Independent third-party accessibility audit, led by Sam Surkhang, CTO. |
| Q2 2027 | Remediate audit findings and publish an updated ACR. |
| Ongoing | Annual VPAT/ACR updates and accessibility checks for significant UI changes. |

---

## Accessibility Conformance Report

### WCAG Edition, based on VPAT® Version 2.5Rev

| | |
|:--|:--|
| **Name of Product/Version** | AceUnlock Job Seeker Interview Portal |
| **Report Date** | September 2026 |
| **Product Description** | AceUnlock is a web-based hiring platform that helps recruiters screen candidates using AI interviewers. It is delivered as a browser-based single-page application and allows candidates to interview on a website. |
| **Contact Information** | Sam Surkhang, CTO, [support@aceunlock.com](mailto:support@aceunlock.com) |

A copy of this report is also available as a document: [AceUnlock ACR (Google Docs)](https://docs.google.com/document/d/1NqOZZ479BvC88WDaP8b8iK5kRHa48eCu/edit?usp=sharing).

### Notes

This report covers the AceUnlock candidate / job seeker web application as accessed through a desktop browser. It does not cover the public marketing website ([www.aceunlock.com](https://www.aceunlock.com)) or the internal recruiter portal.

This is a self-assessment conducted by the AceUnlock team using the methods described below. AceUnlock is committed to improving the accessibility of its product and maintains a remediation roadmap for the gaps identified in this report. This report will be updated as issues are resolved and after any third-party evaluation.

### Evaluation Methods Used

Testing was performed on September 23, 2026 against the production build of the interview portal and candidate site using the following methods:

- **Automated testing:** axe DevTools run on every in-scope screen in default, populated, error, and dialog-open states.
- **Manual keyboard-only testing:** every in-scope user flow completed with keyboard alone, verifying reachability, focus visibility, focus order, focus management in dialogs, and operation of custom controls.
- **Screen reader testing:** VoiceOver with Safari on macOS on the candidate flows.
- **Visual testing:** browser zoom at 200% and 400%, text spacing overrides, colour contrast analysis of text and UI components, and review of colour-only indicators.

**Screens and flows evaluated:**

- Job Posting
- Welcome
- Pre-Interview User Information
- Pre-Interview OTP page
- Pre-Interview Microphone and Camera
- Interview Room
- Thank You

**Browsers:** Google Chrome, Safari

### Applicable Standards/Guidelines

This report covers the degree of conformance for the following accessibility standards/guidelines:

| Standard/Guideline | Included In Report |
|:-------------------|:-------------------|
| [Web Content Accessibility Guidelines 2.0](https://www.w3.org/TR/WCAG20/) | Level A (Yes), Level AA (Yes), Level AAA (No) |
| [Web Content Accessibility Guidelines 2.1](https://www.w3.org/TR/WCAG21/) | Level A (Yes), Level AA (Yes), Level AAA (No) |
| [Web Content Accessibility Guidelines 2.2](https://www.w3.org/TR/WCAG22/) | Level A (Yes), Level AA (Yes), Level AAA (No) |

### Terms

The terms used in the Conformance Level information are defined as follows:

- **Supports:** The functionality of the product has at least one method that meets the criterion without known defects or meets with equivalent facilitation.
- **Partially Supports:** Some functionality of the product does not meet the criterion.
- **Does Not Support:** The majority of product functionality does not meet the criterion.
- **Not Applicable:** The criterion is not relevant to the product.
- **Not Evaluated:** The product has not been evaluated against the criterion. This can only be used in WCAG Level AAA criteria.

### WCAG 2.x Report

Note: When reporting on conformance with the WCAG 2.x Success Criteria, they are scoped for full pages, complete processes, and accessibility-supported ways of using technology as documented in the [WCAG 2.0 Conformance Requirements](https://www.w3.org/TR/WCAG20/#conformance-reqs).

Rows marked "Applies to" indicate criteria introduced in WCAG 2.1 or 2.2. All other criteria apply to WCAG 2.0, 2.1, and 2.2.

#### Table 1: Success Criteria, Level A

| Criteria | Conformance Level | Remarks and Explanations |
|:---------|:------------------|:-------------------------|
| **1.1.1 Non-text Content** (Level A) | Supports | The company logo carries alternative text. Decorative icons are hidden from assistive technology. The candidate's camera preview and self-view video and the optional welcome video are labelled. The only image-based content is the recruiter-supplied logo. |
| **1.2.1 Audio-only and Video-only (Prerecorded)** (Level A) | Supports | Prerecorded audio/video has a text alternative. |
| **1.2.2 Captions (Prerecorded)** (Level A) | Partially Supports | Recruiters may add an optional welcome video to a job. When hosted on YouTube or Vimeo, captions are available through the hosting platform's player if the recruiter has enabled them. Natively hosted welcome videos do not yet support a caption track. Candidate interview recordings are not played back to candidates. Remediation roadmap: caption track support for natively hosted videos and recruiter guidance requiring captions. |
| **1.2.3 Audio Description or Media Alternative (Prerecorded)** (Level A) | Partially Supports | The welcome page displays a recruiter-written text description alongside the optional welcome video, but this is not a full transcript or audio description. Remediation roadmap: transcript field for welcome videos. |
| **1.3.1 Info and Relationships** (Level A) | Supports | Form fields are programmatically labelled. Required fields carry the required attribute. Error messages are associated with their fields using aria-describedby and aria-invalid. Each screen uses header and main landmarks and a single h1 with a logical heading hierarchy. Lists use list markup. Dialogs expose the dialog role with an accessible name. Progress indicators expose progress bar roles and values. Note: job descriptions and consent text are authored by the recruiter as rich text; their internal structure depends on the recruiter's content. |
| **1.3.2 Meaningful Sequence** (Level A) | Supports | All screens use a single-column linear layout. The DOM order matches the visual reading order. No CSS reordering is used. |
| **1.3.3 Sensory Characteristics** (Level A) | Supports | Instructions refer to controls by their visible label, for example "Continue" and "Allow Access". No instruction relies on shape, colour, size, or position. |
| **1.4.1 Use of Color** (Level A) | Supports | Field validation errors are shown as text messages in addition to a red border. Camera and microphone permission status is shown as text ("Granted", "Denied"). Recording status is shown as text alongside the indicator dot. Interview time warnings change the status text as well as the timer colour. |
| **1.4.2 Audio Control** (Level A) | Supports | _[TO CONFIRM: the source ACR repeats the 1.4.1 remarks in this row. Replace with a remark specific to audio control, for example whether any audio plays automatically for more than 3 seconds and how the candidate can pause, stop, or mute it.]_ |
| **2.1.1 Keyboard** (Level A) | Supports | All controls are native buttons, inputs, selects, and checkboxes and are operable with the keyboard. Resume upload offers a keyboard-operable "browse files" button as an alternative to drag and drop. Dialogs are closed with a keyboard-reachable Close or Cancel button. Camera and microphone permissions are granted through the browser's native prompt. |
| **2.1.2 No Keyboard Trap** (Level A) | Supports | Focus can be moved away from every component using standard keys. The Terms dialog and the stop-interview confirmation are dismissed with a button. The embedded YouTube player, when present, allows focus to leave the frame. |
| **2.1.4 Character Key Shortcuts** (Level A)<br>Applies to: WCAG 2.1 and 2.2 | Not Applicable | The product does not implement any single-character keyboard shortcuts. |
| **2.2.1 Timing Adjustable** (Level A) | Partially Supports | The interview has a time limit set by the recruiter per job posting (default 10 minutes). The remaining time is displayed throughout and the status text warns at 30 seconds and 10 seconds. When time expires the interview closes after a short grace period. The candidate cannot extend or turn off the limit within the interview. The email verification code can be re-sent at any time. Remediation roadmap: per-candidate extended-time accommodation configurable by the recruiter, and an in-interview extension prompt. |
| **2.2.2 Pause, Stop, Hide** (Level A) | Supports | The only moving content is a decorative animation representing the AI interviewer and pulsing status indicators. These are disabled when the operating system's reduced-motion preference is enabled. There are no carousels, auto-scrolling regions, or auto-updating content other than the visible interview timer. |
| **2.3.1 Three Flashes or Below Threshold** (Level A) | Supports | No content flashes. The fastest animation cycles once per second. |
| **2.4.1 Bypass Blocks** (Level A) | Supports | Each screen exposes header and main landmarks so assistive technology users can move directly to content. There is no block of navigation repeated across pages, so a skip link is not required. |
| **2.4.2 Page Titled** (Level A) | Supports | Every route sets a descriptive document title, for example "Pre-Interview Setup \| Aceunlock" and "Interview Room \| Aceunlock". |
| **2.4.3 Focus Order** (Level A) | Partially Supports | Tab order follows the visual order on every screen. When the Terms and Conditions dialog or the stop-interview confirmation opens, focus is not moved into the dialog and is not returned to the triggering control on close. When the setup wizard advances a step, focus returns to the top of the document. Remediation roadmap: focus management for dialogs and step changes, and Escape to close dialogs. |
| **2.4.4 Link Purpose (In Context)** (Level A) | Supports | Link text describes its destination, for example "Terms and Conditions". Links inside recruiter-authored job descriptions and consent text are the recruiter's content. |
| **2.5.1 Pointer Gestures** (Level A)<br>Applies to: WCAG 2.1 and 2.2 | Supports | No multipoint or path-based gestures are required. Resume drag and drop has a single-click alternative. |
| **2.5.2 Pointer Cancellation** (Level A)<br>Applies to: WCAG 2.1 and 2.2 | Supports | All actions are triggered on the standard click event, which fires on pointer release. No functionality is bound to the down-event. |
| **2.5.3 Label in Name** (Level A)<br>Applies to: WCAG 2.1 and 2.2 | Supports | The accessible name of every control is its visible text label. Icon glyphs are excluded from accessible names. |
| **2.5.4 Motion Actuation** (Level A)<br>Applies to: WCAG 2.1 and 2.2 | Not Applicable | No functionality is triggered by device motion or user motion. |
| **3.1.1 Language of Page** (Level A) | Partially Supports | The page language is declared as English. Recruiters may configure a job posting in Spanish, French, or German, in which case the candidate flow is translated but the document language attribute remains "en". Remediation roadmap: set the document language from the job posting's language. |
| **3.2.1 On Focus** (Level A) | Supports | Receiving focus does not trigger any change of context. |
| **3.2.2 On Input** (Level A) | Supports | Changing an input does not automatically submit or navigate. The verification code is submitted with an explicit Verify button. Selecting a different camera only updates the preview. Resume upload requires an explicit Upload button. |
| **3.2.6 Consistent Help** (Level A)<br>Applies to: WCAG 2.2 only | Supports | The candidate flow does not include a help mechanism, so the criterion is met. Recruiter contact information appears within the job posting content. |
| **3.3.1 Error Identification** (Level A) | Supports | Required name and email fields display a text error message identifying the problem, associated with the field and announced to assistive technology. Verification code errors, resume upload errors, and connection errors are presented as text in an alert region. |
| **3.3.2 Labels or Instructions** (Level A) | Supports | Every input has a visible label. Required fields are marked with an asterisk. Format guidance is provided for the verification code (6 digits), the LinkedIn URL, and the resume (PDF or Word, 5 MB maximum). |
| **3.3.7 Redundant Entry** (Level A)<br>Applies to: WCAG 2.2 only | Supports | The email address from the interview invitation is pre-filled. Name and contact details entered in the setup step are carried through to resume upload and the interview without being requested again. |
| **4.1.1 Parsing** (Level A)<br>Applies to: WCAG 2.0 and 2.1 only (removed in WCAG 2.2) | Supports | WCAG 2.2 removed this criterion. For WCAG 2.0 and 2.1, the W3C considers the criterion met where content is HTML rendered by modern browsers. |
| **4.1.2 Name, Role, Value** (Level A) | Supports | Controls use native HTML elements that expose name, role, and state. Mute and camera toggles expose their pressed state. Dialogs expose the dialog role and an accessible name. Progress bars expose current and maximum values. Loading, success, and error states are announced through status and alert regions. Note: the embedded YouTube player used for recruiter welcome videos is third-party content with known ARIA attribute defects outside Aceunlock's control. |

#### Table 2: Success Criteria, Level AA

| Criteria | Conformance Level | Remarks and Explanations |
|:---------|:------------------|:-------------------------|
| **1.2.4 Captions (Live)** (Level AA) | Does Not Support | The interview is a live spoken conversation with an AI interviewer. The AI's speech is not currently captioned or transcribed on screen. Candidates who are deaf or hard of hearing cannot follow the interviewer's questions without external captioning. Remediation roadmap (priority 1): display a live transcript of the interviewer's speech in the interview room; the text is already delivered to the browser by the voice service. |
| **1.2.5 Audio Description (Prerecorded)** (Level AA) | Partially Supports | Applies only to the optional recruiter-supplied welcome video. The platform does not provide an audio description track. Welcome videos are typically a recruiter speaking to camera, where the audio conveys the content, and a recruiter-written text description is shown beside the video. |
| **1.3.4 Orientation** (Level AA)<br>Applies to: WCAG 2.1 and 2.2 | Supports | Content is not restricted to a single display orientation. The interview room provides layouts for both portrait and landscape viewports. |
| **1.3.5 Identify Input Purpose** (Level AA)<br>Applies to: WCAG 2.1 and 2.2 | Supports | Personal data fields declare their purpose using autocomplete attributes: given-name, family-name, email, url (LinkedIn profile), and one-time-code for the verification code. |
| **1.4.3 Contrast (Minimum)** (Level AA) | Supports | All text meets a minimum contrast ratio of 4.5:1 against its background, verified with axe DevTools on each screen. Button, link, helper-text, and status colours were adjusted during this assessment to meet the threshold. |
| **1.4.4 Resize Text** (Level AA) | Supports | Layouts use flexible widths and responsive breakpoints. Content and functionality remain available at 200% browser zoom. |
| **1.4.5 Images of Text** (Level AA) | Supports | No text is presented as an image. The only image is the recruiter's company logo. |
| **1.4.10 Reflow** (Level AA)<br>Applies to: WCAG 2.1 and 2.2 | Supports | Job Posting, Welcome, Consent, Pre-Interview Setup, and Thank You reflow to a single column at 320 CSS pixels without horizontal scrolling. The Interview Room uses a fixed viewport-height layout with hidden overflow, so at 320 pixels or 400% zoom some content may be clipped. Remediation roadmap: allow the interview room to scroll vertically on small viewports. |
| **1.4.11 Non-text Contrast** (Level AA)<br>Applies to: WCAG 2.1 and 2.2 | Supports | Focus indicators are a 2-pixel outline at 3.66:1. Text input, select, and file drop-zone borders are 4.54:1. Buttons use solid fills with text meeting 4.5:1. Checkboxes use the browser's native rendering with an accent colour at 3.66:1. |
| **1.4.12 Text Spacing** (Level AA)<br>Applies to: WCAG 2.1 and 2.2 | Partially Supports | Text containers do not use fixed heights, and cards expand with their content. No clipping is expected when line height is set to 1.5, paragraph spacing to 2x, letter spacing to 0.12 em, and word spacing to 0.16 em. |
| **1.4.13 Content on Hover or Focus** (Level AA)<br>Applies to: WCAG 2.1 and 2.2 | Supports | The product does not implement custom tooltips or popovers. Interview control buttons expose a native browser tooltip through the title attribute alongside a visible text label; native tooltips are user-agent controlled and excluded from this criterion. |
| **2.4.5 Multiple Ways** (Level AA) | Not Applicable | The candidate application is a single sequential process (job posting, welcome, consent, setup, interview, thank you). WCAG exempts pages that are steps in a process. |
| **2.4.6 Headings and Labels** (Level AA) | Supports | Each screen has a single descriptive h1 stating its purpose. Section headings and form labels describe their content, for example "Camera Access", "Verification Code", "What happens next". |
| **2.4.7 Focus Visible** (Level AA) | Supports | Every focusable element shows a 2-pixel outline with a 2-pixel offset when focused via keyboard. Component styles that previously suppressed the browser outline on inputs and selects were removed during this assessment. |
| **2.4.11 Focus Not Obscured (Minimum)** (Level AA)<br>Applies to: WCAG 2.2 only | Partially Supports | On the desktop, no sticky header, footer, or toast covers focused elements. On small viewports the interview control bar is fixed to the bottom and the content area is padded so focused controls stay visible. While the Terms dialog or the stop-interview confirmation is open, focus can move to content behind the overlay, where it is hidden. Remediation roadmap: focus containment for dialogs (same item as 2.4.3). |
| **2.5.7 Dragging Movements** (Level AA)<br>Applies to: WCAG 2.2 only | Supports | Resume upload supports drag and drop, and the same action is available through a single-pointer "browse files" button. No other functionality uses dragging. |
| **2.5.8 Target Size (Minimum)** (Level AA)<br>Applies to: WCAG 2.2 only | Supports | All controls are at least 24 by 24 CSS pixels. Interview controls are 60 pixels or larger, the remove-file button is 32 pixels, and the dialog close button is 36 pixels. Checkboxes are 18 pixels but sit inside a larger clickable label. The Terms and Conditions link is inline text and is exempt. |
| **3.1.2 Language of Parts** (Level AA) | Supports | Each job posting is presented in a single language selected by the recruiter. No passages in a second language are inserted by the product. |
| **3.2.3 Consistent Navigation** (Level AA) | Supports | The candidate flow has no repeated navigation. Step navigation ("Back", "Continue") appears in the same position and order on every setup step. |
| **3.2.4 Consistent Identification** (Level AA) | Supports | Controls with the same function use the same label on every screen: "Continue", "Back", "Apply Now", and the interview controls Mute, Video, Stop, and End. |
| **3.3.3 Error Suggestion** (Level AA) | Supports | Error messages state how to correct the input, for example "Please enter a valid email address, for example name@example.com". Resume upload errors state the accepted formats and size limit. Verification code errors explain that the code is incorrect or expired and offer a Resend Code control. |
| **3.3.4 Error Prevention (Legal, Financial, Data)** (Level AA) | Partially Supports | Consent requires an explicit checkbox and a Continue action. Stopping the interview recording asks for confirmation. The End Interview control ends and submits the interview immediately without confirmation. When the interview time limit expires, the interview is submitted automatically after a grace period. Remediation roadmap: confirmation on End Interview. |
| **3.3.8 Accessible Authentication (Minimum)** (Level AA)<br>Applies to: WCAG 2.2 only | Supports | Candidates authenticate with a one-time code sent by email. No password, CAPTCHA, or other cognitive function test is required. The code field accepts pasting and declares the one-time-code autocomplete purpose so browsers and password managers can fill it. |
| **4.1.3 Status Messages** (Level AA)<br>Applies to: WCAG 2.1 and 2.2 | Supports | Loading states, verification code errors, permission results, resume upload progress and result, the interviewer's status line including the time-remaining warnings, recording status, and the interview upload progress are exposed through status or alert live regions so screen readers announce them without a change of focus. |

#### Table 3: Success Criteria, Level AAA

Level AAA success criteria were not evaluated in this assessment.

| Criteria | Conformance Level | Remarks and Explanations |
|:---------|:------------------|:-------------------------|
| **1.2.6 Sign Language (Prerecorded)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.2.7 Extended Audio Description (Prerecorded)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.2.8 Media Alternative (Prerecorded)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.2.9 Audio-only (Live)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.3.6 Identify Purpose** (Level AAA)<br>Applies to: WCAG 2.1 and 2.2 | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.4.6 Contrast (Enhanced)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.4.7 Low or No Background Audio** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.4.8 Visual Presentation** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **1.4.9 Images of Text (No Exception)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.1.3 Keyboard (No Exception)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.2.3 No Timing** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.2.4 Interruptions** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.2.5 Re-authenticating** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.2.6 Timeouts** (Level AAA)<br>Applies to: WCAG 2.1 and 2.2 | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.3.2 Three Flashes** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.3.3 Animation from Interactions** (Level AAA)<br>Applies to: WCAG 2.1 and 2.2 | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.4.8 Location** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.4.9 Link Purpose (Link Only)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.4.10 Section Headings** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.4.12 Focus Not Obscured (Enhanced)** (Level AAA)<br>Applies to: WCAG 2.2 only | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.4.13 Focus Appearance** (Level AAA)<br>Applies to: WCAG 2.2 only | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.5.5 Target Size (Enhanced)** (Level AAA)<br>Applies to: WCAG 2.1 and 2.2 | Not Evaluated | Level AAA success criteria were not evaluated. |
| **2.5.6 Concurrent Input Mechanisms** (Level AAA)<br>Applies to: WCAG 2.1 and 2.2 | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.1.3 Unusual Words** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.1.4 Abbreviations** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.1.5 Reading Level** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.1.6 Pronunciation** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.2.5 Change on Request** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.3.5 Help** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.3.6 Error Prevention (All)** (Level AAA) | Not Evaluated | Level AAA success criteria were not evaluated. |
| **3.3.9 Accessible Authentication (Enhanced)** (Level AAA)<br>Applies to: WCAG 2.2 only | Not Evaluated | Level AAA success criteria were not evaluated. |

---

*"Voluntary Product Accessibility Template" and "VPAT" are registered service marks of the Information Technology Industry Council (ITI).*

*Last updated: September 2026*
