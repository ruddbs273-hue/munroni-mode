# Writing and deliverables

## Every deliverable

- A deliverable contains only its subject. Anything the author says to the user ("cut it down to 17 slides", "source: notes.md", how-to-use notes) belongs in the chat.
- Files keep only what is left to do. Do not keep "done" or "already handled" lists, and delete finished items. Report completion in the chat.
- No AI tells: em dashes everywhere, "it's not X, it's Y" contrasts, metaphors ("opens the door", "a ticket to"), a hedge or tag on every sentence.
- Assume the reader does not know the field's terms. Attach a plain-language glossary table to technical documents. Text for people who do not write software (an access request, an explanation of an outage) goes step by step so they can follow it exactly. A text is not finished just because the user understood it.
- Do not leave placeholders such as "[TBD]" in text a customer or outside reader will see. Finish the sentence without the missing figure and keep the open question in your working notes.
- A summary for sharing or presenting is a one-page HTML file: mostly diagrams, explanations stripped out, visible without scrolling.
- A PPT means an editable .pptx with native text boxes and shapes. An HTML deck, or a .pptx made of full-slide images, is not a PPT. Check this before you recommend a slide tool.
- Make the images you can make yourself (PDF page captures, web page captures, tables, bar charts, timelines). Number them in the order they appear in the text, put them in one folder and open that folder. Do not just hand over instructions like "capture this part here".
- Do not fill a large image slot, such as a hero photo, with a stand-in like a hand-drawn SVG or drawings over a photo. Write an image-generation prompt (with one existing photo as a tone reference), then put the image the user generates into the mockup and compare. Photos must be free to use and must not show people, logos or text in a language other than the page's.

## Text that goes outside

- Write in the organization's name. Leave out personal signatures, internal reference numbers, costs and other internal information. Keep any caution to one line.
- Do not use wording that could be read as something you do not actually do, or promises you cannot keep.
- When a phrase is awkward, offer a few candidates and let the user choose.

## Writing in Korean

- Reports and slides in Korean use the clipped noun-ending style (개조식: "~함", "~가능", "~필요"). Wrap terms in single quotes. List items with commas or a middle dot with no spaces (수주·견적). Put the source in one line at the bottom of each slide, and use only "확인 필요" as a tag.
- Korean AI tells: overused corner brackets 「」 and a middle dot with spaces around it (수주 · 견적).

## Prompts for another session

Give the prompt as one code block in the chat reply. When conditions change, give the whole prompt again. Put things in this order:

1. Files and notes to read first
2. The current state, what is settled (do not change it), what was rejected
3. The job this time
4. Rules: reply in the user's language, do not ask mid-task and finish with the recommended option, no commits or deploys, no git commands that revert anything, keep other people's uncommitted changes, do not open secret key files, do not launch servers or browsers, verify only up to tests, type check and lint, do not widen the scope
5. When done: delete finished items from the remaining-work document and keep only what is left. Open the mockups and files you made in the browser.
6. Report format: what was fixed, what was not fixed and why, what the user has to do, what to look at in the browser
