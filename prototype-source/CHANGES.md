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
- Example PO-4477 (Indus Highways, repeat order) is saved but not yet in the production queue, waiting for logo artwork. Its PO page shows an "Add to production queue" button. It appears under a new "Not in queue" filter in Orders and in notifications. The new-order popup has a tick box to add the order to the queue now or later.

## Production queue changes
- Production stages: Added to queue → Cutting → Stitching → Logo printing / embroidery → Reflective tape → Quality check → Ready for packing. Every change is saved with date, time and who updated it.
- "On the floor now" board: count of orders and PO numbers at each stage, plus Not in queue, Waiting and Ready for packing.
- Queue table: when each PO joined the queue and how long it has waited, current stage with how long it has been there and a progress bar, deliver-by with days left. Actions: Start production (first order, admin), Move to next stage (admin), Request priority.
- Timeline per PO (button on each row): every stage with date, time, who updated it and how long it took. Priority moves appear in it too.
- The PO page history and the Orders list show the production stage.
- Open question: the real production stages are not confirmed yet. The stages above are placeholders.

## Dispatch and tracking changes
- Summary boxes: Ready to pack, In transit, Out for delivery, Overdue, Delivered. Clicking one filters the list.
- Shipments list: invoice and PO, customer and city, transporter and LR, dispatched date and time, expected date with days left or days late, last tracking update with time and source (transporter website or a named person), status.
- Shipment details: PO, envelope, box-wise packing, delivery address, printed labels, proof of delivery, and a tracking timeline (Packed → Dispatched → In transit hubs → Out for delivery → Delivered, plus follow-ups) with date, time and source.
- Log follow-up popup: how, who you spoke to, what they said, optional new expected date (keeps the first promised date).
- Update status popup for transporters without online tracking: In transit (with place), Out for delivery, or Delivered (received by, proof of delivery file).
- Pack and dispatch now opens as a popup. Saving it records the Packed and Dispatched entries with time.
