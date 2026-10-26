# THE FINALS compatibility

Choose one ZIP matching your CrossOver version and how you launch Steam.

| Package | Version |
| --- | --- |
| CrossOver Preview 27.0.0.41073 — NotProton Steam native | 0.1.0-alpha6 |
| CrossOver Preview 27.0.0.41073 — CrossOver Steam bottle | 0.1.0-alpha6 |
| CrossOver 26.3 — NotProton Steam native | 0.1.0-alpha6 |
| CrossOver 26.3 — CrossOver Steam bottle | 0.1.0-alpha6 |

**Requirements:** Apple Silicon, macOS 27.x, Rosetta, the matching CrossOver
version, and a Steam copy of THE FINALS. Native Steam also requires NotProton 1.2.1.
For Preview, download `crossover-preview-20261015.zip` from CodeWeavers' Preview Center (not the `arm64` one).

Extract the whole ZIP, open `Install.command`, and choose **Install / update**.
The CPU compatibility correction and S12 skin correction are included in that one installation.

- **CrossOver Steam bottle:** launch **THE FINALS (Patched)** inside your selected bottle.
- **NotProton Steam native:** restart Steam, select **THE FINALS - CrossOver 26.3** or **THE FINALS - CrossOver Preview 27.0.0.41073** as the compatibility tool, and click **Play**.

The installer creates a private runtime and preserves your installed CrossOver app
and game files. Verification and rollback are included. Each ZIP's `VALIDATION.md`
records what was tested for that route; results for one route do not certify the others.

The skin correction is a separate internal component that can be retired independently
when an upstream fix is verified. It applies only to matching converted shaders and
preserves the game's normal visibility rules. No game shaders are included in the download.

Source, licenses and rebuild instructions are included under `Support`.
ZIP checksums are in `SHA256SUMS.txt`.

## Game specific information

- **Ray tracing (CrossOver Preview):** turned off by default, because it currently fails on this Preview build. To test it anyway, add `D3DM_SUPPORT_DXR=1` before `%command%` in Steam's Launch Options (NotProton) — expect a crash if it is still unsupported.
- **Freeze after long play:** if THE FINALS freezes after loading in (audio keeps playing) and then shows an "Unhandled page fault" popup, the D3DMetal shader cache has grown too large for the Apple GPU driver. The launcher now clears that cache automatically once after such a hang. You can also clear it yourself: quit the game, open `Install.command` and choose **5 Clear D3DMetal shader cache**, or run `rm -rf "$(getconf DARWIN_USER_CACHE_DIR)d3dm/Discovery.exe"`. It rebuilds by itself; expect some stutter for the first session or two.

<details>
<summary><strong>Changelog</strong></summary>

**0.1.0-alpha6 (October 2026)**

- Preview downloads now target **CrossOver Preview 20261015 (27.0.0.41073)**, which official NotProton supports (the previous July Preview build was not).
- NotProton downloads now require **NotProton 1.2.1**.
- The S12 skin correction now also covers this Preview build; exposed arms render correctly in first and third person. CrossOver 26.3 keeps its own unchanged correction.
- Ray tracing is turned off on the Preview (see Game specific information).
- **Fixed:** freezes after long play caused by an oversized D3DMetal shader cache: the launcher clears the cache once after such a hang, and `Install.command` has a new **5 Clear D3DMetal shader cache** option.
- The Steam compatibility tool is now simply named **THE FINALS - CrossOver &lt;version&gt;**.
- Tested: Preview + NotProton launches with the skin correction working. The other downloads use the same fixes but were not separately launch-tested.

</details>

If you'd like to support compatibility work and ongoing maintenance:

<p>
  <a href="https://ko-fi.com/andreiii22"><img src="docs/images/support-kofi.svg" alt="Support on Ko-fi" width="250" height="64"></a>&nbsp;
  <a href="https://github.com/sponsors/zzoko"><img src="docs/images/github-sponsors.svg" alt="Support through GitHub Sponsors" width="250" height="64"></a>
</p>
