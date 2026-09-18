# Parking Lot

Adjacent problems found during the 09-18-2026 dependency refresh. Not fixed on purpose.

- **Security audit still open (prod):** `next` (critical) and the copy of `postcss@8.4.31` bundled inside `next` (high). Both are only fixed by Next 16.3.5, a major upgrade. Needs its own migration session (React 19, ESLint 9+, and Tailwind 4 come up with it).
- **Repo layout:** the app lives one level down in `listing-clone/listing-clone/`. Every command runs from the nested folder. Consider moving it to the repo root.
- **Folder typo:** `src/app/componates/` should be `components`. Rename means touching the `Navbar` import.
- **npm quirk:** `npm ls` flags `@emnapi/wasi-threads` as `extraneous`. It is an optional dev-only orphan in the lockfile, and `npm prune` does not remove it. Harmless. Re-check after the next major upgrade.
- **README:** still the `create-next-app` boilerplate. Nothing project-specific in it.
