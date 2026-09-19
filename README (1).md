# Sathi — a daily companion for senior citizens

Built for the PromptWars Warm-up Challenge (Google for Developers).

## The problem
Most digital tools are designed for tech-savvy, younger users, leaving seniors feeling overwhelmed or excluded in an increasingly online-first world.

## The solution
Sathi is a single-page, GenAI-styled companion website that goes beyond a simple chatbot:

- **Proactive assistance** — a "Right now" focus card surfaces the single most important thing (a medicine reminder) instead of a wall of options.
- **Simplifies complex information** — "Ask Sathi" answers everyday questions (bigger text, OTP scams, video calls, bill payment) in short, numbered, plain-language steps, and can **read the answer aloud** using the browser's built-in text-to-speech.
- **Anticipates needs** — a short daily task list for health, family, and bills, with one-tap "mark as done."
- **Genuinely supportive & trustworthy** — a "Learn as you go" section explains things like OTP safety and scam-call red flags in plain language, plus one-tap calling for trusted family contacts and an SOS button for emergencies (112).
- **Tailored to pace and comfort** — a working accessibility bar (A+/A−, high-contrast mode) that remembers the person's preference on their device, built on Atkinson Hyperlegible, a typeface designed specifically for low-vision readability.

## Tech stack
Plain HTML, CSS, and vanilla JavaScript — a single self-contained file, no build step, no dependencies. Uses the browser's native `SpeechSynthesis` API for read-aloud and `localStorage` for remembering accessibility preferences.

## Files
- `sathi.html` — the entire application (open directly in any browser)

## Running it locally
No install needed:
```bash
# just open it
open sathi.html         # macOS
start sathi.html        # Windows
xdg-open sathi.html     # Linux
```
Or serve it (useful if your submission form wants a URL):
```bash
python3 -m http.server 8000
# then visit http://localhost:8000/sathi.html
```

## Deploying it for a submission link
Any static host works, for example:
- **GitHub Pages**: push `sathi.html` (rename to `index.html`) to a repo, enable Pages in Settings → Pages → deploy from `main`.
- **Netlify / Vercel drop**: drag the `sathi.html` file onto netlify.com/drop or vercel.com's new-project import.

## Extending it (next steps beyond the warm-up)
- Swap the canned "Ask Sathi" answers for a real GenAI call (Gemini API) so it can handle open-ended questions, not just the seeded ones.
- Add speech-to-text input so seniors can ask by voice, not just typing.
- Pull real task data from a calendar or family-shared list instead of the hardcoded sample day.
