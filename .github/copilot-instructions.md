# Copilot instructions

Project context Copilot should apply to every session in this repository.

## Stack

- Framework: Astro (static output).
- Language: TypeScript.
- Styling: plain CSS in the base layout.

## Conventions

- Keep components small and focused.
- Prefer semantic HTML and accessible markup.
- Do not close, or add closing keywords for, the exercise walkthrough issue (issue #1) in any pull request. The exercise's GitHub Actions workflows manage that issue. When you open a pull request for app work, link only the specific app work-item issue you are implementing.

## Persistence and hydration rules

- Bookmarks are persisted in the browser using `localStorage` under the `mona-bookmarks` key. Treat stored JSON as untrusted and validate every entry as a `{url, slug}` object before rendering.
- All browser-only code, including every `localStorage` access, must run behind a `client:load` boundary or the component's inline `<script>` so the static Astro build never touches browser APIs during SSR.
