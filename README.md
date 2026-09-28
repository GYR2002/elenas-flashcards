# Elena’s Flashcards

A small flashcard app in one file, `index.html`. To use it, double-click the file and it opens in your browser. It needs no install and no internet.

## How to use
1. **Create a deck**, e.g. "Spanish verbs".
2. **Add cards** one at a time (word + definition), or open **"Add many at once"**:
   - Paste a list with one card per line, e.g. `casa - house`. The app recognises a tab, ` - `, `:`, `=`, `;` or `,` between the word and the definition.
   - Or click **Import CSV / text file…** and pick a CSV file (e.g. from Excel or Google Sheets) with the word in column A and the definition in column B.
   - Words already in the deck are skipped.
3. **Study**
   - **Review due cards** shows the cards that are due. Flip the card, then rate yourself:
     *Hard* (comes back a few cards later in this session), *Good* (comes back tomorrow) or *Easy* (comes back in 3 days).
   - **Browse all**: flip through every card with Prev / Next / Shuffle.
   - **Exam mode**: every word in the deck, shuffled, round after round until you leave, whether or not you already know it. You can still press Hard / Good / Easy, but they change nothing: no schedule, no stats.
   - **Show first** switches between word → definition and definition → word.
   - **Skip**: not sure yet? Press *Skip* (or `S`). Skipped cards come back at the end of the session.
   - Keyboard: `Space` = flip, `←` `→` = previous / next, `1` `2` `3` = Hard / Good / Easy, `S` = skip, `Esc` = back.
4. **Front page: practise across all decks**
   - **Daily challenge**: 30 words a day from all decks, the ones you find hardest first. A word counts on the progress bar once you rate it *Good* or *Easy*; *Hard* words come back later in the session. Your progress is kept if you stop and continue later that day. A new set starts each day. Open **Today’s words** in the box to see the list, with which ones you already know. **Reset** starts the day over with new words.
   - **Test random words**: 10, 20 or 50 random cards from all decks.
   - Next to the daily challenge sits a stick figure on the toilet. He strains harder as your progress bar fills and only succeeds when the challenge is done.
   - **Streak**: the number of days in a row you finished the daily challenge (🔥 on the front page). Missing a day resets it. When you finish, a popup shows your streak filling toward the next milestone (3, 7, 14, 30, 60, 100, 200, 365 days).
   - **Missed days**: after 1 missed day he's red and sweating from the start. After 2 he's purple, bloated and desperate. After 3 he dies of constipation, and a gravestone stays until you finish a challenge. Then he flies out of the toilet like Superman and sits back down.
   - Both are practice only: they don't change when a card is due in *Review due cards*. They do remember which words you miss, so the daily challenge can pick your weakest words.

5. **Deck results**: each deck shows **Your results**: how many answers were *Hard*, *Good* and *Easy*, the % right, and a chart of the last 14 days (hover or tap a day for its numbers). Every kind of test counts, except exam mode. Click **Hard**, **Good** or **Easy** to see which words you rated that way and how often.
   - **Words you keep missing** lists the words you get wrong more often than right, up to 5% of the deck (at least 1). **Practise these** tests just those words (practice only).

## Ready-made decks
The `vocabulary/` folder has veterinary anatomy lists. For each one, create a deck (e.g. "Vet anatomy – Bones"), open **Add many at once → Import CSV / text file…**, pick the file and press **Add cards**.

## Your data
Cards are saved **in the browser you use** (localStorage), right after every change. They stay there when you close the tab or the browser.

Unfinished typing (a half-typed card, a card you are editing, a pasted list) is saved too: every 3 minutes, when you switch away from or close the tab, and when you press **Save now** (bottom right) or `Ctrl/Cmd+S`. When you open the app again, it goes back to the deck you had open, with your typing still in place. The bottom-right line shows when it last saved.

But:
- another browser or device won't see them, and
- clearing your browser data deletes them.

Use **Export backup** on the home screen to save a `.json` file, and **Import backup** to load it on another device or browser. Import merges: it adds decks and cards you don't already have.

## Files
- `index.html`: the whole app (HTML, CSS and JavaScript in one file)
- `vocabulary/*.csv`: ready-to-import word lists
