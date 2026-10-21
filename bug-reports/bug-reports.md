# Bug Reports — Templates and Examples

This document provides a reporting template and hypothetical examples for practice. **The examples below are not confirmed defects in JSONPlaceholder.** Do not report them as real findings without reproducing them.

## Bug report template

- **ID:** BUG-XXX
- **Title:** `[Component] Short description of the issue`
- **Environment:** OS, browser/client, build/version
- **Preconditions:** State required before testing
- **Steps to reproduce:**
  1. Step one
  2. Step two
- **Actual result:** What happened
- **Expected result:** What should happen
- **Severity:** Critical / Major / Moderate / Minor / Trivial
- **Priority:** P1 / P2 / P3 / P4
- **Attachments:** Screenshot, request/response, logs

## Hypothetical example

**Title:** `[Posts API] Response returns a string instead of a numeric ID`

- **Environment:** API client, test environment
- **Preconditions:** A post exists
- **Steps to reproduce:**
  1. Send `GET /posts/1`.
  2. Inspect the type of the `id` field.
- **Actual result:** Hypothetical: `id` is returned as a string.
- **Expected result:** `id` is returned as a number, according to the API contract.
- **Severity:** Moderate, if the consumer contract requires a numeric ID.
- **Priority:** To be assigned based on product impact and release context.

This is a training example only. The actual API response must be checked before filing a defect.
