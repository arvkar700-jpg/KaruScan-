# KaruScan

KaruScan finds the AI tools and app subscriptions charging your bank card, shows which ones you don't use or don't recognise, and helps you cancel them.

**Use it:** https://arvkar700-jpg.github.io/KaruScan-/

Your statement is read inside your own browser and never uploaded. There is no account, no tracking and no server. Saved payments are kept unencrypted in that browser, so use KaruScan on a device only you use. See the [privacy policy](privacy.html).

## Install it on your phone or tablet

- **iPhone or iPad:** open the link in Safari, tap Share, then "Add to Home Screen".
- **Android:** open the link in Chrome, tap the ⋮ menu, then "Install app" (or tap "Install KaruScan" on the page).

KaruScan then opens from its own icon, full screen, and works without internet.

## How to use it

1. **Add a statement.** Export your transactions as CSV from internet banking, or open a PDF statement, copy all the text, and paste it in. Add 2 to 6 months so KaruScan can see repeating charges.
2. **Review each subscription.** Choose when you last used it. KaruScan labels it Keep, Review, Cancel this, or Dispute with bank.
3. **Cancel.** Open "How to cancel" for the company's billing page, step-by-step instructions, a cancellation email and a bank dispute letter.
4. **Check next month.** Add the next statement. Any charge after you cancelled is flagged in red.

KaruScan can't sign in to your bank or app accounts, so the final "Cancel" click is always yours.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets phones install KaruScan with its name and icon |
| `sw.js` | Saves the app on the device so it works offline |
| `privacy.html` | Privacy policy |
| `icons/` | App icon in Papua New Guinea flag colours (`icon-teal.svg` is the alternative design) |
| `tests/` | Automated checks of statement reading, estimates, backups and letters |

## Publishing an update

1. Edit the files.
2. Run the checks: `npm ci` once, then `npm test`. They also run on GitHub after every push.
3. Change `VERSION` at the top of `sw.js` (for example `karuscan-v3`) so installed copies pick up the change.
