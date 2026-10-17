# THE FINALS compatibility — 0.1.0-alpha2

If you'd like to support the compatibility work and ongoing maintenance:

<p>
  <a href="https://ko-fi.com/andreiii22"><img src="docs/images/support-kofi.svg" alt="Support on Ko-fi" width="250" height="64"></a>&nbsp;
  <a href="https://github.com/sponsors/zzoko"><img src="docs/images/github-sponsors.svg" alt="Support through GitHub Sponsors" width="250" height="64"></a>
</p>

Choose **one** ZIP matching your CrossOver version and how you launch Steam. Extract it completely, read its setup guide, then open `Install.command`.

| Download | Use it with | Current validation |
| --- | --- | --- |
| THE FINALS — CrossOver 26.3 — CrossOver Steam bottle | Stable 26.3.0.39832; Windows Steam inside CrossOver | Installer, CPU/memory/TLS and CrossOver icon checks passed. Separate bottle gameplay pending. |
| THE FINALS — CrossOver 26.3 — NotProton Steam native | Stable 26.3.0.39832 runner; native macOS Steam with NotProton | Practice Range and clean lobby relaunch confirmed. Full stable online match pending. |
| THE FINALS — CrossOver Preview 27.0.0.40734 — CrossOver Steam bottle | This exact Preview app; its Windows Steam bottle | Installer, CPU/memory/TLS and icon checks passed. Earlier private Windows Steam setup completed an online match; final packaged bottle gameplay pending. |
| THE FINALS — CrossOver Preview 27.0.0.40734 — NotProton Steam native | This exact Preview runner; native macOS Steam with NotProton | Byte-identical runtime passed native gameplay and repeated lobby launches. Package checks passed. |

## CrossOver Steam bottle

Use the **CrossOver Steam bottle** ZIP. Install Windows Steam and THE FINALS in a 64-bit bottle using your own matching CrossOver app. Extract the ZIP, close applications in that bottle, open Install.command and choose Install / update. Select the app and bottle. Reopen CrossOver and launch **THE FINALS (Patched)** inside that bottle. The ordinary Steam icon and other games remain intact. Use CrossOver's bottle graphics controls.

The installer creates a private runtime under `~/Library/Application Support/THE FINALS Compatibility/`; it does not replace your installed CrossOver application. Stable uses GPTK3; Preview uses GPTK4.

## NotProton Steam native

Use the **NotProton Steam native** ZIP. Set up the matching Rosetta runner in NotProton, install THE FINALS through native macOS Steam, quit Steam, then extract the ZIP and open Install.command. Restart Steam, select the named THE FINALS compatibility tool, and use the normal NotProton graphics controls. No CrossOver-managed Steam bottle or full Windows Steam client is required. Steam supplies the game-library path; the adapter maintains its own prefix.

## Package contents

Each ZIP includes Install / Verify / Restore / Remove, route-specific instructions and validation, guarded patches, dependency manifests, automatic checks, corresponding source, rebuild instructions, licenses and checksums. Extract the entire ZIP and keep Support beside Install.command. Requirements are Apple Silicon, Rosetta and compatible macOS 27.x; checks target actual components rather than one OS build number.

CrossOver itself must be supplied by the recipient. These downloads contain no complete CrossOver/Apple runtime, Steam, NotProton, game, prefix or account data. Game and protection binaries are unchanged. These packages have not been released publicly. The parent project's personal Preview installation remains separate.

Read each archive's VALIDATION.md before choosing a route. A second Mac and future game/OS/runtime builds have not been tested.
