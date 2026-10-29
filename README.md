# THE FINALS compatibility

**Check compatibility status in the main repository before downloading or opening an issue.** [View compatibility status ↗](https://github.com/zzoko/mac-gaming-compatibility#readme)

**YouTube setup video:** [Watch on YouTube](https://www.youtube.com/watch?v=5emn-mqPV5A) (The video covers ARC Raiders, but the installation method is the same.)

<br><br>

Choose one ZIP matching your CrossOver version and how you launch Steam.

| Package | Version |
| --- | --- |
| CrossOver Preview 27.0.0.41073 — NotProton Steam native | 0.1.0-alpha8 |
| CrossOver Preview 27.0.0.41073 — CrossOver Steam bottle | 0.1.0-alpha8 |
| CrossOver 26.3 — NotProton Steam native | 0.1.0-alpha8 |
| CrossOver 26.3 — CrossOver Steam bottle | 0.1.0-alpha8 |

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
when an upstream fix is verified. It recognizes the affected curve by its structure and
preserves the game's normal visibility rules. Unrecognized patterns remain unchanged.
No game shaders are included, and users do not need Xcode, Python or a compiler.

Source, licenses and rebuild instructions are included under `Support`.
ZIP checksums are in `SHA256SUMS.txt`.

## Game specific information

- **Shader-cache recovery:** for recurring graphics freezes, quit the game and try **5 — Clear D3DMetal shader cache** in `Install.command`. It rebuilds automatically; expect shader-compilation stutter.

<details>
<summary><strong>Changelog</strong></summary>

**0.1.0-alpha8 (27 October 2026)**

- Replaced the M5-only shader-hash recipes with automatic structural detection, intended to recognize the same affected curve on other GPU families.
- The same single installer includes the prebuilt component; no developer tools are required.
- Local component and installer checks passed. Preview + NotProton also reached the menu with exposed skin confirmed visible on M5. M4 and older chips still need confirmation from users; unsupported shader layouts keep their original behavior.

**0.1.0-alpha7 — Preview downloads (26 October 2026)**

- Updated Preview graphics defaults.
- Added shader-cache recovery guidance. CrossOver 26.3 downloads remain at alpha6.

**0.1.0-alpha6 (October 2026)**

- Preview downloads now target **CrossOver Preview 20261015 (27.0.0.41073)**, which official NotProton supports (the previous July Preview build was not).
- NotProton downloads now require **NotProton 1.2.1**.
- The S12 skin correction covered this Preview build on the tested M5; exposed arms rendered correctly in first and third person. Those hash recipes did not cover the reported M4 Pro. CrossOver 26.3 keeps its own unchanged correction.
- **Fixed:** freezes after long play caused by an oversized D3DMetal shader cache: the launcher clears the cache once after such a hang, and `Install.command` has a new **5 Clear D3DMetal shader cache** option.
- The Steam compatibility tool is now simply named **THE FINALS - CrossOver &lt;version&gt;**.
- Tested: Preview + NotProton launches with the skin correction working. The other downloads use the same fixes but were not separately launch-tested.

</details>

If you'd like to support compatibility work and ongoing maintenance:

<p>
  <a href="https://ko-fi.com/andreiii22"><img src="docs/images/support-kofi.svg" alt="Support on Ko-fi" width="250" height="64"></a>&nbsp;
  <a href="https://github.com/sponsors/zzoko"><img src="docs/images/github-sponsors.svg" alt="Support through GitHub Sponsors" width="250" height="64"></a>
</p>
