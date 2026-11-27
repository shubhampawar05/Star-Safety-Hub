# Feedback branch: Vikas review, 27 Nov 2026

Source of the prototype (Design canvas format). `index.html` on this branch is still the old export; download a new export from the preview canvas and replace it before merging.

## Changes
- Forms open as modal popups: new lead, mark as lost, log activity, add contact, upload document, view document, meeting-recording summary, upload PO, log reminder, request priority. Close with ×, Cancel, Esc or a click outside.
- New lead: company name, plant, industry, source; contact person name, designation, department, phone, email; several product lines, each with sizes, quantity, target price and customisation; salesperson assignment for admins. Required fields are checked.
- Activity log records who from the customer (contact chips or a typed name), what was discussed, date and time, who from our side, where (meetings), outcome, next step and next follow-up. The timeline shows all of these.
- Contacts show phone and email, with Call, WhatsApp, Email and "Log what happened" buttons, plus Add contact.
- Documents have View (preview popup) and Download buttons. In the prototype the download is a sample text file.
- Requirement card lists each product line separately with its standard.
- Notification bell in the header: follow-ups due, priority requests, late-penalty dates within 7 days, new customer reminders, overdue shipments and payments over 45 days, with unread count and Mark all as read.

## PO changes
- PO page redesigned: header with customer PO, plant and handler; progress line (PO received → In queue → In production → Ready to pack → Dispatched → Delivered → Paid); key dates with days left; payment terms; delivery address and invoice envelope; items with size-wise quantities and totals; production chart; customer reminders; PO history.
- Production button: "Go to Production queue · #3 of 5" while the order waits. Once it starts, a green "Added to production · being made now" status replaces it. When made items are done, it shows "Production done" and a "Go to Dispatch" button.
- Orders list: deliver-by with days left, item summary, clear status, reminders, and filters (All, Waiting, In production, Ready to dispatch) with counts.
- New order (upload PO): the AI-read fields and item lines are editable (customer PO number, dates, penalty, payment terms; item, sizes, quantity per size, Make or Buy-in; add or remove items), with checks before saving.
