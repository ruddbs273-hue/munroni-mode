# Screen defaults

Build these into new screens, mockups and forms from the start. Do not make the user point them out again.

## Plain, but with the structure visible

- No decoration: left accent bars, timeline connector lines and circles, initial-letter avatars, ⓘ icons and gray help boxes, colored dots in front of status or menu rows, vertical dividers between metric cells, repeated values, decorative gradients. If a legend is needed, use the real mark (a map pin and so on). A check mark without a circle on a finished step is not decoration.
- No duplicate displays, no numbers or step numbers nobody needs, no standing notices ("only managers can see this", "this is a test"). Hide what a user has no permission for instead of explaining it. The only text to keep is errors, confirmations for actions that cannot be undone, and numeric limits such as file count and size.
- When you remove something, remove the empty space it leaves too. Keep the top of the screen light.
- Plain does not mean the structure is invisible. When a screen has several groups, show where each one ends with a structural element such as a tinted header band or a bordered panel. Test it by checking whether you can count the groups within a second.
- Use few colors. The only accent color is the brand color. Reuse existing colors for status. Do not color table headers or titles. Do not build hierarchy by making titles and totals big. Use spacing, text color and weight instead.
- A selected row gets a fill plus a border so it still shows on a dim screen.
- Do not add a tab or a menu for every new feature. Attach it to the screen where that data already lives, and open forms in a small dialog.
- Screens for outside users (customers, partners) are simpler than internal ones. Without any training, they should see what they need to do now, with one button to press at that moment. However many internal states exist, they show up as a few to-do groups. Internal category names and internal amounts (fees, margins and so on) are never shown.

## Tables

- Headers are always centered. In the body, only sentence-like cells such as titles and memos are left-aligned. Everything else (status, number, owner, date, amount, quantity) is centered.
- Write amounts with their currency ($1,500, ₩15,000). Split a cell that mixes numbers and text into two cells. In card layouts on narrow screens, drop the table alignment and align left.
- Search conditions go in a filter bar at the top. Table view controls (view switch, collapse, Excel export) go right above the table on the right. Do not mix the two.

## Control shapes and names

- Tell kinds of controls apart by shape. Switches turn things on and off, buttons perform actions, and rounded chips are only for single-choice filters.
- The same action always has the same shape and the same name. Do not change its color by row position. A button that only opens a screen does not get an action name like "Send".
- Action buttons have an icon and a label. Icon-only buttons are for universal, safe actions in tight spots (close, refresh, Excel download), and then they get both aria-label and title. Search, Cancel and Apply are text only. Dangerous actions such as delete, send and pay always keep their label. An "open" link inside a row is colored text with a small icon, not a boxed button.
- Labels on work screens use the terms the business already uses (e.g. Order, Invoice, Pending), not chatty paraphrases ("stuff to make", "waiting for an answer"). Name labels from the viewer's side.

## What colors mean

- Red is only for deleting and for things past a set date. The delete confirmation button is solid red, and a delete label or trash icon inside a row is red too. Use one red value everywhere. The × for close, remove or cancel is not red.
- "Overdue" is only for things past a set deadline or due date. For the days since something came in, do not use "overdue", red or orange. Write "N days ago" in plain text. To surface old items, sort oldest first.

## Dialogs and confirmation

- A dialog with input fields does not close when the user clicks outside it. Only [Cancel] and Esc close it. Confirmation dialogs, read-only dialogs and popovers do close on an outside click.
- A button that changes the other party's state (a customer, a partner, another team) opens a confirmation in the form "X will happen. Continue?", with the real values in it (the other party's name, the amount). A dialog where the user types or picks a reason is already the confirmation, so do not stack another one on it. Notes, file uploads and drafts save without confirmation.
- Put a consent checkbox right above the confirm button. Its text is one factual line about the outcome, e.g. "Once paid, this order cannot be canceled." Do not use "I agree to..." wording. The error text is "Please review the above and check the box."
- Long read-only text expands in place ("Show all", "Collapse") instead of opening in a popup. Keep long groups collapsed, and when the user picks one from a list, expand only that one.
- Make failures visible. A failed or bounced send is never left showing "done". Raise a notification.

## Input

- Build in input help before anyone asks: automatic formatting for phone numbers and business or tax IDs, thousands separators for amounts and quantities (with the cursor kept in place), a numeric keypad for number fields (inputMode), address search, autocomplete for names, companies and addresses, and type="email" for email fields. Store digits only and show the formatted value on screen.
- Do not leave a stray 0 showing in number fields. Reopen a form with the saved values, not the defaults. Show applied settings (such as a percentage) when viewing. Keep line breaks in multi-line text.
- A "type your own" option is a combo box the user can type into directly, not an extra field underneath.

## AI indicators

- While AI is running, show a spinner and "AI is reading…", and block a second click. Use one shared spinner component.
- AI-made records and drafts get only a small "AI-written" tag. Documents that go to customers do not get it.
- Automation stops at sorting and drafting. Sending anything outside and finalizing are done by a person pressing a button. Keep the number of "needs checking" items handed to people as low as possible.

## Phones and finishing

- On phone lists, do not lay the filters out at the top. Show the current conditions in one line and a "Filters n" button that opens a bottom sheet.
- On small screens, scale everything down so it fits at a glance. Do not enlarge text or line height.
- Check the finish before reporting: centering, shadow size, white bands at borders, clipping (logos and the like), icons spilling out of cells, awkward gaps and overlaps.
- After adding a section, check that the existing layout around it (column count, alternating left and right) is unchanged. Do not change an existing layout unless asked.
