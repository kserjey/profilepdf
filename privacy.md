---
title: Privacy policy
permalink: /privacy/
---

# ProfilePDF privacy policy

_Last updated: 2026-11-01_

ProfilePDF is a Chrome extension that turns the LinkedIn profile page you have open into a PDF
résumé. This policy explains what it handles, what (little) leaves your device, and the choices
you have. ProfilePDF is not affiliated with or endorsed by LinkedIn.

**In short:** the profile and the PDF are processed only in your browser and are never sent to
us or anyone else. Unless you turn it off, the extension sends a small amount of anonymous
technical diagnostics (error codes, counts and timings) so we can tell when a LinkedIn change has
broken it.

## 1. Profile content: processed locally, never sent

When you click the extension icon on a LinkedIn profile page, ProfilePDF reads that page to
build the PDF. This can include the person's name, headline, location, photo, About text,
experience, education, languages and company logos. To get the full Experience, Education and
Languages lists, it also loads that profile's own "Show all" pages from linkedin.com, in your
existing LinkedIn session, the same as if you opened them yourself.

All of this happens inside your browser:

- The profile content is used only to generate the PDF. It is **not** sent to us or to any third
  party, and the extension does not store it.
- The finished PDF is saved to your Downloads folder like any other download. ProfilePDF keeps no
  copy.
- The extension only runs when you click its icon on a page. It does not read other tabs or your
  browsing history, and it does not run in the background on websites.

If you save a profile that isn't yours, you are responsible for using that person's information
lawfully, for example only for a purpose they would reasonably expect, such as a hiring process
they are part of.

## 2. Anonymous diagnostics

To find and fix problems (most often a LinkedIn layout change that breaks extraction),
ProfilePDF sends technical events to [PostHog](https://posthog.com), an analytics provider. We
use its EU-hosted service.

**What is sent:**

- **Run outcome:** whether creating a PDF succeeded, the step where it stopped (for example
  "extract" or "render"), a fixed error code (for example `render-failed`) and how long it took.
  If some text could not be drawn in the PDF, it also includes how many characters were left out
  and which broad script groups they belong to (for example "Chinese, Japanese or Korean" or
  "Arabic"). The characters themselves are never sent.
- **Extraction quality:** which profile sections were found on the page (yes/no per section),
  how many entries were found (for example "4 experience entries"), and for each "Show all"
  page, whether loading it worked, its HTTP status code and how long it took.
- **Technical context:** the extension version and the Chrome version.
- **A random install ID:** a random number created by the extension, so we can tell one
  installation's repeated errors from many users hitting the same error. It is not linked to your
  name, email, LinkedIn account or anything else about you.

**What is never sent:** profile content of any kind (names, text, photos, companies), page URLs
or profile addresses, the PDF, your browsing history, or free-form error messages.

**Your IP address:** like any web request, the request to PostHog carries your IP address.
PostHog is configured to discard it on receipt. It is not stored and is not used to work out
your location.

**Retention:** diagnostic events are deleted after 12 months.

**Legal basis (EU/UK GDPR):** our legitimate interest in keeping the extension working
(Art. 6(1)(f)). You can object at any time by turning diagnostics off (see section 4).

## 3. What the extension stores on your device

In Chrome's extension storage, on your computer only:

- your diagnostics setting (on or off),
- your PDF choices (page size, and whether to include your photo),
- the random install ID,
- a short queue of diagnostic events not yet sent (at most 100). Each is removed once sent,
- the result of your last run on each open tab (the saved file name, which includes the profile name, or an error message). It is kept in the browser's memory only, never written to disk, and is cleared when you close the tab or the browser.

Turning diagnostics off deletes the install ID and the queue. Uninstalling the extension deletes
everything.

## 4. Your choices

- **Turn diagnostics off:** right-click the ProfilePDF icon in the toolbar → **Options**, and untick
  **Share anonymous diagnostics**. Nothing more is sent, and the install ID and any unsent
  events are deleted from your device.
- **Remove everything:** uninstall the extension.
- **Data already sent:** diagnostics carry no information that identifies you, so we cannot find
  "your" events, and that includes when you ask us to. Your events are deleted automatically after 12 months.

## 5. What we don't do

- We don't sell or rent any data.
- We don't use data for advertising, credit decisions or profiling.
- We don't transfer data to anyone except PostHog, which processes it on our behalf as described
  above.

The use of information received from Chrome APIs adheres to the
[Chrome Web Store User Data Policy](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq),
including the Limited Use requirements.

## 6. Permissions the extension asks for

| Permission  | Why                                                                  |
| ----------- | -------------------------------------------------------------------- |
| `activeTab` | Read the profile page you clicked the icon on, and only that page.   |
| `scripting` | Run the code that reads the profile, on that page, when you click.   |
| `downloads` | Save the generated PDF to your Downloads folder.                     |
| `offscreen` | Generate the PDF in a hidden extension page, so no server is needed. |
| `storage`   | Remember your diagnostics setting, your page size and photo choices, the install ID and unsent events, and show your last result if you reopen the popup. |

## 7. Children

ProfilePDF is not directed at children under 16.

## 8. Changes

If this policy changes, the new version will be posted on this page with a new "Last updated"
date. The full history is available in this site's
[repository](https://github.com/kserjey/profilepdf/commits/main/privacy.md).

## 9. Contact

Questions or requests: **kserjey2store@gmail.com**
