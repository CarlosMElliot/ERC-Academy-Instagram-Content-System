# Publisher Diagnostic — 2026-09-28

This note preserves a historical publishing failure so future chats do not misdiagnose it.

## Context

Target Instagram account: `@erc.nic`.

At the time of diagnosis, ERC Academy Publisher reported that the account was connected and matched the configured Instagram account. The publishing quota was not exhausted.

## #139 attempt

The approved #139 artwork/caption was prepared for publication, but the temporary image-transfer step failed before the image reached the publisher.

Observed transfer error:

`Could not resolve host: steep-lake-7e78.ntpointless-education.workers.dev`

The failure occurred while attempting to send the JPEG to a temporary Cloudflare Workers upload hostname.

## Interpretation

The evidence at that time pointed to a DNS/network-resolution failure on the temporary image-transfer path, not an Instagram authentication failure, caption problem, quota problem or invalid image.

Because the bytes did not reach the temporary upload destination, the normal prepare/publish sequence did not complete and there was no successful publication receipt from that attempt.

## Duplicate-safety rule

Never assume this historical infrastructure problem still exists. Check the current publisher capabilities/state.

If a future prepare or publish operation returns an ambiguous result, inspect the same receipt/container/media state before creating a replacement or retrying blindly.
