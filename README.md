# THE FINALS compatibility

Choose one ZIP matching your CrossOver version and how you launch Steam.

| Package | Version |
| --- | --- |
| CrossOver Preview 27.0.0.40734 — NotProton Steam native | 0.1.0-alpha4 |
| CrossOver Preview 27.0.0.40734 — CrossOver Steam bottle | 0.1.0-alpha3 |
| CrossOver 26.3 — NotProton Steam native | 0.1.0-alpha4 |
| CrossOver 26.3 — CrossOver Steam bottle | 0.1.0-alpha3 |

**Requirements:** Apple Silicon, macOS 27.x, Rosetta, the matching CrossOver
version, and a Steam copy of THE FINALS. Native Steam also requires NotProton 1.2.0.

Extract the whole ZIP, open `Install.command`, and choose **Install / update**.
The CPU compatibility correction and S12 skin correction are included in that one installation.

- **CrossOver Steam bottle:** launch **THE FINALS (Patched)** inside your selected bottle.
- **NotProton Steam native:** restart Steam, select the game's compatibility tool, and click **Play**.

The installer creates a private runtime and preserves your installed CrossOver app
and game files. Verification and rollback are included. Each ZIP's `VALIDATION.md`
records what was tested for that route; results for one route do not certify the others.

The skin correction is a separate internal component that can be retired independently
when an upstream fix is verified. It applies only to matching converted shaders and
preserves the game's normal visibility rules. No game shaders are included in the download.

Source, licenses and rebuild instructions are included under `Support`.
ZIP checksums are in `SHA256SUMS.txt`.

If you'd like to support compatibility work and ongoing maintenance:

<p>
  <a href="https://ko-fi.com/andreiii22"><img src="docs/images/support-kofi.svg" alt="Support on Ko-fi" width="250" height="64"></a>&nbsp;
  <a href="https://github.com/sponsors/zzoko"><img src="docs/images/github-sponsors.svg" alt="Support through GitHub Sponsors" width="250" height="64"></a>
</p>
